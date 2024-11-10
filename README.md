# Guía de niveles - Bandit
## Bandit0
**Objetivo**: Conectarse por SSH al host, encontrar un archivo readme y obtener la contraseña dentro.

1. Conéctate al host usando:

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

**Username**: bandit0

**Password**: bandit0

2. Busca el archivo readme con:

```bash
ls
```

3. Visualiza el contenido del archivo para encontrar la contraseña con:

```bash
cat readme
```
**Password to Bandit1**: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

## Bandit1

1. Sal de Bandit0:

```bash
exit
```

2. Conéctate a Bandit1 usando:

```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```
**Password**: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

3. El archivo que contiene la contraseña tiene un nombre inusual (dash filename). Para visualizar su contenido, usa:

```bash
cat < -
```
**Password to Bandit2**: 263JGJPfgU6LtdEvgfWU1XP5yac29mFx

## Bandit2

1. Sal de Bandit1 y conéctate a Bandit2:

```bash
exit
ssh bandit2@bandit.labs.overthewire.org -p 2220
```
**Password**: 263JGJPfgU6LtdEvgfWU1XP5yac29mFx

2. El archivo con la contraseña tiene espacios en su nombre. Para abrirlo, usa comillas simples alrededor del nombre:

```bash
cat 'nombre del archivo con espacios'
```

**Password to Bandit3**: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

## Bandit3

1. Sal de Bandit2 y conéctate a Bandit3:

```bash
exit
ssh bandit3@bandit.labs.overthewire.org -p 2220
```
**Password**: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

2. El archivo está oculto. Usa ls -a para mostrar archivos ocultos:

```bash
ls -a
```
3. Localiza el archivo en la carpeta inhere y visualiza su contenido con:

```bash
cat .hidden
```
**Password to Bandit4**: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

## Bandit4

1. Sal de Bandit3 y conéctate a Bandit4:

```bash
exit
ssh bandit4@bandit.labs.overthewire.org -p 2220
```
**Password**: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

2. Encuentra un archivo "legible por humanos". Ingresa a la carpeta inhere:

```bash
cd inhere
```

3. Usa el siguiente comando para identificar el archivo human-readable:

```bash
file ./*
```

4. Una vez que encuentres el archivo ASCII (file07), visualiza su contenido:

```bash
cat ./file07
```

**Password to Bandit5**: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

## Bandit5

1. Sal de Bandit4 y conéctate a Bandit5:

```bash
exit
ssh bandit5@bandit.labs.overthewire.org -p 2220
```
**Password**: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

2. Busca un archivo que cumpla estas características: human-readable, tamaño de 1033 bytes y no ejecutable. Usa el siguiente comando:

```bash
find . -type f -size 1033c ! -executable
```

3. Encuentra el archivo adecuado (./maybehere07/.file2) y abrelo:

```bash
cat ./maybehere07/.file2
```

**Password to Bandit6**: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

## Bandit6

1. Sal de Bandit5 y conéctate a Bandit6:

```bash
exit
ssh bandit6@bandit.labs.overthewire.org -p 2220
```
**Password**: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

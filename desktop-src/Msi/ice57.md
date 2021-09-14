---
description: ICE57 valida que los componentes individuales no mezclan datos por equipo y por usuario. Esta acción personalizada de ICE comprueba las entradas del Registro, los archivos, las rutas de acceso de las claves de directorio y los accesos directos no anunciados.
ms.assetid: 3c82efa7-9cf3-4bcd-8ec4-b81d1d7aa0a6
title: ICE57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a59d609e5d7de0011666be0b5cc5e76417d8e67d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074577"
---
# <a name="ice57"></a>ICE57

ICE57 valida que los componentes individuales no mezclan datos por equipo y por usuario. Esta acción personalizada de ICE comprueba las entradas del Registro, los archivos, las rutas de acceso de las claves de directorio y los accesos directos no anunciados.

La combinación de datos por usuario y por máquina en el mismo componente podría dar lugar solo a la instalación parcial del componente para algunos usuarios en un entorno de varios usuarios.

Vea la [**propiedad ALLUSERS.**](allusers.md)

## <a name="result"></a>Resultado

ICE57 publica un error si encuentra algún componente que contenga entradas del Registro por equipo y por usuario, archivos, rutas de acceso de clave de directorio o accesos directos no anunciados.

## <a name="example"></a>Ejemplo

ICE57 informa de los siguientes errores para el ejemplo mostrado.

``` syntax
Component 'Component1' has both per-user and per-machine 
    data with a per-machine KeyPath. 
 
WARNING: Component 'Component2' has both per-user and 
    per-machine data with an HKCU Registry KeyPath. 
 
Component 'Component3' has a registry entry that 
    can be either per-user or per-machine and a per-machine KeyPath. 
 
Component 'Component4' has both per-user data and 
    a keypath that can be either per-user or per-machine.
```

[Tabla de componentes](component-table.md) (parcial)



| Componente  | Directorio  | Atributos | KeyPath |
|------------|------------|------------|---------|
| Componente1 | DirectorioA | 0          | Archivo A   |
| Componente 2 | DirectorioA | 4          | RegKeyB |
| Componente 3 | DirectorioA | 0          | FileC   |
| Componente 4 | DirectorioA | 4          | RegKeyD |



 

[Tabla del Registro](registry-table.md) (parcial)



| Registro | Root | Componente\_ |
|----------|------|-------------|
| RegKeyA  | 1    | Componente1  |
| RegKeyB  | 1    | Componente 2  |
| RegKeyC  | -1   | Componente 3  |
| RegKeyD  | -1   | Componente 4  |



 

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | Componente\_ |
|-------|-------------|
| Archivo A | Componente1  |
| FileB | Componente 2  |
| FileC | Componente 3  |
| Presentado | Componente 4  |



 

[Tabla de directorios](directory-table.md)



| Directorio  | Elemento primario \_ del directorio | DefaultDir |
|------------|-------------------|------------|
| TARGETDIR  |                   | SourceDir  |
| DirectorioA | TARGETDIR         | DirectorioA |



 

Para corregir los errores, reorganice la aplicación de forma que cada componente contenga solo recursos por usuario o por equipo, y no ambos.

El primer mensaje de error se publica porque Component1 contiene FileA (por equipo) y la clave del Registro HKCU RegKeyA (por usuario).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




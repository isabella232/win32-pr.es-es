---
description: ICE57 valida que los componentes individuales no mezclen los datos por equipo y por usuario. Esta acción personalizada de ICE comprueba las entradas del registro, los archivos, las rutas de acceso a las claves del directorio y los métodos abreviados no anunciados.
ms.assetid: 3c82efa7-9cf3-4bcd-8ec4-b81d1d7aa0a6
title: ICE57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a59d609e5d7de0011666be0b5cc5e76417d8e67d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278157"
---
# <a name="ice57"></a>ICE57

ICE57 valida que los componentes individuales no mezclen los datos por equipo y por usuario. Esta acción personalizada de ICE comprueba las entradas del registro, los archivos, las rutas de acceso a las claves del directorio y los métodos abreviados no anunciados.

La combinación de datos por usuario y por equipo en el mismo componente podría dar lugar a la instalación parcial del componente solo para algunos usuarios en un entorno de varios usuarios.

Vea la propiedad [**AllUsers**](allusers.md) .

## <a name="result"></a>Resultado

ICE57 publica un error si encuentra algún componente que contenga entradas de registro por equipo y por usuario, archivos, rutas de acceso de clave de directorio o accesos directos no anunciados.

## <a name="example"></a>Ejemplo

ICE57reports los siguientes errores para el ejemplo que se muestra.

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



| Componente  | Directorio  | Atributos | Rutas |
|------------|------------|------------|---------|
| Component1 | Directorioa | 0          | Archivoa   |
| Component2 | Directorioa | 4          | RegKeyB |
| Component3 | Directorioa | 0          | FileC   |
| Component4 | Directorioa | 4          | RegKeyD |



 

[Tabla del registro](registry-table.md) (parcial)



| Registro | Root | Componente\_ |
|----------|------|-------------|
| RegKeyA  | 1    | Component1  |
| RegKeyB  | 1    | Component2  |
| RegKeyC  | -1   | Component3  |
| RegKeyD  | -1   | Component4  |



 

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | Componente\_ |
|-------|-------------|
| Archivoa | Component1  |
| FileB | Component2  |
| FileC | Component3  |
| Registrado | Component4  |



 

[Tabla de directorio](directory-table.md)



| Directorio  | Directorio \_ primario | DefaultDir |
|------------|-------------------|------------|
| TARGETDIR  |                   | SourceDir  |
| Directorioa | TARGETDIR         | Directorioa |



 

Para corregir los errores, reorganice la aplicación de modo que cada componente contenga solo recursos por usuario o por equipo, y no ambos.

Se envía el primer mensaje de error porque Component1 contiene Filea (por equipo) y la clave del registro HKCU RegKeyA (por usuario).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




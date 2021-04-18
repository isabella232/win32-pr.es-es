---
description: ICE30 valida que la instalación de los componentes que contienen el mismo archivo nunca instala el archivo más de una vez en el mismo directorio.
ms.assetid: 74cb455b-a53e-4c6b-98ff-08cf0858f11f
title: ICE30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78fa96899231015d864e5a0912b8ff73cedbbe75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667758"
---
# <a name="ice30"></a>ICE30

ICE30 valida que la instalación de los componentes que contienen el mismo archivo nunca instala el archivo más de una vez en el mismo directorio.

ICE30 va a todos los componentes de la [tabla componente](component-table.md) y, a continuación, determina el directorio de destino del componente en la [tabla de directorios](directory-table.md). Después, comprueba para ver cuáles de estos componentes se instalan en el mismo directorio de destino. Por último, usa la [tabla de archivos](file-table.md) para comprobar que ninguno de los archivos de estos componentes tiene el mismo nombre.

ICE30 comprueba los nombres de archivo largos (LFN) y los nombres de archivo cortos (SFN).

ICE30 no evalúa las propiedades en la resolución de directorios porque estas propiedades pueden cambiar en tiempo de ejecución y modificar el esquema de resolución de directorios. Esto significa que ICE30 puede detectar colisiones de archivos debido a directorios con la misma propiedad en sus rutas de acceso, pero no detecta colisiones resultantes de dos propiedades que tienen el mismo valor.

## <a name="result"></a>Resultado

ICE30 envía un mensaje de error para cada par de componentes que instala el mismo archivo en el mismo directorio.

## <a name="example"></a>Ejemplo

En el ejemplo mostrado se devuelve dos veces cada uno de los siguientes errores.



| Error o advertencia de ICE30                                                                                                                                                                                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERROR: el archivo de destino ' README. 1o ' está instalado en ' TARGETDIR \\ Product ' por dos componentes diferentes en un sistema SFN: ' Component1 ' y ' Component2 '. Esto rompe el recuento de referencias de componentes.                                                                                           | Component1 y Component2 tienen un archivo denominado ' READEME. 1º '. Al usar nombres de archivo cortos, el instalador instala dir1 y Dir2 en el mismo directorio, el \\ producto targetdir.<br/> ICE30 genera dos errores, uno para cada archivo. En un entorno de creación que muestre ubicaciones de errores, el primer error se encuentra en la entrada de un archivo en la [tabla de archivos](file-table.md)y en la segunda ubicación del otro archivo.<br/> |
| ERROR: la instalación de un componente condicional haría que el archivo de destino ' README. 1o ' se instalara en ' TARGETDIR \\ Common Tools ' por dos componentes diferentes en un sistema LFN: ' Component3 ' y ' Component4 '. Esto interrumpirá el recuento de referencias de componentes.                      | Component4 tiene una entrada en la columna condition de la [tabla Component](component-table.md) y Component3 no. Si [**VersionNT**](versionnt.md) es true, se instala Component4 y existe una colisión con el archivo Léame. 1ª siempre instalado por Component3.<br/> ICE30 genera 4 errores, un par para SFN, uno para LFN.<br/>                                                                                            |
| ADVERTENCIA: el archivo de destino ' README. 1o ' puede instalarse en ' TARGETDIR \\ Common Tools ' mediante dos componentes condicionales diferentes en un sistema SFN: ' Component4 ' y ' Component5 '. Si las condiciones no son mutuamente excluyentes, se interrumpirá el sistema de recuento de referencias de componentes. | Dado que Component4 y Component5 tienen entradas en la columna condición de la [tabla componente](component-table.md) , esta colisión de archivos puede no producirse. ICE30 solo publica una advertencia porque las condiciones deben determinarse en el momento de la instalación.<br/> ICE30 genera 4 Advertencias, una par para SFN, una para LFN.<br/>                                                                                            |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente  | Directorio | Condición |
|------------|-----------|-----------|
| Component1 | Dir1      |           |
| Component2 | Dir2      |           |
| Component3 | Dir3      |           |
| Component4 | Dir3      | VersionNT |
| Component5 | Dir3      | Version9X |



 

[Tabla de directorio](directory-table.md)



| Directorio | \_Directorio principal | DefaultDir                    |
|-----------|-------------------|-------------------------------|
| SOURCEDIR |                   | TARGETDIR                     |
| Dir1      | SOURCEDIR         | Producto \| Component1 del producto:. |
| Dir2      | SOURCEDIR         | Producto:.                     |
| Dir3      | SOURCEDIR         | \|Herramientas comunes comunes:         |



 

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | Componente\_ | FileName   |
|-------|-------------|------------|
| Archivo1 | Component1  | Léame. 1 |
| Archivo2 | Component2  | Léame. 1 |
| File3 | Component3  | Léame. 1 |
| File4 | Component4  | Léame. 1 |
| File5 | Component5  | Léame. 1 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 





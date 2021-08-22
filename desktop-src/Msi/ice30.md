---
description: ICE30 valida que la instalación de los componentes que contienen el mismo archivo nunca instala el archivo más de una vez en el mismo directorio.
ms.assetid: 74cb455b-a53e-4c6b-98ff-08cf0858f11f
title: ICE30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba807ec1eb3bde54b1f115e93c531f24414b75e7a293c8ff1b7d7ff1d3abca8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528665"
---
# <a name="ice30"></a>ICE30

ICE30 valida que la instalación de los componentes que contienen el mismo archivo nunca instala el archivo más de una vez en el mismo directorio.

ICE30 va a todos los componentes de la [tabla Component](component-table.md) y, a continuación, determina el directorio de destino del componente a partir de la [tabla Directory](directory-table.md). A continuación, comprueba cuál de estos componentes se instala en el mismo directorio de destino. Por último, usa la [tabla File para](file-table.md) comprobar que ninguno de los archivos de estos componentes tiene el mismo nombre.

ICE30 comprueba los nombres de archivo largos (LFN) y los nombres de archivo cortos (SFN).

ICE30 no evalúa las propiedades en la resolución de directorios porque estas propiedades pueden cambiar en tiempo de ejecución y modificar el esquema de resolución de directorios. Esto significa que ICE30 puede detectar colisiones de archivos debido a directorios con la misma propiedad en sus rutas de acceso, pero no detecta colisiones resultantes de dos propiedades que tienen el mismo valor.

## <a name="result"></a>Resultado

ICE30 publica un mensaje de error para cada par de componentes que instala el mismo archivo en el mismo directorio.

## <a name="example"></a>Ejemplo

El ejemplo que se muestra devuelve dos veces cada uno de los siguientes errores.



| Error o advertencia de ICE30                                                                                                                                                                                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERROR: El archivo de destino "README.1st" está instalado en "TARGETDIR PRODUCT" por dos componentes diferentes en un \\ sistema SFN: "Component1" y "Component2". Esto interrumpe el recuento de referencias de componentes.                                                                                           | Component1 y Component2 tienen un archivo denominado "READEME.1st". Cuando se usan nombres de archivo cortos, el instalador instala Dir1 y Dir2 en el mismo directorio, TARGETDIR \\ PRODUCT.<br/> ICE30 genera dos errores, uno para cada archivo. En un entorno de creación que muestra ubicaciones de error, el [](file-table.md)primer error se encuentra en la entrada de un archivo de la tabla de archivos y el segundo en la ubicación del otro archivo.<br/> |
| ERROR: La instalación de un componente condicionalizado haría que el archivo de destino "README.1st" se instalara en "TARGETDIR COMMON TOOLS" por dos componentes diferentes en un sistema \\ LFN: "Component3" y "Component4". Esto interrumpiría el recuento de referencias de componentes.                      | Component4 tiene una entrada en la columna Condición de la [tabla Component y](component-table.md) Component3 no. Si [**VersionNT**](versionnt.md) es True, se instala Component4 y hay una colisión con readme.1st instalado siempre por Component3.<br/> ICE30 genera 4 errores, un par para SFN y otro para LFN.<br/>                                                                                            |
| ADVERTENCIA: El archivo de destino "README.1st" podría instalarse en "TARGETDIR COMMON TOOLS" mediante dos componentes condicionales diferentes en un sistema \\ SFN: "Component4" y "Component5". Si las condiciones no son mutuamente excluyentes, se interrumpirá el sistema de recuento de referencias de componentes. | Dado que Component4 y Component5 tienen entradas en la columna Condición de la [tabla Component,](component-table.md) es posible que no se produzca esta colisión de archivos. ICE30 solo envía una advertencia porque las condiciones deben determinarse en el momento de la instalación.<br/> ICE30 genera 4 advertencias, un par para SFN y otro para LFN.<br/>                                                                                            |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente  | Directorio | Condición |
|------------|-----------|-----------|
| Componente1 | Dir1      |           |
| Componente 2 | Dir2      |           |
| Componente 3 | Dir3      |           |
| Componente 4 | Dir3      | VersionNT |
| Componente5 | Dir3      | Version9X |



 

[Tabla de directorios](directory-table.md)



| Directorio | Directorio \_ primario | DefaultDir                    |
|-----------|-------------------|-------------------------------|
| SOURCEDIR |                   | TARGETDIR                     |
| Dir1      | SOURCEDIR         | Componente \| de producto1 Producto:. |
| Dir2      | SOURCEDIR         | Producto:.                     |
| Dir3      | SOURCEDIR         | Common \| Common Tools:         |



 

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | Componente\_ | FileName   |
|-------|-------------|------------|
| Archivo1 | Componente1  | README.1st |
| Archivo2 | Componente 2  | README.1st |
| File3 | Componente 3  | README.1st |
| File4 | Componente 4  | README.1st |
| File5 | Componente5  | README.1st |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 





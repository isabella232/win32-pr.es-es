---
description: ICE30 valida que la instalación de los componentes que contienen el mismo archivo nunca instala el archivo más de una vez en el mismo directorio.
ms.assetid: 74cb455b-a53e-4c6b-98ff-08cf0858f11f
title: ICE30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78fa96899231015d864e5a0912b8ff73cedbbe75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074631"
---
# <a name="ice30"></a>ICE30

ICE30 valida que la instalación de los componentes que contienen el mismo archivo nunca instala el archivo más de una vez en el mismo directorio.

ICE30 va a todos los componentes de la [tabla Component y,](component-table.md) a continuación, determina el directorio de destino del componente de la [tabla Directory](directory-table.md). A continuación, comprueba qué componentes se instalan en el mismo directorio de destino. Por último, usa la [tabla File para](file-table.md) comprobar que ninguno de los archivos de estos componentes tiene el mismo nombre.

ICE30 comprueba los nombres de archivo largos (LFN) y los nombres de archivo cortos (SFN).

ICE30 no evalúa las propiedades en la resolución de directorios porque estas propiedades pueden cambiar en tiempo de ejecución y modificar el esquema de resolución de directorios. Esto significa que ICE30 puede detectar colisiones de archivos debido a directorios con la misma propiedad en sus rutas de acceso, pero no detecta colisiones resultantes de dos propiedades que tienen el mismo valor.

## <a name="result"></a>Resultado

ICE30 publica un mensaje de error para cada par de componentes que instala el mismo archivo en el mismo directorio.

## <a name="example"></a>Ejemplo

El ejemplo mostrado devuelve dos veces cada uno de los errores siguientes.



| Error o advertencia de ICE30                                                                                                                                                                                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERROR: El archivo de destino "README.1st" se instala en "TARGETDIR PRODUCT" mediante dos componentes diferentes en un sistema \\ SFN: "Component1" y "Component2". Esto interrumpe el recuento de referencias de componentes.                                                                                           | Component1 y Component2 tienen un archivo denominado "READEME.1st". Cuando se usan nombres de archivo cortos, el instalador instala Dir1 y Dir2 en el mismo directorio, TARGETDIR \\ PRODUCT.<br/> ICE30 genera dos errores, uno para cada archivo. En un entorno de creación que muestra las ubicaciones de error, [](file-table.md)el primer error se encuentra en la entrada de un archivo en la tabla de archivos y el segundo en la ubicación del otro archivo.<br/> |
| ERROR: La instalación de un componente condicional haría que el archivo de destino "README.1st" se instalara en "TARGETDIR COMMON TOOLS" por dos componentes diferentes en un sistema \\ LFN: "Component3" y "Component4". Esto interrumpiría el recuento de referencias de componentes.                      | Component4 tiene una entrada en la columna Condición de la [tabla Component](component-table.md) y Component3 no. Si [**VersionNT**](versionnt.md) es True, se instala Component4 y hay una colisión con el archivo Readme.1st siempre instalado por Component3.<br/> ICE30 genera 4 errores, un par para SFN y otro para LFN.<br/>                                                                                            |
| ADVERTENCIA: El archivo de destino "README.1st" podría instalarse en "TARGETDIR COMMON TOOLS" mediante dos componentes condicionales diferentes en un sistema \\ SFN: "Component4" y "Component5". Si las condiciones no son mutuamente excluyentes, se interrumpirá el sistema de recuento de referencias de componentes. | Dado que Component4 y Component5 tienen entradas en la columna Condición de la [tabla Component,](component-table.md) es posible que esta colisión de archivos no se produzca. ICE30 solo envía una advertencia porque las condiciones deben determinarse en el momento de la instalación.<br/> ICE30 genera 4 advertencias, un par para SFN y otro para LFN.<br/>                                                                                            |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente  | Directorio | Condición |
|------------|-----------|-----------|
| Componente1 | Dir1      |           |
| Componente 2 | Dir2      |           |
| Componente 3 | Dir3      |           |
| Componente 4 | Dir3      | VersionNT |
| Componente 5 | Dir3      | Versión9X |



 

[Tabla de directorios](directory-table.md)



| Directorio | Directorio \_ primario | DefaultDir                    |
|-----------|-------------------|-------------------------------|
| SOURCEDIR |                   | TARGETDIR                     |
| Dir1      | SOURCEDIR         | Product \| Component1 Product:. |
| Dir2      | SOURCEDIR         | Producto:.                     |
| Dir3      | SOURCEDIR         | Herramientas \| comunes:         |



 

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | Componente\_ | FileName   |
|-------|-------------|------------|
| Archivo1 | Componente1  | README.1st |
| Archivo2 | Componente 2  | README.1st |
| File3 | Componente 3  | README.1st |
| File4 | Componente 4  | README.1st |
| File5 | Componente 5  | README.1st |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 





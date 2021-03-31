---
description: ICE19 valida que los componentes anunciados hacen referencia a un archivo de la columna de ruta de acceso de la tabla de componentes y que un acceso directo anunciado hace referencia a un directorio de esta columna.
ms.assetid: 438153c1-bc4b-4ecf-ab85-d66ad69c987c
title: ICE19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a53aa3268a1c77f674d4a130c9de02c44b56243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277551"
---
# <a name="ice19"></a>ICE19

ICE19 valida que los componentes anunciados hacen referencia a un archivo de la columna de ruta de acceso de la [tabla de componentes](component-table.md) y que un acceso directo anunciado hace referencia a un directorio de esta columna.

ICE19 valida que los componentes o accesos directos anunciados tienen un ComponentId. Los componentes de la [tabla PublishComponent](publishcomponent-table.md), que no se anuncian en otra tabla, solo se comprueban para ver si tienen un ComponentID.

## <a name="result"></a>Resultado

ICE19 envía un mensaje de error si la columna de ruta de acceso de la tabla de componentes no hace referencia a un archivo en el caso de un componente anunciado o un directorio en el caso de un acceso directo anunciado. ICE19 envía un mensaje de error si alguno de los componentes o accesos directos anunciados no tiene un ComponentId.

## <a name="example"></a>Ejemplo

ICE19 expone los siguientes mensajes de error para el ejemplo mostrado:

-   La extensión FLP hace referencia al componente Comp1, que no tiene especificado un ComponentId en la [tabla de componentes](component-table.md).
-   La extensión exe hace referencia al componente Comp4, que hace referencia a un directorio como su ruta de rutas. La ruta de la ruta de la tabla de componentes es NULL.
-   Shortcut Shortcut2 hace referencia al componente Comp3, que hace referencia a una entrada del registro como la ruta de acceso de la clave. El valor de la columna Attributes de la tabla de componentes es 4.

[Tabla de componentes](component-table.md) (parcial)



| Componente | ComponentId                            | Atributos | Rutas |
|-----------|----------------------------------------|------------|---------|
| Comp1     | Null                                   | 0          | Archivo1   |
| Comp2     | {00000002-0003-0000-0000-624474736554} | 0          | Archivo2   |
| Comp3     | {00000003-0003-0000-0000-624474736554} | 4          | Reg3    |
| Comp4     | {00000004-0003-0000-0000-624474736554} | 0          | Null    |



 

[Tabla de extensión](extension-table.md) (parcial)



| Extensión | Componente\_ |
|-----------|-------------|
| FLP       | Comp1       |
| TST       | Comp2       |
| exe       | Comp4       |



 

[Tabla de acceso directo](shortcut-table.md) (parcial)



| Acceso directo  | Componente\_ | Característica\_      |
|-----------|-------------|----------------|
| Shortcut1 | Comp4       | ProductFeature |
| Shortcut2 | Comp3       | ProductFeature |



 

[Tabla de características](feature-table.md) (parcial)



| Característica        |
|----------------|
| ProductFeature |



 

> [!Note]  
> Si la extensión FLP y exe hacen referencia al mismo componente, el servidor EXE o COM que los abre deben ser el mismo. Este archivo EXE suele ser la ruta de la ruta de archivo del componente. En el caso de OFFICE, las extensiones doc y XLS no pueden hacer referencia al mismo componente porque el mismo EXE no abre ambas extensiones. Necesita winword.exe para abrir las extensiones de documento y necesita excel.exe para abrir las extensiones xls.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




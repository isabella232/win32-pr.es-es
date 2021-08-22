---
description: ICE19 valida que los componentes anunciados hacen referencia a un archivo de la columna KeyPath de la tabla Component y que un acceso directo anunciado hace referencia a un directorio de esta columna.
ms.assetid: 438153c1-bc4b-4ecf-ab85-d66ad69c987c
title: ICE19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1a706999744762a930a800326cb8d38487f19c1c4ea3e01b6b1f8aeae4ca2dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529115"
---
# <a name="ice19"></a>ICE19

ICE19 valida que los componentes anunciados hacen referencia a un archivo de la columna KeyPath de la tabla [Component](component-table.md) y que un acceso directo anunciado hace referencia a un directorio de esta columna.

ICE19 valida que los componentes o accesos directos anunciados tienen un ComponentId. Los componentes de [la tabla PublishComponent](publishcomponent-table.md), que no se anuncian en otra tabla, solo se comprueban para ver si tienen un ComponentId.

## <a name="result"></a>Resultado

ICE19 envía un mensaje de error si la columna KeyPath de la tabla Component no hace referencia a un archivo en el caso de un componente anunciado o un directorio en el caso de un acceso directo anunciado. ICE19 envía un mensaje de error si los componentes o accesos directos anunciados no tienen un ComponentId.

## <a name="example"></a>Ejemplo

ICE19 publica los siguientes mensajes de error para el ejemplo que se muestra:

-   La extensión flp hace referencia al componente Comp1 que no tiene un ComponentId especificado en la [tabla Component](component-table.md).
-   El archivo exe de extensión hace referencia al componente Comp4, que hace referencia a un directorio como KeyPath. KeyPath es NULL en la tabla Component.
-   Acceso directo2 hace referencia al componente Comp3, que hace referencia a una entrada del Registro como ruta de acceso de clave. El valor de la columna Attributes de la tabla Component es 4.

[Tabla de componentes](component-table.md) (parcial)



| Componente | Componentid                            | Atributos | KeyPath |
|-----------|----------------------------------------|------------|---------|
| Comp1     | Null                                   | 0          | Archivo1   |
| Comp2     | {00000002-0003-0000-0000-624474736554} | 0          | Archivo2   |
| Comp3     | {00000003-0003-0000-0000-624474736554} | 4          | Reg3    |
| Comp4     | {00000004-0003-0000-0000-624474736554} | 0          | Null    |



 

[Tabla de extensiones](extension-table.md) (parcial)



| Extensión | Componente\_ |
|-----------|-------------|
| Flp       | Comp1       |
| Tst       | Comp2       |
| exe       | Comp4       |



 

[Tabla de métodos abreviados](shortcut-table.md) (parcial)



| Acceso directo  | Componente\_ | Característica\_      |
|-----------|-------------|----------------|
| Acceso directo1 | Comp4       | ProductFeature |
| Acceso directo2 | Comp3       | ProductFeature |



 

[Tabla de características](feature-table.md) (parcial)



| Característica        |
|----------------|
| ProductFeature |



 

> [!Note]  
> Si la extensión flp y exe hacen referencia al mismo componente, el servidor EXE o COM que los abre debe ser el mismo. Este EXE suele ser keyPath para el componente. Para OFFICE, el documento de extensiones y xls no pueden hacer referencia al mismo componente porque el mismo EXE no abre ambas extensiones. Necesita winword.exe para abrir extensiones de documento y necesita excel.exe para abrir extensiones xls.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




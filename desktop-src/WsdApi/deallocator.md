---
description: Especifica el tipo de desasignador que va a usar una función de código auxiliar.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: deallocator, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 692ed2e57b3e649c0ee7af171f205c949496f9b4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994942"
---
# <a name="deallocator-element"></a>elemento deallocator

Especifica el tipo de desasignador que va a usar una función de código auxiliar.

## <a name="usage"></a>Uso

``` syntax
<deallocator/>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                               | Descripción                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**stubDefinitions**](stubdefinitions.md)<br/> | Genera implementaciones para funciones de código auxiliar para operaciones de tipo de puerto.<br/> <br/> |



## <a name="remarks"></a>Comentarios

El tipo de desasignador debe incluirse en un par de <deallocator></deallocator> etiquetas. Las cadenas siguientes son valores de desasignador válidos:

-   ninguno
-   WSDFreeLinkedMemory
-   CoTaskMemFree
-   libre
-   delete
-   deleteArray
-   Release

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 





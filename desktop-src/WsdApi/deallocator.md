---
description: Especifica el tipo de desasignador que va a usar una función de código auxiliar.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: deallocator, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e9a27f768d0c9d854d13bd58c0c797234a0526c4abb95a0c5f4fb553466a6ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991755"
---
# <a name="deallocator-element"></a>deallocator, elemento

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
| [**stubDefinitions**](stubdefinitions.md)<br/> | Genera implementaciones para las funciones de código auxiliar para las operaciones de tipo de puerto.<br/> <br/> |



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



| Etiqueta | Valor |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 





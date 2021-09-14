---
description: Especifica el tipo de desasignador que va a usar una función de código auxiliar.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: deallocator, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2617ce92dcd0c2763f77b0bc6f0fb5c1beea1c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358930"
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



## <a name="remarks"></a>Observaciones

El tipo deallocator debe incluirse en un par de etiquetas &lt; de desasignador. &gt; </deallocator> Las cadenas siguientes son valores de desasignador válidos:

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



 

 





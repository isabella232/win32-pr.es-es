---
description: Especifica el desasignador de tipos que va a usar una función de código auxiliar de operaciones.
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: operationDeallocator, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ce2902bbfac16cb096da334cf3f22a12c68e3720d575fa303b8f3b133c9328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991695"
---
# <a name="operationdeallocator-element"></a>operationDeallocator, elemento

Especifica el desasignador de tipos que va a usar la función de código auxiliar de una operación.

## <a name="usage"></a>Uso

``` syntax
<operationDeallocator
  operation = "character_string"
  deallocator = "character_string"/>
```

## <a name="attributes"></a>Atributos



| Atributo                  | Tipo                         | Requerido       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------|------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **deallocator**<br/> | cadena \_ de caracteres<br/> | Sí<br/> | Desasignador que se usará para la operación.<br/> <br/> Las cadenas siguientes son valores válidos.<br/> <br/> <dl><span id="none"></span><span id="NONE"></span><dt>**none**</dt> <span id="WSDFreeLinkedMemory"></span> <span id="wsdfreelinkedmemory"></span> <span id="WSDFREELINKEDMEMORY"></span> <dt>**WSDFreeLinkedMemory***</dt> <span id="CoTaskMemFree"></span> <span id="cotaskmemfree"></span> <span id="COTASKMEMFREE"></span> <dt>*:CoTaskMemFree***</dt> <span id="free"></span> <span id="FREE"></span> <dt>***free***</dt> <span id="delete"></span> <span id="DELETE"></span> <dt>**delete***</dt> <span id="deleteArray"></span> <span id="deletearray"></span> <span id="DELETEARRAY"></span> <dt>***deleteArray***</dt> <span id="Release"></span> <span id="release"></span> <span id="RELEASE"></span> <dt>***Versión***</dt> </dl> |
| **operation**<br/>   | cadena \_ de caracteres<br/> | Sí<br/> | Nombre de la operación.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                               | Descripción                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**stubDefinitions**](stubdefinitions.md)<br/> | Genera implementaciones para las funciones de código auxiliar para las operaciones de tipo de puerto.<br/> <br/> |



## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 





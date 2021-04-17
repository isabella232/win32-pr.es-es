---
description: Especifica el tipo desasignador que va a usar una función de código auxiliar de operaciones.
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: elemento operationDeallocator
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c214b5dbc3245f63797c55880fe052d5c3ced15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697219"
---
# <a name="operationdeallocator-element"></a>elemento operationDeallocator

Especifica el tipo desasignador que va a usar la función de código auxiliar de una operación.

## <a name="usage"></a>Uso

``` syntax
<operationDeallocator
  operation = "character_string"
  deallocator = "character_string"/>
```

## <a name="attributes"></a>Atributos



| Atributo                  | Tipo                         | Obligatorio       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------|------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **desasignador**<br/> | cadena de caracteres \_<br/> | Sí<br/> | Desasignador que se va a usar para la operación.<br/> <br/> Las cadenas siguientes son valores válidos.<br/> <br/> <dl><span id="none"></span><span id="NONE"></span><dt>* * * * ninguno * *</dt> <span id="WSDFreeLinkedMemory"></span> <span id="wsdfreelinkedmemory"></span> <span id="WSDFREELINKEDMEMORY"></span> * * * * * * <dt>WSDFreeLinkedMemory * *</dt> <span id="CoTaskMemFree"></span> <span id="cotaskmemfree"></span> <span id="COTASKMEMFREE"></span> * * * <dt>* * * * CoTaskMemFree * *</dt> <span id="free"></span> <span id="FREE"></span> * * <dt>* * * * gratis * *</dt> <span id="delete"></span> <span id="DELETE"></span> * * <dt>* * * * eliminar * *</dt> <span id="deleteArray"></span> <span id="deletearray"></span> <span id="DELETEARRAY"></span> * * * * * * <dt>deleteArray * *</dt> <span id="Release"></span> <span id="release"></span> <span id="RELEASE"></span> * * * * * * * <dt>Versión * *</dt> * * </dl> |
| **operation**<br/>   | cadena de caracteres \_<br/> | Sí<br/> | Nombre de la operación.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                               | Descripción                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**stubDefinitions**](stubdefinitions.md)<br/> | Genera implementaciones para las funciones de código auxiliar para las operaciones de tipo de puerto.<br/> <br/> |



## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 





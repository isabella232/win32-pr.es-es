---
description: La plantilla de clase CGenericList que implementa una lista específica del tipo. Para obtener más información, vea CBaseList.
ms.assetid: 69067530-3a7d-4731-8ac6-9d02dbba8440
title: Clase CGenericList (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6de3a2dde8d4549221ef4f13decab167fcf6d560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660833"
---
# <a name="cgenericlist-class"></a>Clase CGenericList

![jerarquía de clases cgenericlist](images/list01.png)

La `CGenericList` plantilla de clase que implementa una lista específica del tipo. Para obtener más información, vea [**CBaseList**](cbaselist.md).

Para usar esta plantilla, declare una variable de tipo `CGenericList` con un argumento de plantilla que defina el tipo de objeto de la lista. Por ejemplo, la siguiente instrucción declara una lista de objetos [**CBaseFilter**](cbasefilter.md) :


```
CGenericList<CBaseFilter> myFilterList("Filters"); 
```



Por comodidad, Wxlist. h define los siguientes tipos de lista:

``` syntax
typedef CGenericList<CBaseObject> CBaseObjectList;
typedef CGenericList<IUnknown> CBaseInterfaceList;
```



| Métodos públicos                                          | Descripción                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [**CGenericList**](cgenericlist-cgenericlist.md)       | Método de constructor.                                                      |
| [**~ CGenericList**](cgenericlist--cgenericlist.md)     | Método de destructor.                                                       |
| [**GetHeadPosition**](cgenericlist-getheadposition.md) | Recupera la posición del primer elemento de la lista.                    |
| [**GetTailPosition**](cgenericlist-gettailposition.md) | Recupera la posición del último elemento de la lista.                     |
| [**GetCount**](cgenericlist-getcount.md)               | Recupera el número de elementos de la lista.                               |
| [**GetNext**](cgenericlist-getnext.md)                 | Recupera el elemento en la posición especificada y hace avanzar la posición. |
| [**Obtener**](cgenericlist-get.md)                         | Recupera el elemento en la posición especificada.                            |
| [**GetHead**](cgenericlist-gethead.md)                 | Recupera el elemento situado en el encabezado de la lista.                              |
| [**RemoveHead**](cgenericlist-removehead.md)           | Quita el primer elemento de la lista.                                      |
| [**RemoveTail**](cgenericlist-removetail.md)           | Quita el último elemento de la lista.                                       |
| [**Retirar**](cgenericlist-remove.md)                   | Quita el elemento de en la posición especificada.                              |
| [**AddBefore**](cgenericlist-addbefore.md)             | Inserta un elemento o una lista antes de la posición especificada.                   |
| [**AddAfter**](cgenericlist-addafter.md)               | Inserta un elemento o una lista después de la posición especificada.                    |
| [**AddHead**](cgenericlist-addhead.md)                 | Agrega un elemento o una lista al principio de la lista.                           |
| [**Addtail (**](cgenericlist-addtail.md)                 | Anexa un elemento o una lista al final de la lista.                          |
| [**Buscar**](cgenericlist-find.md)                       | Recupera la primera posición que contiene el elemento especificado.              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 





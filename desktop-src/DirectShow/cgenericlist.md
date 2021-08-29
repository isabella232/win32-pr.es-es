---
description: Plantilla de clase CGenericList que implementa una lista específica del tipo. Para obtener más información, vea CBaseList.
ms.assetid: 69067530-3a7d-4731-8ac6-9d02dbba8440
title: CGenericList (clase, Wxlist.h)
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
ms.openlocfilehash: 79bbc003770d7fec94af93a54386bccbfbd00c4cd2a8b3f9a8ff81e14aa7a6ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999425"
---
# <a name="cgenericlist-class"></a>CGenericList (clase)

![jerarquía de clases cgenericlist](images/list01.png)

Plantilla `CGenericList` de clase que implementa una lista específica del tipo. Para obtener más información, vea [**CBaseList**](cbaselist.md).

Para usar esta plantilla, declare una variable de tipo `CGenericList` con un argumento de plantilla que defina el tipo de objeto en la lista. Por ejemplo, la siguiente instrucción declara una lista de [**objetos CBaseFilter:**](cbasefilter.md)


```
CGenericList<CBaseFilter> myFilterList("Filters"); 
```



Para mayor comodidad, Wxlist.h define los siguientes tipos de lista:

``` syntax
typedef CGenericList<CBaseObject> CBaseObjectList;
typedef CGenericList<IUnknown> CBaseInterfaceList;
```



| Métodos públicos                                          | Descripción                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [**CGenericList**](cgenericlist-cgenericlist.md)       | Método constructor.                                                      |
| [**~CGenericList**](cgenericlist--cgenericlist.md)     | Método destructor.                                                       |
| [**GetHeadPosition**](cgenericlist-getheadposition.md) | Recupera la posición del primer elemento de la lista.                    |
| [**GetTailPosition**](cgenericlist-gettailposition.md) | Recupera la posición del último elemento de la lista.                     |
| [**GetCount**](cgenericlist-getcount.md)               | Recupera el número de elementos de la lista.                               |
| [**GetNext**](cgenericlist-getnext.md)                 | Recupera el elemento en la posición especificada y avanza la posición. |
| [**Obtener**](cgenericlist-get.md)                         | Recupera el elemento en la posición especificada.                            |
| [**GetHead**](cgenericlist-gethead.md)                 | Recupera el elemento en la parte principal de la lista.                              |
| [**RemoveHead**](cgenericlist-removehead.md)           | Quita el primer elemento de la lista.                                      |
| [**RemoveTail**](cgenericlist-removetail.md)           | Quita el último elemento de la lista.                                       |
| [**Quitar**](cgenericlist-remove.md)                   | Quita el elemento de en la posición especificada.                              |
| [**AddBefore**](cgenericlist-addbefore.md)             | Inserta un elemento o una lista antes de la posición especificada.                   |
| [**AddAfter**](cgenericlist-addafter.md)               | Inserta un elemento o una lista después de la posición especificada.                    |
| [**AddHead**](cgenericlist-addhead.md)                 | Agrega un elemento o una lista al frente de la lista.                           |
| [**AddTail**](cgenericlist-addtail.md)                 | Anexa un elemento o una lista al final de la lista.                          |
| [**Buscar**](cgenericlist-find.md)                       | Recupera la primera posición que contiene el elemento especificado.              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 





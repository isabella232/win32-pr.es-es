---
description: El método CBaseList implementa una lista de abstracciones. La plantilla de clase CGenericList, que se deriva de CBaseList, proporciona comprobación de tipos y una interfaz más sencilla que la clase CBaseList.
ms.assetid: 372ee6f7-be0c-469f-92b3-673970ebd6da
title: CBaseList (clase, Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6aa4a3c80cd583bd3cc83a2a0adedecb6caaf7c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361388"
---
# <a name="cbaselist-class"></a>CBaseList (clase)

![jerarquía de clases cbaselist](images/list01.png)

El **método CBaseList** implementa una lista de abstracciones. La [**plantilla de clase CGenericList,**](cgenericlist.md) que se deriva de **CBaseList,** proporciona comprobación de tipos y una interfaz más sencilla que la **clase CBaseList.**

La **clase CBaseList** se modela después de la **clase CObList** en la biblioteca Microsoft Foundation Classes (MFC). Las posiciones dentro de la lista se representan mediante una estructura POSITION. El autor de la llamada no debe tener acceso a los miembros internos de la estructura POSITION; tratarlo como un puntero a un nodo de lista. La posición de un objeto en la lista sigue siendo válida hasta que se elimina el objeto.

La lista no requiere ninguna compatibilidad con los objetos que contiene. No realiza ninguna administración de almacenamiento ni copia en los objetos. Los objetos pueden estar en varias listas.

Aproximadamente la mitad de los métodos de esta clase actúan sobre objetos individuales. Estos métodos tienen el sufijo : I en el nombre del método. Los otros métodos actúan en listas enteras. Por ejemplo, el [**método CBaseList::AddAfter**](cbaselist-addafter.md) anexa una lista a otra lista. Las operaciones de objeto único devuelven valores POSITION o **NULL en** caso de error. Las operaciones de lista **devuelven TRUE si** se realiza **correctamente o FALSE** en caso contrario.



| Variables de miembro protegido                             | Descripción                                                               |
|--------------------------------------------------------|---------------------------------------------------------------------------|
| [**m \_ Count**](cbaselist-m-count.md)                  | Número de elementos de la lista.                                              |
| [**m \_ pFirst**](cbaselist-m-pfirst.md)                | Puntero al primer nodo de la lista.                                    |
| [**m \_ pLast**](cbaselist-m-plast.md)                  | Puntero al último nodo de la lista.                                     |
| Métodos protegidos                                      | Descripción                                                               |
| [**GetNextI**](cbaselist-getnexti.md)                 | Recupera el elemento en la posición especificada y avanza la posición.  |
| [**GetI**](cbaselist-geti.md)                         | Recupera el elemento en la posición especificada.                             |
| [**FindI**](cbaselist-findi.md)                       | Recupera la primera posición que contiene el elemento especificado.               |
| [**RemoveHeadI**](cbaselist-removeheadi.md)           | Quita el primer elemento de la lista.                                       |
| [**RemoveTailI**](cbaselist-removetaili.md)           | Quita el último elemento de la lista.                                        |
| [**RemoveI**](cbaselist-removei.md)                   | Quita el elemento de en la posición especificada.                               |
| [**AddTailI**](cbaselist-addtaili.md)                 | Agrega un elemento al final de la lista.                                      |
| [**AddHeadI**](cbaselist-addheadi.md)                 | Agrega un elemento al frente de la lista.                                    |
| [**AddAfterI**](cbaselist-addafteri.md)               | Inserta un elemento después de la posición especificada.                             |
| [**AddBeforeI**](cbaselist-addbeforei.md)             | Inserta un elemento antes de la posición especificada.                            |
| Métodos públicos                                         | Descripción                                                               |
| [**CBaseList**](cbaselist-cbaselist.md)               | Método constructor.                                                       |
| [**~ CBaseList**](cbaselist--cbaselist.md)            | Método destructor.                                                        |
| [**Removeall**](cbaselist-removeall.md)               | Quita todos los nodos de la lista.                                          |
| [**GetHeadPositionI**](cbaselist-getheadpositioni.md) | Recupera la posición del primer elemento de la lista.                     |
| [**GetTailPositionI**](cbaselist-gettailpositioni.md) | Recupera la posición del último elemento de la lista.                      |
| [**GetCountI**](cbaselist-getcounti.md)               | Recupera el número de elementos de la lista.                                |
| [**Next**](cbaselist-next.md)                         | Recupera la siguiente posición de la lista.                                  |
| [**Prev**](cbaselist-prev.md)                         | Recupera la posición anterior en la lista.                              |
| [**AddHead**](cbaselist-addhead.md)                   | Inserta otra lista al frente de esta lista.                           |
| [**AddTail**](cbaselist-addtail.md)                   | Anexa otra lista al final de esta lista.                             |
| [**AddAfter**](cbaselist-addafter.md)                 | Inserta una lista después de la posición especificada.                              |
| [**AddBefore**](cbaselist-addbefore.md)               | Inserta una lista antes de la posición especificada.                             |
| [**MoveToTail**](cbaselist-movetotail.md)             | Divide la lista y anexa la parte principal al final de otra lista. |
| [**MoveToHead**](cbaselist-movetohead.md)             | Divide la lista e inserta la parte final en la parte superior de otra lista. |
| [**Marcha atrás**](cbaselist-reverse.md)                   | Invierte el orden de la lista.                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[DirectShow Clases base](directshow-base-classes.md)
</dt> </dl>

 

 





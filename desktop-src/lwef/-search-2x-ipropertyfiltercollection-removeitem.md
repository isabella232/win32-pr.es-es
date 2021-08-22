---
title: Propiedad RemoveItem de IPropertyFilterCollection (WdsSharedIDL.h)
description: Quita un filtro específico de la colección.
ms.assetid: a8b8a1f7-d47a-45dc-81c9-f01ecf6c1560
keywords:
- Características heredadas del entorno de Windows removeItem
- Propiedades Legacy Windows Environment Features , IPropertyFilterCollection (interfaz IPropertyFilterCollection)
- IPropertyFilterCollection interface Legacy Windows Environment Features , RemoveItem property
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.RemoveItem
- IPropertyFilterCollection.put_RemoveItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54822e95e2ea7d6e10fdd5bbf833adb63b51cb01e8d860ce77f550432b41e926
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755424"
---
# <a name="ipropertyfiltercollectionremoveitem-property"></a>Propiedad IPropertyFilterCollection::RemoveItem

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la API [Windows Search en](../search/-search-reference-entry-page.md) su lugar. 

Quita un filtro específico de la colección.

Esta propiedad es de solo escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RemoveItem(
  [in] long index
);
```



## <a name="property-value"></a>Valor de propiedad

Acepta un puntero al índice para el filtro que se va a quitar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio sp1 \[\]<br/>                             |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 






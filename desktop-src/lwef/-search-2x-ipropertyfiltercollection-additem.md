---
title: Propiedad IPropertyFilterCollection AddItem (WdsSharedIDL. h)
description: Agrega un nuevo filtro a la colección.
ms.assetid: 01078e7a-811a-4dfb-b122-4801f39413d8
keywords:
- Propiedad AddItem características de entorno de Windows heredadas
- Propiedad AddItem características de entorno de Windows heredadas, interfaz IPropertyFilterCollection
- Interfaz IPropertyFilterCollection características del entorno heredado de Windows, propiedad AddItem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.AddItem
- IPropertyFilterCollection.get_AddItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b199f0e696f75fb5549b274ac888989f7a723b48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079228"
---
# <a name="ipropertyfiltercollectionadditem-property"></a>IPropertyFilterCollection:: AddItem (propiedad)

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar. 

Agrega un nuevo filtro a la colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_AddItem(
  [out, retval] IPropertyFilter **filter
);
```



## <a name="property-value"></a>Valor de propiedad

Devuelve un puntero a la dirección para el nuevo filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]<br/>                             |
| Redistribuible<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Encabezado<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 






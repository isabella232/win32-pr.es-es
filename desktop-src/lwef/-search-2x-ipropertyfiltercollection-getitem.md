---
title: Propiedad GetITem de IPropertyFilterCollection (WdsSharedIDL. h)
description: Devuelve un filtro específico dentro de la colección.
ms.assetid: 72a35d98-b2d8-4dfb-84a7-365a3778fc85
keywords:
- Propiedad GetITem características de entorno de Windows heredado
- Propiedad GetITem características de entorno heredado de Windows, interfaz IPropertyFilterCollection
- Interfaz IPropertyFilterCollection características del entorno heredado de Windows, propiedad GetITem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.GetITem
- IPropertyFilterCollection.get_GetITem
- IPropertyFilterCollection.put_GetITem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8027bf175efc615c1324f55229c7e307a123c39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996241"
---
# <a name="ipropertyfiltercollectiongetitem-property"></a>IPropertyFilterCollection:: GetITem (propiedad)

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar. 

Devuelve un filtro específico dentro de la colección.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_GetITem(
  [in]          long            index
);

HRESULT get_GetITem(
  [out, retval] IPropertyFilter **filter
);
```



## <a name="property-value"></a>Valor de propiedad

Establece la dirección del filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]<br/>                             |
| Redistribuible<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Encabezado<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 






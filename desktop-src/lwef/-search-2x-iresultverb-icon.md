---
title: Propiedad Icono IResultVerb (WdsSharedIDL.h)
description: Esta propiedad devuelve un puntero para controlar el icono opcional asociado al verbo .
ms.assetid: 19de0e36-b453-48a4-8ac0-f26432e088ae
keywords:
- Propiedad icon Legacy Windows Environment Features
- Propiedad icon Legacy Windows Environment Features , IResultVerb (Interfaz IResultVerb)
- IResultVerb interface Legacy Windows Environment Features , Propiedad Icon
topic_type:
- apiref
api_name:
- IResultVerb.Icon
- IResultVerb.get_Icon
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef3715aacb0fd2f4bb0f47424d239e3d4b9717d83471906de8d1b2637fab472a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117694733"
---
# <a name="iresultverbicon-property"></a>IResultVerb::Icon, propiedad

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API Windows Search en](../search/-search-reference-entry-page.md) su lugar. 

Esta propiedad devuelve un puntero para controlar el icono opcional asociado al verbo .

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Icon(
  [out, retval] SHANDLE_PTR *hicon
);
```



## <a name="property-value"></a>Valor de propiedad

hicon es un puntero al identificador del icono opcional asociado con el verbo .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio de SP1 \[\]<br/>                             |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 






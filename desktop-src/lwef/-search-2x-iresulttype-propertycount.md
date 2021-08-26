---
title: Propiedad IResultType PropertyCount (WdsSharedIDL.h)
description: Esta propiedad contiene el número de propiedades expuestas por el tipo .
ms.assetid: 4ca4b18c-d228-4275-b00d-06c6f227e0ae
keywords:
- Propiedades de PropertyCount características heredadas Windows entorno
- Propiedad PropertyCount Heredada de Windows Environment Features , IResultType (interfaz)
- IResultType interface Legacy Windows Environment Features , PropertyCount property
topic_type:
- apiref
api_name:
- IResultType.PropertyCount
- IResultType.get_PropertyCount
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6952f2efb6e0d14be22daf71e352747915b2ba05bf543d764ee9af5f496715ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014635"
---
# <a name="iresulttypepropertycount-property"></a>Propiedad IResultType::P ropertyCount

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la API [Windows Search en](../search/-search-reference-entry-page.md) su lugar. 

Esta propiedad contiene el número de propiedades expuestas por el tipo .

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_PropertyCount(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Valor de propiedad

devuelve la dirección del número de propiedades expuestas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio sp1 \[\]<br/>                             |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 






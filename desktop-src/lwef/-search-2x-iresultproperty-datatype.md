---
title: Propiedad DataType de IResultProperty (WdsSharedIDL.h)
description: Tipo de datos properties.
ms.assetid: 2bf83256-0d69-48f2-aa7d-d34dcba17050
keywords:
- Características heredadas del entorno de Windows datatype
- Propiedad DataType Legacy Windows Environment Features , IResultProperty (interfaz)
- IResultProperty interface Legacy Windows Environment Features , DataType property
topic_type:
- apiref
api_name:
- IResultProperty.DataType
- IResultProperty.get_DataType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f669fdbb01459e99edb0ccc9ba75fed1cbd60ebfe789fdb4393d217239cdc1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755264"
---
# <a name="iresultpropertydatatype-property"></a>Propiedad IResultProperty::D ataType

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API Windows Search en](../search/-search-reference-entry-page.md) su lugar. 

Tipo de datos properties.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DataType(
  [out, retval] VARTYPE *vt
);
```



## <a name="property-value"></a>Valor de propiedad

devuelve un puntero al tipo de datos properties.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio de SP1 \[\]<br/>                             |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 






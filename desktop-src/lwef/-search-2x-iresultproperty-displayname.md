---
title: Propiedad IResultProperty DisplayName (WdsSharedIDL. h)
description: Nombre para mostrar localizado de la propiedad.
ms.assetid: 8f9e118a-9e92-4919-afe1-735c61af38f7
keywords:
- Propiedad DisplayName características de entorno de Windows heredadas
- Propiedad DisplayName características de entorno de Windows heredadas, interfaz IResultProperty
- Interfaz IResultProperty características del entorno heredado de Windows, propiedad DisplayName
topic_type:
- apiref
api_name:
- IResultProperty.DisplayName
- IResultProperty.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f36aa934d2ddf31d841478cef1cb9a33b0531224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150577"
---
# <a name="iresultpropertydisplayname-property"></a>IResultProperty::D propiedad isplayName

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar. 

Nombre para mostrar localizado de la propiedad.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Valor de propiedad

Devuelve un puntero al nombre para mostrar localizado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]<br/>                             |
| Redistribuible<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Encabezado<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 






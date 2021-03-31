---
title: Propiedad IResultVerb DisplayName (WdsSharedIDL. h)
description: Esta propiedad devuelve un puntero al nombre para mostrar localizado del verbo.
ms.assetid: f1f4a30e-ecfb-4091-b9cd-312e427d0eb4
keywords:
- Propiedad DisplayName características de entorno de Windows heredadas
- Propiedad DisplayName características de entorno de Windows heredadas, interfaz IResultVerb
- Interfaz IResultVerb características del entorno heredado de Windows, propiedad DisplayName
topic_type:
- apiref
api_name:
- IResultVerb.DisplayName
- IResultVerb.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721831274fc87ee65c8ee1655fdb7b38f80e1114
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079225"
---
# <a name="iresultverbdisplayname-property"></a>IResultVerb::D propiedad isplayName

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar. 

Esta propiedad devuelve un puntero al nombre para mostrar localizado del verbo.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *Verb
);
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad devuelve un puntero al nombre para mostrar localizado del verbo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]<br/>                             |
| Redistribuible<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Encabezado<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 






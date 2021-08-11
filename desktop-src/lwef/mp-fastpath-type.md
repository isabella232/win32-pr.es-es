---
title: MP_FASTPATH_TYPE enumeración (MpClient.h)
description: Tipo FastPath.
ms.assetid: BD72228F-DCC0-435E-A408-BD7FB02E55E1
keywords:
- MP_FASTPATH_TYPE enumeración heredada de Windows environment
- PMP_FASTPATH_TYPE puntero de enumeración heredados Windows environment
topic_type:
- apiref
api_name:
- MP_FASTPATH_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7bd9a8ce26f930a35c9c4fa547234b0d55b0b588b60881cf8aae31621e9a83a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247450"
---
# <a name="mp_fastpath_type-enumeration"></a>Enumeración \_ MP FASTPATH \_ TYPE

Tipo FastPath.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMP_FASTPATH_TYPE { 
  MP_FASTPATH_UNKNOWN   = 0,
  MP_FASTPATH_VDM       = 1,
  MP_FASTPATH_DISABLED  = 2
} MP_FASTPATH_TYPE, *PMP_FASTPATH_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MP_FASTPATH_UNKNOWN"></span><span id="mp_fastpath_unknown"></span>**MP \_ FASTPATH \_ UNKNOWN**
</dt> <dd>

Desconocido.

</dd> <dt>

<span id="MP_FASTPATH_VDM"></span><span id="mp_fastpath_vdm"></span>**MP \_ FASTPATH \_ VDM**
</dt> <dd>

Actualización de VDM.

</dd> <dt>

<span id="MP_FASTPATH_DISABLED"></span><span id="mp_fastpath_disabled"></span>**MP \_ FASTPATH \_ DESHABILITADO**
</dt> <dd>

Notificación de deshabilitación de firma.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 






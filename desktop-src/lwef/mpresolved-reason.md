---
title: MPRESOLVED_REASON enumeración (MpClient.h)
description: Posibles motivos para resolver un error de corrección.
ms.assetid: 29E875D7-97DA-4129-AB71-B261CD0E682A
keywords:
- MPRESOLVED_REASON enumeración de características heredadas Windows entorno
- PMPRESOLVED_REASON puntero de enumeración Heredados Windows Environment Features
topic_type:
- apiref
api_name:
- MPRESOLVED_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a365ef55d9fe2d76e619f3c772cc1df2e6c5e1c8c33721f24dc844d064b33398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975985"
---
# <a name="mpresolved_reason-enumeration"></a>Enumeración MPRESOLVED \_ REASON

Posibles motivos para resolver un error de corrección.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPRESOLVED_REASON { 
  MPRESOLVED_REASON_UNKNOWN    = 0,
  MPRESOLVED_REASON_FULL_SCAN  = 1,
  MPRESOLVED_REASON_TIMED_OUT  = 2
} MPRESOLVED_REASON, *PMPRESOLVED_REASON;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MPRESOLVED_REASON_UNKNOWN"></span><span id="mpresolved_reason_unknown"></span>**MOTIVO MPRESOLVED \_ \_ DESCONOCIDO**
</dt> <dd>

En estado de error.

</dd> <dt>

<span id="MPRESOLVED_REASON_FULL_SCAN"></span><span id="mpresolved_reason_full_scan"></span>**EXAMEN COMPLETO DE LA \_ RAZÓN \_ DE MPRESOLVED \_**
</dt> <dd>

Se realizó un examen completo.

</dd> <dt>

<span id="MPRESOLVED_REASON_TIMED_OUT"></span><span id="mpresolved_reason_timed_out"></span>**SE HA RESUELTO \_ EL TIEMPO DE ESPERA DE LA \_ RAZÓN DE MPRESOLVED \_**
</dt> <dd>

Ha pasado suficiente tiempo. El valor predeterminado es una semana.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 






---
title: WINBIO_ANTI_SPOOF_POLICY_ACTION enumeración (Winbio \_ types.h)
description: Especifica los tipos de acciones que se llevan a cabo para la directiva de antispoofing de un usuario.
ms.assetid: 846C0725-1796-49E4-883C-44AC7D618317
keywords:
- WINBIO_ANTI_SPOOF_POLICY_ACTION enumeración Windows BIOMETRIC Framework API
- PWINBIO_ANTI_SPOOF_POLICY puntero de enumeración Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY_ACTION
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65fec198a0784bf076eb90224318bd36a88ba3ed96258ffd2014a27da5c8f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911283"
---
# <a name="winbio_anti_spoof_policy_action-enumeration"></a>Enumeración \_ WINBIO ANTI \_ SPOOF \_ POLICY \_ ACTION

Especifica los tipos de acciones que se llevan a cabo para la directiva de antispoofing de un usuario.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _WINBIO_ANTI_SPOOF_POLICY_ACTION { 
  WINBIO_ANTI_SPOOF_DISABLE  = 0x00000000,
  WINBIO_ANTI_SPOOF_ENABLE   = 0x00000001,
  WINBIO_ANTI_SPOOF_REMOVE   = 0x00000002
} WINBIO_ANTI_SPOOF_POLICY_ACTION, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**WINBIO \_ ANTI \_ SPOOF \_ DISABLE**
</dt> <dd>

Desactiva la detección de suplantación de seguridad para un factor biométrico.

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**WINBIO \_ ANTI \_ SPOOF \_ ENABLE**
</dt> <dd>

Activa la detección de suplantación de seguridad para un factor biométrico.

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**QUITAR \_ ANTI \_ SUPLANTACIÓN DE \_ WINBIO**
</dt> <dd>

Quita de la cuenta la directiva antispoofing completa para el factor biométrico.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                                                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluya Winbio.h para aplicaciones cliente o Adaptadores \_ de Winbio.h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ACCIÓN DE \_ DIRECTIVA \_ ANTI SUPLANTACIÓN \_ DE SEGURIDAD DE \_ WINBIO**](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[**ORIGEN DE \_ LA DIRECTIVA \_ WINBIO**](winbio-policy-source.md)
</dt> </dl>

 

 






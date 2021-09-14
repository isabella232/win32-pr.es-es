---
title: WINBIO_ANTI_SPOOF_POLICY_ACTION enumeración (Tipos \_ de Winbio.h)
description: Especifica los tipos de acciones que se llevan a cabo para la directiva de antispoofing de un usuario.
ms.assetid: 846C0725-1796-49E4-883C-44AC7D618317
keywords:
- WINBIO_ANTI_SPOOF_POLICY_ACTION enumeración Windows BIOMETRIC Framework API
- PWINBIO_ANTI_SPOOF_POLICY puntero de enumeración Windows API de marco biométrico
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
ms.openlocfilehash: 5905624bad252475cdde12c003f31a734e64dd2e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160791"
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

<span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**WINBIO \_ ANTI \_ SUPOOF \_ DISABLE**
</dt> <dd>

Desactiva la detección de suplantación de un factor biométrico.

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**WINBIO \_ ANTI \_ SPOOF \_ ENABLE**
</dt> <dd>

Activa la detección de suplantación de seguridad para un factor biométrico.

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**ELIMINACIÓN \_ DE \_ LA SUPLANTACIÓN DE WINBIO \_ ANTI**
</dt> <dd>

Quita de la cuenta toda la directiva antispoofing para el factor biométrico.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                                                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ types.h (incluye Winbio.h para aplicaciones cliente o Adaptadores de \_ Winbio.h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ACCIÓN DE DIRECTIVA \_ \_ ANTI SUPLANTACIÓN DE \_ \_ WINBIO**](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[**ORIGEN DE \_ LA DIRECTIVA \_ WINBIO**](winbio-policy-source.md)
</dt> </dl>

 

 






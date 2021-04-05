---
title: Enumeración WINBIO_ANTI_SPOOF_POLICY_ACTION (Winbio \_ Types. h)
description: Especifica los tipos de acciones que se realizan para la Directiva de antifalsificación de un usuario.
ms.assetid: 846C0725-1796-49E4-883C-44AC7D618317
keywords:
- WINBIO_ANTI_SPOOF_POLICY_ACTION enumeración Plataforma de biometría de Windows API
- PWINBIO_ANTI_SPOOF_POLICY de puntero de enumeración Plataforma de biometría de Windows API
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996615"
---
# <a name="winbio_anti_spoof_policy_action-enumeration"></a>\_ \_ \_ Enumeración de acciones de directiva de WINBIO anti spoofing \_

Especifica los tipos de acciones que se realizan para la Directiva de antifalsificación de un usuario.

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

<span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**Deshabilitación de WINBIO \_ anti \_ Spoofing \_**
</dt> <dd>

Desactiva la detección de suplantación de identidad para un factor biométrico.

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**\_ \_ habilitación de WINBIO antispoofing \_**
</dt> <dd>

Activa la detección de suplantación de identidad para un factor biométrico.

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**\_quitar la \_ suplantación de WINBIO \_**
</dt> <dd>

Quita la Directiva de antifalsificación completa del factor biométrico de la cuenta.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                                                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h para aplicaciones cliente o \_ adaptadores de Winbio. h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**acción de directiva de WINBIO \_ anti \_ Spoofing \_ \_**](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[**\_origen de directiva de WINBIO \_**](winbio-policy-source.md)
</dt> </dl>

 

 






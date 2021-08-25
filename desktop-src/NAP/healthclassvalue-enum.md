---
title: Enumeración HealthClassValue (NapProtocol.h)
description: Indica el valor de la clase de mantenimiento TLV.
ms.assetid: af80c27a-a686-494b-8795-73eb366deaa0
keywords:
- Nap de enumeración HealthClassValue
topic_type:
- apiref
api_name:
- HealthClassValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b76b3fef268417f14bf22d2e25539a245cebc31820b746847f1e7b1091492b82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891645"
---
# <a name="healthclassvalue-enumeration"></a>Enumeración HealthClassValue

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **tipo de enumeración HealthClassValue** indica el valor de la clase de mantenimiento TLV.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagHealthClassValue { 
  healthClassFirewall        = 0,
  healthClassPatchLevel      = 1,
  healthClassAntiVirus       = 2,
  healthClassCriticalUpdate  = 3,
  healthClassReserved        = 128
} HealthClassValue;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="healthClassFirewall"></span><span id="healthclassfirewall"></span><span id="HEALTHCLASSFIREWALL"></span>**healthClassFirewall**
</dt> <dd>

La clase de mantenimiento TLV es firewall.

</dd> <dt>

<span id="healthClassPatchLevel"></span><span id="healthclasspatchlevel"></span><span id="HEALTHCLASSPATCHLEVEL"></span>**healthClassPatchLevel**
</dt> <dd>

La clase de mantenimiento TLV es el nivel de revisión.

</dd> <dt>

<span id="healthClassAntiVirus"></span><span id="healthclassantivirus"></span><span id="HEALTHCLASSANTIVIRUS"></span>**healthClassAntiVirus**
</dt> <dd>

La clase de mantenimiento TLV es antivirus.

</dd> <dt>

<span id="healthClassCriticalUpdate"></span><span id="healthclasscriticalupdate"></span><span id="HEALTHCLASSCRITICALUPDATE"></span>**healthClassCriticalUpdate**
</dt> <dd>

La clase de mantenimiento TLV es una actualización crítica.

</dd> <dt>

<span id="healthClassReserved"></span><span id="healthclassreserved"></span><span id="HEALTHCLASSRESERVED"></span>**healthClassReserved**
</dt> <dd>

Reservado solo para uso del sistema.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |



 

 






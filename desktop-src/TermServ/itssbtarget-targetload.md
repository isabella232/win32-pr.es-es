---
title: Propiedad TargetLoad de ITsSbTarget
description: Recupera la carga relativa en un destino.
ms.assetid: 56618dcf-1319-4310-80ba-7ed71b8b02e8
ms.tgt_platform: multiple
keywords:
- Propiedad TargetLoad Servicios de Escritorio remoto
- Propiedad TargetLoad Servicios de Escritorio remoto , interfaz ITsSbTarget
- Interfaz ITsSbTarget Servicios de Escritorio remoto , propiedad TargetLoad
- Propiedad TargetLoad Servicios de Escritorio remoto , interfaz ITsSbTargetEx
- Interfaz ITsSbTargetEx Servicios de Escritorio remoto , propiedad TargetLoad
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetLoad
- ITsSbTarget.get_TargetLoad
- ITsSbTargetEx.TargetLoad
- ITsSbTargetEx.get_TargetLoad
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8224106fad6031a18bf061020a259813db639e
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983928"
---
# <a name="itssbtargettargetload-property"></a>Propiedad ITsSbTarget::TargetLoad

Recupera la carga relativa en un destino. Este valor se basa en el número de sesiones existentes y pendientes. De forma predeterminada, una sesión pendiente tiene el mismo valor que una sesión existente.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_TargetLoad(
  [out, retval] DWORD *pTargetLoad
);
```



## <a name="property-value"></a>Valor de propiedad

Número que representa la carga relativa en un destino.

## <a name="remarks"></a>Observaciones

El peso de una sesión pendiente en relación con una sesión activa se puede cambiar estableciendo el valor del parámetro *\_ Lb ConnectionEstablishmentPenalty* para el Agente de conexión. Este parámetro se encuentra en la clave del Registro **HKLM \\ System \\ CurrentControlSet \\ Services \\ Tssdis \\ Parameters.** El valor predeterminado de 1 especifica que las sesiones pendientes tienen el mismo peso que las sesiones activas.

Esta propiedad está disponible en Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) instalado en la [**interfaz ITsSbTargetEx.**](itssbtargetex.md)

## <a name="requirements"></a>Requisitos




| Requisito | Value |
|--------|-------|
| Cliente mínimo compatible<br /> | No se admite ninguno<br /> | 
| Servidor mínimo compatible<br /> | Windows Server 2016<br /> | 
| IDL<br /> | <dl><dt>Sbtsv.idl</dt></dl> | 
| IID<br /> | IID_ITsSbTarget se define como:<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 en Windows Server 2008 R2</li></ul> | 




## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 






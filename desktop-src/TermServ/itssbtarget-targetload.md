---
title: Propiedad TargetLoad de ITsSbTarget
description: Recupera la carga relativa en un destino.
ms.assetid: 56618dcf-1319-4310-80ba-7ed71b8b02e8
ms.tgt_platform: multiple
keywords:
- Propiedades TargetLoad Servicios de Escritorio remoto
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
ms.openlocfilehash: 03d6d4839f60ef4b4af33498658bd78bf234c14f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482351"
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

## <a name="remarks"></a>Comentarios

El peso de una sesión pendiente con respecto a una sesión activa se puede cambiar estableciendo el valor del parámetro *\_ LB ConnectionEstablishmentPenalty* para el Agente de conexión. Este parámetro se encuentra en la clave del Registro **HKLM \\ System \\ CurrentControlSet \\ Services \\ Tssdis \\ Parameters.** El valor predeterminado de 1 especifica que las sesiones pendientes tienen el mismo peso que las sesiones activas.

Esta propiedad está disponible en Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) instalado en la [**interfaz ITsSbTargetEx.**](itssbtargetex.md)

## <a name="requirements"></a>Requisitos




| | | Cliente mínimo admitido<br /> | No se admite ninguna<br /> | | Servidor mínimo admitido<br /> | Windows Server 2016<br /> | | IDL<br /> | <dl><dt>Sbtsv.idl</dt></dl> | | IID<br /> | IID_ITsSbTarget se define como:<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 en Windows Server 2008 R2</li></ul> | 




## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 






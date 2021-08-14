---
title: Interfaz ITsSbTargetEx
description: Expone propiedades que almacenan información de configuración y estado sobre un destino.
ms.assetid: 3f0f26fb-e8bc-47eb-8038-e51792ad4376
ms.tgt_platform: multiple
keywords:
- Interfaz ITsSbTargetEx Servicios de Escritorio remoto
- Interfaz ITsSbTargetEx Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- ITsSbTargetEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fb9be0e4cf5c0395efa93d308fdfa45362a7ac8919ab49a108700106aff6081b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989825"
---
# <a name="itssbtargetex-interface"></a>Interfaz ITsSbTargetEx

Expone propiedades que almacenan información de configuración y estado sobre un destino.

Esta interfaz solo está disponible en Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) instalado. La [**propiedad TargetLoad**](itssbtarget-targetload.md) de la [**interfaz ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) está disponible a partir de Windows Server 2016.

## <a name="members"></a>Miembros

La **interfaz ITsSbTargetEx** hereda de [**ITsSbTarget.**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) **ITsSbTargetEx también** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz ITsSbTargetEx** tiene estas propiedades.



| Propiedad                                                                      | Tipo de acceso           | Descripción                                                                               |
|:------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [**EnvironmentName**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_environmentname)<br/>             | Lectura/escritura<br/> | Recupera o especifica el nombre del entorno asociado al destino.<br/> |
| [**FarmName**](itssbtarget-farmname.md)<br/>                           | Lectura/escritura<br/> | Especifica o recupera el nombre de la granja a la que está unido este destino.<br/>    |
| [**IpAddresses**](itssbtarget-ipaddresses.md)<br/>                     | Lectura/escritura<br/> | Recupera o especifica las direcciones IP externas del destino.<br/>                |
| [**NumPendingConnections**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numpendingconnections)<br/> | Solo lectura<br/>  | Recupera el número de conexiones de usuario pendientes para el destino.<br/>               |
| [**NumSessions**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numsessions)<br/>                     | Solo lectura<br/>  | Recupera el número de sesiones mantenidas por el agente para el destino.<br/>          |
| [**TargetFQDN**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetfqdn)<br/>                       | Lectura/escritura<br/> | Especifica o recupera el nombre de dominio completo del destino.<br/>          |
| [**TargetLoad**](/previous-versions/windows/desktop/legacy/mt703468(v=vs.85))<br/>                     | Solo lectura<br/>  | Recupera la carga relativa en un destino.<br/>                                       |
| [**TargetName**](itssbtarget-targetname.md)<br/>                       | Lectura/escritura<br/> | Especifica o recupera el nombre del destino.<br/>                                 |
| [**TargetNetbios**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetnetbios)<br/>                 | Lectura/escritura<br/> | Especifica o recupera el nombre NetBIOS del destino.<br/>                         |
| [**TargetPropertySet**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetpropertyset)<br/>         | Lectura/escritura<br/> | Especifica o recupera el conjunto de propiedades para el destino.<br/>                        |
| [**TargetState**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetstate)<br/>                     | Lectura/escritura<br/> | Especifica o recupera el estado de destino.<br/>                                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                        |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2012 R2<br/>                                                |
| IID<br/>                      | IID \_ ITsSbTargetEx se define como 74f99987-625d-11e5-bea1-a0481c7e9064<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[Escritorio remoto interfaces de virtualización](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 


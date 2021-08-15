---
title: Interfaz INapComponentConfig2 (NapCommon.h)
description: Proporciona métodos de configuración del sistema NAP para validadores de estado del sistema (SHV) para configurar una interfaz de usuario del servidor de directivas de red (NPS) de forma remota.
ms.assetid: 35150184-300c-4ea4-bff9-b3c33fa3156b
keywords:
- NAP de interfaz INapComponentConfig2
- Nap de interfaz INapComponentConfig2 , descrito
topic_type:
- apiref
api_name:
- INapComponentConfig2
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a80dfa1a9160b32b6d3c869795c9e23e41a5fdba39e38051bd29376caf8847
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368394"
---
# <a name="inapcomponentconfig2-interface"></a>Interfaz INapComponentConfig2

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **interfaz INapComponentConfig2** proporciona métodos de configuración del sistema NAP para validadores de estado del sistema (SHV) para configurar una interfaz de usuario del servidor de directivas de red (NPS) de forma remota.

> [!Note]  
> Esta interfaz hereda todos los métodos de [**INapComponentConfig**](inapcomponentconfig.md) y se debe usar en su lugar.

 

## <a name="members"></a>Miembros

La **interfaz INapComponentConfig2** hereda de [**INapComponentConfig.**](inapcomponentconfig.md) **INapComponentConfig2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz INapComponentConfig2** tiene estos métodos.



| Método                                                                                                | Descripción                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapComponentConfig2::InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md)           | Implementado por SHV según sea necesario para administrar la configuración remota directamente en la máquina especificada.<br/>                                                                 |
| [**INapComponentConfig2::InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md)   | Implementado por SHV según sea necesario para cargar la configuración de la máquina remota en memoria y para mostrar una interfaz de usuario que permita la manipulación de los datos de configuración.<br/> |
| [**INapComponentConfig2::IsRemoteConfigSupported**](inapcomponentconfig2-isremoteconfigsupported.md) | Implementado por SHV para indicar si se admite la configuración remota.<br/>                                                                                      |



 

## <a name="remarks"></a>Comentarios

Los agentes de mantenimiento del sistema (SHA) o los clientes de cumplimiento de cuarentena (QEC) no deben implementar esta interfaz.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

 






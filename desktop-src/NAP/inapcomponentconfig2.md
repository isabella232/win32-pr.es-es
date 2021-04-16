---
title: Interfaz INapComponentConfig2 (NapCommon. h)
description: Proporciona métodos de configuración del sistema NAP para validadores de mantenimiento del sistema (SHV) para configurar una interfaz de usuario del servidor de directivas de redes (NPS) de forma remota.
ms.assetid: 35150184-300c-4ea4-bff9-b3c33fa3156b
keywords:
- Interfaz INapComponentConfig2 NAP
- Interfaz INapComponentConfig2 NAP, descripción
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
ms.openlocfilehash: 29bd6fbea7696d0e4d5eacefd028ce7d33e549e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665955"
---
# <a name="inapcomponentconfig2-interface"></a>Interfaz INapComponentConfig2

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La interfaz **INapComponentConfig2** proporciona métodos de configuración del sistema NAP para los validadores de mantenimiento del sistema (SHV) para configurar una interfaz de usuario del servidor de directivas de redes (NPS) de forma remota.

> [!Note]  
> Esta interfaz hereda todos los métodos de [**INapComponentConfig**](inapcomponentconfig.md) y se debe usar en su lugar.

 

## <a name="members"></a>Miembros

La interfaz **INapComponentConfig2** hereda de [**INapComponentConfig**](inapcomponentconfig.md). **INapComponentConfig2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **INapComponentConfig2** tiene estos métodos.



| Método                                                                                                | Descripción                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapComponentConfig2::InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md)           | Implementado por SHV según sea necesario para administrar la configuración remota directamente en el equipo especificado.<br/>                                                                 |
| [**INapComponentConfig2::InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md)   | Implementado por SHV según sea necesario para cargar la configuración del equipo remoto en la memoria y mostrar una interfaz de usuario que permita la manipulación de los datos de configuración.<br/> |
| [**INapComponentConfig2::IsRemoteConfigSupported**](inapcomponentconfig2-isremoteconfigsupported.md) | Implementado por SHV para indicar si se admite la configuración remota.<br/>                                                                                      |



 

## <a name="remarks"></a>Observaciones

Esta interfaz no debe ser implementada por los agentes de mantenimiento del sistema (SHA) o los clientes de aplicación de cuarentena (QECs).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

 






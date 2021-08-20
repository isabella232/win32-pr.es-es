---
title: Interfaz INapEnforcementClientConnection2 (NapEnforcementClient.h)
description: Permitir la administración de conexiones de cliente. | Interfaz INapEnforcementClientConnection2 (NapEnforcementClient.h)
ms.assetid: f7b5d8cc-6a91-4e49-8957-cf67d1001089
keywords:
- NAP de la interfaz INapEnforcementClientConnection2
- Interfaz NAP de INapEnforcementClientConnection2 , descrita
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e60e91ffbc12534bb3b5a8ac22cbd13a1238ba32e09b4f56b4ab570ffd1ea8be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144398"
---
# <a name="inapenforcementclientconnection2-interface"></a>Interfaz INapEnforcementClientConnection2

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

**INapEnforcementClientConnection2** proporciona métodos que permiten la administración de conexiones de cliente.

> [!Note]  
> Esta interfaz hereda todos los métodos de [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) y se debe usar en su lugar.

 

## <a name="members"></a>Miembros

La **interfaz INapEnforcementClientConnection2** hereda de [**INapEnforcementClientConnection**](inapenforcementclientconnection.md). **INapEnforcementClientConnection2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz INapEnforcementClientConnection2** tiene estos métodos.



| Método                                                                                                              | Descripción                                                                      |
|:--------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**INapEnforcementClientConnection2::GetInstalledShvs**](inapenforcementclientconnection2-getinstalledshvs.md)     | Se usa para obtener los ID de los SHV instalados para el cliente.<br/>             |
| [**INapEnforcementClientConnection2::GetIsolationInfoEx**](inapenforcementclientconnection2-getisolationinfoex.md) | Se usa para obtener la información de aislamiento del cliente.<br/>                 |
| [**INapEnforcementClientConnection2::SetInstalledShvs**](inapenforcementclientconnection2-setinstalledshvs.md)     | Lo usa NapAgent para establecer los ID de SHV instalados para el cliente.<br/>     |
| [**INapEnforcementClientConnection2::SetIsolationInfoEx**](inapenforcementclientconnection2-setisolationinfoex.md) | Lo usa NapAgent para establecer la información de aislamiento del cliente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

 






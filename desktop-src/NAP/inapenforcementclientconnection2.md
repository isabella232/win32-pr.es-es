---
title: Interfaz INapEnforcementClientConnection2 (NapEnforcementClient. h)
description: Permite la administración de conexiones de cliente. | Interfaz INapEnforcementClientConnection2 (NapEnforcementClient. h)
ms.assetid: f7b5d8cc-6a91-4e49-8957-cf67d1001089
keywords:
- Interfaz INapEnforcementClientConnection2 NAP
- Interfaz INapEnforcementClientConnection2 NAP, descripción
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
ms.openlocfilehash: 3503e1bf6db01920e814b96e3daf5fe04eabc6b9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914361"
---
# <a name="inapenforcementclientconnection2-interface"></a>Interfaz INapEnforcementClientConnection2

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

**INapEnforcementClientConnection2** proporciona métodos que permiten la administración de conexiones de cliente.

> [!Note]  
> Esta interfaz hereda todos los métodos de [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) y se debe usar en su lugar.

 

## <a name="members"></a>Miembros

La interfaz **INapEnforcementClientConnection2** hereda de [**INapEnforcementClientConnection**](inapenforcementclientconnection.md). **INapEnforcementClientConnection2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **INapEnforcementClientConnection2** tiene estos métodos.



| Método                                                                                                              | Descripción                                                                      |
|:--------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**INapEnforcementClientConnection2::GetInstalledShvs**](inapenforcementclientconnection2-getinstalledshvs.md)     | Se usa para obtener los identificadores de los SHV instalados para el cliente.<br/>             |
| [**INapEnforcementClientConnection2::GetIsolationInfoEx**](inapenforcementclientconnection2-getisolationinfoex.md) | Se utiliza para obtener la información de aislamiento para el cliente.<br/>                 |
| [**INapEnforcementClientConnection2::SetInstalledShvs**](inapenforcementclientconnection2-setinstalledshvs.md)     | Lo usa NapAgent para establecer los identificadores de SHV instalados para el cliente.<br/>     |
| [**INapEnforcementClientConnection2::SetIsolationInfoEx**](inapenforcementclientconnection2-setisolationinfoex.md) | Lo usa NapAgent para establecer la información de aislamiento para el cliente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

 






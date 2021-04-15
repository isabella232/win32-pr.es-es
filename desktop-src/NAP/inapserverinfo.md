---
title: Interfaz INapServerInfo (NapServerManagement. h)
description: Los clientes de administración (por ejemplo, proveedores WMI o herramientas de línea de comandos) usan para consultar el estado del sistema del servidor NAP.
ms.assetid: 3c6d3f76-ea63-4cb2-bac7-e5668e50b7a7
keywords:
- Interfaz INapServerInfo NAP
- Interfaz INapServerInfo NAP, descripción
topic_type:
- apiref
api_name:
- INapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec17e3303fe4af4d359279de6c5fa7aa5f34d409
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676792"
---
# <a name="inapserverinfo-interface"></a>Interfaz INapServerInfo

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

**INapServerInfo** proporciona métodos que los clientes de administración (por ejemplo, proveedores WMI o herramientas de línea de comandos) usan para consultar el estado del sistema del servidor NAP.

## <a name="members"></a>Miembros

La interfaz **INapServerInfo** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapServerInfo** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **INapServerInfo** tiene estos métodos.



| Método                                                                                                                   | Descripción                                                             |
|:-------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**INapServerInfo::GetFailureCategoryMappings**](inapserverinfo-getfailurecategorymappings-method.md)                   | Recupera las asignaciones de categorías de error para un SHV especificado.<br/> |
| [**INapServerInfo::GetNapServerInfo**](inapserverinfo-getnapserverinfo-method.md)                                       | Recupera información acerca del servidor NAP.<br/>                  |
| [**INapServerInfo::GetRegisteredSystemHealthValidators**](inapserverinfo-getregisteredsystemhealthvalidators-method.md) | Recupera una lista de SHV registrados.<br/>                         |



 

## <a name="remarks"></a>Observaciones

Estos métodos proporcionan solo información estática sobre el servidor NAP y sus componentes en el sistema.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                               |
| Encabezado<br/>                   | <dl> <dt>NapServerManagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapServerManagement. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 


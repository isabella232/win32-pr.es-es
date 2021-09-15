---
title: Interfaz INapServerManagement (NapServerManagement.h)
description: Se usan para administrar el servidor NAP.
ms.assetid: 5c4f9bf1-fe82-48f5-8aa4-5c73ab01a78a
keywords:
- NAP de la interfaz INapServerManagement
- Nap de interfaz INapServerManagement , descrito
topic_type:
- apiref
api_name:
- INapServerManagement
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5eed03f535653a3b9244ff1aa74fe499c1bf2f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473768"
---
# <a name="inapservermanagement-interface"></a>Interfaz INapServerManagement

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

**INapServerManagement proporciona** métodos que se usan para administrar el servidor NAP.

## <a name="members"></a>Members

La **interfaz INapServerManagement** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapServerManagement** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz INapServerManagement** tiene estos métodos.



| Método                                                                                                                       | Descripción                                          |
|:-----------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------|
| [**INapServerManagement::RegisterSystemHealthValidator**](inapservermanagement-registersystemhealthvalidator-method.md)     | Registra una SHV.<br/>                         |
| [**INapServerManagement::SetFailureCategoryMappings**](inapservermanagement-setfailurecategorymappings-method.md)           | Establece las asignaciones de categorías de error de SHV.<br/> |
| [**INapServerManagement::UnregisterSystemHealthValidator**](inapservermanagement-unregistersystemhealthvalidator-method.md) | Anula el registro de una SHV del servidor NAP.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                               |
| Encabezado<br/>                   | <dl> <dt>NapServerManagement.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapServerManagement.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 


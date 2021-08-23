---
title: Interfaz INapServerCallback (NapSystemHealthValidator.h)
description: Las SHV usan para indicar la finalización de solicitudes asincrónicas.
ms.assetid: 0138767a-9553-4de0-87da-97dd92906406
keywords:
- NAP de interfaz INapServerCallback
- Nap de interfaz INapServerCallback , descrito
topic_type:
- apiref
api_name:
- INapServerCallback
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47876290a58d6029559ef4d18baa9067913fe9034cbf218e40f0e382902270e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626155"
---
# <a name="inapservercallback-interface"></a>Interfaz INapServerCallback

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

**INapServerCallback proporciona** un método que los SHV usan para indicar la finalización de solicitudes asincrónicas.

## <a name="members"></a>Miembros

La **interfaz INapServerCallback** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapServerCallback** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz INapServerCallback** tiene estos métodos.



| Método                                                                         | Descripción                                                        |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**INapServerCallback::OnComplete**](inapservercallback-oncomplete-method.md) | Usado por shvs para indicar la finalización de solicitudes asincrónicas.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Header<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 


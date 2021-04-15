---
description: La definición de la interfaz ISCardAuth se proporciona como un estándar que se puede seguir al desarrollar un proveedor de servicios de tarjetas inteligentes. La interfaz ISCardAuth se puede usar para exponer los servicios de autenticación admitidos por una tarjeta inteligente.
ms.assetid: 6b8a5b90-49ad-48fd-813c-c3c3337ec8f1
title: Interfaz ISCardAuth
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth
api_type:
- COM
api_location: ''
ms.openlocfilehash: bf8df3702aceb2ac8bbf5ad090802be2dc07e45a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497296"
---
# <a name="iscardauth-interface"></a>Interfaz ISCardAuth

\[La interfaz **ISCardAuth** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

La definición de la interfaz **ISCardAuth** se proporciona como un estándar que se puede seguir al desarrollar un [*proveedor de servicios*](../secgloss/c-gly.md)de [*tarjetas inteligentes*](../secgloss/s-gly.md) .

La interfaz **ISCardAuth** se puede usar para exponer los servicios de autenticación admitidos por una tarjeta inteligente. Estos servicios incluyen la autenticación de la aplicación, la autenticación mediante tarjeta inteligente y la autenticación de usuario.

En el ejemplo siguiente se muestra un uso típico de la interfaz **ISCardAuth** .

**Para usar ISCardAuth**

1.  Cree una interfaz **ISCardAuth** (mediante el método de interfaz [**ISCardManage**](iscardmanage.md) correspondiente).
2.  Llame al método **ISCardAuth** adecuado ([**\_ autenticación**](iscardauth-app-auth.md)de la aplicación, [**GetChallenge**](iscardauth-getchallenge.md), [**\_ autenticación ICC**](iscardauth-icc-auth.md)o [**\_ autenticación de usuario**](iscardauth-user-auth.md)).
3.  Libere la interfaz **ISCardAuth** .

## <a name="members"></a>Miembros

La interfaz **ISCardAuth** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardAuth** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ISCardAuth** tiene estos métodos.



| Método                                          | Descripción                                                                                    |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Autenticación de la aplicación \_**](iscardauth-app-auth.md)        | Permite que la aplicación se autentique mediante un protocolo de desafío/firma.<br/> |
| [**GetChallenge**](iscardauth-getchallenge.md) | Devuelve un desafío de la tarjeta inteligente.<br/>                                            |
| [**Autenticación de ICC \_**](iscardauth-icc-auth.md)        | Permite que una aplicación autentique la tarjeta inteligente.<br/>                               |
| [**Autenticación de usuario \_**](iscardauth-user-auth.md)      | Permite el acceso a los servicios de autenticación de usuario.<br/>                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                       |



 

 

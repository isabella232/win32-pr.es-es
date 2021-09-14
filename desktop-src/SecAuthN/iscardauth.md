---
description: La definición de la interfaz ISCardAuth se proporciona como un estándar que se puede seguir al desarrollar un proveedor de servicios de tarjeta inteligente. La interfaz ISCardAuth se puede usar para exponer los servicios de autenticación compatibles con una tarjeta inteligente.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259719"
---
# <a name="iscardauth-interface"></a>Interfaz ISCardAuth

\[La **interfaz ISCardAuth** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

La definición de la interfaz **ISCardAuth** se proporciona como un estándar que se puede seguir al desarrollar un [*proveedor de servicios de tarjeta*](../secgloss/s-gly.md) [*inteligente*](../secgloss/c-gly.md).

La **interfaz ISCardAuth** se puede usar para exponer los servicios de autenticación compatibles con una tarjeta inteligente. Estos servicios incluyen la autenticación de aplicaciones, la autenticación de tarjeta inteligente y la autenticación de usuario.

En el ejemplo siguiente se muestra un uso típico de la **interfaz ISCardAuth.**

**Para usar ISCardAuth**

1.  Cree una **interfaz ISCardAuth** (mediante el método de [**interfaz ISCardManage**](iscardmanage.md) correspondiente).
2.  Llame al método **ISCardAuth** adecuado [**(APP \_ Auth,**](iscardauth-app-auth.md) [**GetChallenge,**](iscardauth-getchallenge.md) [**LA AUTENTICACIÓN DE ORI \_**](iscardauth-icc-auth.md)o [**\_ Autenticación de usuario).**](iscardauth-user-auth.md)
3.  Libere la **interfaz ISCardAuth.**

## <a name="members"></a>Members

La **interfaz ISCardAuth** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardAuth también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ISCardAuth** tiene estos métodos.



| Método                                          | Descripción                                                                                    |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Autenticación \_ de aplicaciones**](iscardauth-app-auth.md)        | Permite que la aplicación se autentique mediante un protocolo de desafío o firma.<br/> |
| [**GetChallenge**](iscardauth-getchallenge.md) | Devuelve un desafío de la tarjeta inteligente.<br/>                                            |
| [**Autenticación DE LA \_ TOI**](iscardauth-icc-auth.md)        | Permite que una aplicación autentique la tarjeta inteligente.<br/>                               |
| [**Autenticación \_ de usuario**](iscardauth-user-auth.md)      | Permite el acceso a los servicios de autenticación de usuario.<br/>                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                       |



 

 

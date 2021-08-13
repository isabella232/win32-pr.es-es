---
title: AccessPermission
description: Describe la lista Access Control (ACL) de las entidades de seguridad que pueden tener acceso a instancias de esta clase. Esta ACL solo la usan las aplicaciones que no llaman a CoInitializeSecurity.
ms.assetid: 92518de0-66ca-4d7a-8d91-63b41e6d3c24
keywords:
- AccessPermission registry value COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 641512d34b963879ceb3d1a6266a017836879b224b228edb3ad62d61300fb03e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551349"
---
# <a name="accesspermission"></a>AccessPermission

Describe la lista Access Control (ACL) de las entidades de seguridad que pueden tener acceso a instancias de esta clase. Esta ACL solo la usan las aplicaciones que no llaman a [**CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AccessPermission = ACL
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG BINARY.** Contiene datos que describen la lista de Access Control (ACL) de las entidades de seguridad que pueden acceder a instancias de esta clase. Al recibir una solicitud para conectarse a un objeto existente de esta clase, la aplicación a la que se llama comprueba la ACL al suplantar al autor de la llamada. Si se produce un error en la comprobación de acceso, no se permite la conexión. Si este valor con nombre no existe, se prueba la ACL [**DefaultAccessPermission**](defaultaccesspermission.md) para determinar si se va a permitir la conexión.

En el caso de las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o no usan la interfaz [**IGlobalOptions**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) para especificar el AppID, el ejecutable del binario de la aplicación debe asignarse al AppID de la aplicación como se describe en [**AppID**](appid.md). Esto es necesario para que COM pueda localizar el AppID de la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**DefaultAccessPermission**](defaultaccesspermission.md)
</dt> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 
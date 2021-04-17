---
title: AccessPermission
description: Describe la lista de Access Control (ACL) de las entidades de seguridad que pueden tener acceso a las instancias de esta clase. Esta ACL solo la usan las aplicaciones que no llaman a CoInitializeSecurity.
ms.assetid: 92518de0-66ca-4d7a-8d91-63b41e6d3c24
keywords:
- Valor del registro AccessPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6210eba77f614b16c8fde59948b350ad150909
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488314"
---
# <a name="accesspermission"></a>AccessPermission

Describe la lista de Access Control (ACL) de las entidades de seguridad que pueden tener acceso a las instancias de esta clase. Esta ACL solo la usan las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AccessPermission = ACL
```

## <a name="remarks"></a>Observaciones

Se trata de un valor **\_ binario de registro** . Contiene datos que describen la lista de Access Control (ACL) de las entidades de seguridad que pueden tener acceso a las instancias de esta clase. Al recibir una solicitud para conectarse a un objeto existente de esta clase, se comprueba la ACL de la aplicación a la que se llama durante la suplantación del autor de la llamada. Si se produce un error en la comprobación de acceso, no se permite la conexión. Si este valor con nombre no existe, la ACL [**DefaultAccessPermission**](defaultaccesspermission.md) se prueba para determinar si la conexión se va a permitir.

En el caso de las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o no usan la interfaz [**IGlobalOptions**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) para especificar el AppID, el archivo ejecutable del archivo binario de la aplicación debe estar asignado al AppID de la aplicación, tal y como se describe en [**AppID**](appid.md). Esto es necesario para que COM pueda localizar el AppID de la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Fall**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**DefaultAccessPermission**](defaultaccesspermission.md)
</dt> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 
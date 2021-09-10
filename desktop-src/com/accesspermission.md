---
title: AccessPermission
description: Describe la Access Control lista de entidades de seguridad (ACL) de las entidades de seguridad que pueden tener acceso a las instancias de esta clase. Esta ACL solo la usan las aplicaciones que no llaman a CoInitializeSecurity.
ms.assetid: 92518de0-66ca-4d7a-8d91-63b41e6d3c24
keywords:
- Valor del Registro AccessPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6210eba77f614b16c8fde59948b350ad150909
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369532"
---
# <a name="accesspermission"></a>AccessPermission

Describe la Access Control lista de entidades de seguridad (ACL) de las entidades de seguridad que pueden tener acceso a las instancias de esta clase. Esta ACL solo la usan las aplicaciones que no llaman a [**CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AccessPermission = ACL
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG BINARY.** Contiene datos que describen la lista Access Control (ACL) de las entidades de seguridad que pueden tener acceso a las instancias de esta clase. Al recibir una solicitud para conectarse a un objeto existente de esta clase, la aplicación a la que se llama comprueba la ACL mientras suplanta al autor de la llamada. Si se produce un error en la comprobación de acceso, no se permite la conexión. Si este valor con nombre no existe, se prueba la ACL [**DefaultAccessPermission**](defaultaccesspermission.md) para determinar si se va a permitir la conexión.

En el caso de las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o que no usan la interfaz [**IGlobalOptions**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) para especificar el AppID, el archivo ejecutable del archivo binario de la aplicación debe asignarse al AppID de la aplicación como se describe en [**AppID**](appid.md). Esto es necesario para que COM pueda buscar el AppID de la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**DefaultAccessPermission**](defaultaccesspermission.md)
</dt> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 
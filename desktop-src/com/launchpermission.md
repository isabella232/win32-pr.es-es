---
title: LaunchPermission
description: Describe la lista Access Control (ACL) de las entidades de seguridad que pueden iniciar nuevos servidores para esta clase. Este valor se puede agregar bajo cualquier clave AppID para limitar la activación por parte de clientes remotos de clases específicas.
ms.assetid: 7b8c1ae4-fbbd-489f-b1b5-60ae5a04f906
keywords:
- Valor del Registro LaunchPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5967ee63288b11edca017820b9a367dd4e6c017e993330616e633e7448a098b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756105"
---
# <a name="launchpermission"></a>LaunchPermission

Describe la lista Access Control (ACL) de las entidades de seguridad que pueden iniciar nuevos servidores para esta clase. Este valor se puede agregar bajo cualquier clave [**AppID**](appid-key.md) para limitar la activación por parte de clientes remotos de clases específicas.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LaunchPermission = ACL
```

## <a name="remarks"></a>Comentarios

Se trata de **un valor \_ REG BINARY.** Al recibir una solicitud local o remota para iniciar el servidor de esta clase, la ACL descrita por este valor se comprueba al suplantar al cliente y su éxito permite o no permite el inicio del servidor. Si este valor no existe, el valor [**DefaultLaunchPermission**](defaultlaunchpermission.md) se comprueba de la misma manera para determinar si se puede iniciar el código de clase.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**DefaultLaunchPermission**](defaultlaunchpermission.md)
</dt> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 





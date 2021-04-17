---
title: DefaultAccessPermission
description: Establece la lista de Access Control (ACL) de las entidades de seguridad que pueden tener acceso a las clases para las que no hay ningún valor AccessPermission.
ms.assetid: 02675d0e-a96c-476e-820e-e6ff3c2d1be1
keywords:
- Valor del registro DefaultAccessPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e6c132096807b8c234259071758ebd361421f8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704571"
---
# <a name="defaultaccesspermission"></a>DefaultAccessPermission

Establece la lista de Access Control (ACL) de las entidades de seguridad que pueden tener acceso a las clases para las que no hay ningún valor [**AccessPermission**](accesspermission.md) . Esta ACL solo la usan las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) y no tienen un valor **AccessPermission** bajo su clave [**AppID**](appid-key.md) .

> [!Caution]  
> No se recomienda cambiar este valor, ya que esto afectará a todas las aplicaciones de servidor COM que no establezcan su propia seguridad en todo el proceso y podrían impedir que funcionen correctamente. Si va a cambiar este valor para que afecte a la configuración de seguridad de una aplicación COM determinada, debe cambiar la configuración de seguridad de todo el proceso para esa aplicación COM en particular. Para obtener más información sobre cómo establecer la seguridad de todo el proceso, consulte [configuración de la seguridad de todo el proceso](setting-processwide-security.md).

 

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultAccessPermission = ACL
```

## <a name="remarks"></a>Observaciones

Se trata de un valor **\_ binario de registro** .

El tiempo de ejecución de COM en el servidor comprueba la ACL descrita por este valor durante la suplantación del autor de la llamada que está intentando conectarse al objeto y su éxito determina si se permite o no el acceso. Si se produce un error en la comprobación de acceso, no se permite la conexión con el objeto. Si este valor con nombre no existe, solo se permite a la entidad de seguridad del servidor y al sistema local llamar al servidor.

De forma predeterminada, este valor no tiene ninguna entrada. Solo la entidad de seguridad de servidor y el sistema pueden llamar al servidor.

Este valor proporciona un nivel simple de administración centralizada del acceso de conexión predeterminado a los objetos en ejecución en un equipo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**AccessPermission**](accesspermission.md)
</dt> <dt>

[Registrar servidores COM](registering-com-servers.md)
</dt> <dt>

[Establecer la seguridad de todo el proceso](setting-processwide-security.md)
</dt> </dl>

 

 





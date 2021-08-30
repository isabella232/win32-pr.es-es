---
title: DefaultAccessPermission
description: Establece la Access Control lista de entidades de seguridad (ACL) de las entidades de seguridad que pueden tener acceso a clases para las que no hay ninguna configuración AccessPermission.
ms.assetid: 02675d0e-a96c-476e-820e-e6ff3c2d1be1
keywords:
- Valor del Registro DefaultAccessPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95e41803dc70a894e2c230c5c6231a4b7ab7c166c7926a8fff900ebd183a41da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993415"
---
# <a name="defaultaccesspermission"></a>DefaultAccessPermission

Establece la Access Control lista de entidades de seguridad (ACL) de las entidades de seguridad que pueden tener acceso a clases para las que no hay ninguna [**configuración AccessPermission.**](accesspermission.md) Esta ACL solo la usan las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) y no tienen un valor **AccessPermission** bajo su [**clave AppID.**](appid-key.md)

> [!Caution]  
> No se recomienda cambiar este valor, ya que esto afectará a todas las aplicaciones de servidor COM que no establezcan su propia seguridad en todo el proceso y podrían impedir que funcionen correctamente. Si va a cambiar este valor para que afecte a la configuración de seguridad de una aplicación COM determinada, en su lugar debe cambiar la configuración de seguridad de todo el proceso para esa aplicación COM concreta. Para obtener más información sobre cómo establecer la seguridad de todo el proceso, vea [Establecer la seguridad de todo el proceso.](setting-processwide-security.md)

 

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultAccessPermission = ACL
```

## <a name="remarks"></a>Comentarios

Se trata de **un valor \_ REG BINARY.**

El tiempo de ejecución COM del servidor comprueba la ACL descrita por este valor al suplantar al autor de la llamada que está intentando conectarse al objeto y su éxito determina si se permite o no el acceso. Si se produce un error en la comprobación de acceso, no se permite la conexión al objeto . Si este valor con nombre no existe, solo la entidad de seguridad del servidor y el sistema local pueden llamar al servidor.

De forma predeterminada, este valor no tiene entradas. Solo la entidad de seguridad y el sistema del servidor pueden llamar al servidor.

Este valor proporciona un nivel sencillo de administración centralizada del acceso de conexión predeterminado a los objetos en ejecución en un equipo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**AccessPermission**](accesspermission.md)
</dt> <dt>

[Registro de servidores COM](registering-com-servers.md)
</dt> <dt>

[Establecer la seguridad de todo el proceso](setting-processwide-security.md)
</dt> </dl>

 

 





---
title: DefaultAccessPermission
description: Establece la Access Control lista de entidades de seguridad (ACL) de las entidades de seguridad que pueden tener acceso a clases para las que no hay ninguna configuración AccessPermission.
ms.assetid: 02675d0e-a96c-476e-820e-e6ff3c2d1be1
keywords:
- Valor del Registro DefaultAccessPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e6c132096807b8c234259071758ebd361421f8f
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369531"
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

## <a name="remarks"></a>Observaciones

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

 

 





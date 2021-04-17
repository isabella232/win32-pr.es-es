---
description: El instalador establece el valor de la propiedad UserSID en la representación de cadena del identificador de seguridad (SID) del usuario que ejecuta la instalación. Para obtener más información, vea estructuras de autorización.
ms.assetid: 94524636-c7f2-4de2-b35e-644c0c171193
title: UserSID (propiedad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fab01b3f87c654a306bfe3633adf0973ed58aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653659"
---
# <a name="usersid-property"></a>UserSID (propiedad)

El instalador establece el valor de la propiedad **UserSID** en la representación de cadena del identificador de seguridad (SID) del usuario que ejecuta la instalación. Para obtener más información, vea [estructuras de autorización](../secauthz/authorization-structures.md).

## <a name="default-value"></a>Valor predeterminado

Ninguno.

## <a name="remarks"></a>Observaciones

El Windows Installer establecer esta propiedad en Windows 2000, Windows XP y Windows Vista. Esta propiedad no está definida en el resto de sistemas operativos.

Tenga en cuenta que esta propiedad tiene el atributo especial que se puede recuperar de una acción personalizada diferida. Una acción personalizada que se ejecuta con privilegios elevados puede seguir devolviendo el SID del usuario en la propiedad **UserSID** . Para obtener más información, vea [obtener información de contexto para las acciones personalizadas de ejecución aplazada](obtaining-context-information-for-deferred-execution-custom-actions.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 

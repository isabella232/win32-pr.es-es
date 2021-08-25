---
description: El instalador establece el valor de la propiedad UserSID en la representación de cadena del identificador de seguridad (SID) del usuario que ejecuta la instalación. Para obtener más información, vea Estructuras de autorización.
ms.assetid: 94524636-c7f2-4de2-b35e-644c0c171193
title: Propiedad UserSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b26185c886117b39355241151ffef6d8615bd5f8d10a7f50bd5937a301f7b398
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809165"
---
# <a name="usersid-property"></a>Propiedad UserSID

El instalador establece el valor de la **propiedad UserSID** en la representación de cadena del identificador de seguridad (SID) del usuario que ejecuta la instalación. Para obtener más información, vea [Estructuras de autorización](../secauthz/authorization-structures.md).

## <a name="default-value"></a>Valor predeterminado

Ninguno.

## <a name="remarks"></a>Comentarios

El instalador Windows establece esta propiedad en Windows 2000, Windows XP y Windows Vista. Esta propiedad no está definida en el resto de sistemas operativos.

Tenga en cuenta que esta propiedad tiene el atributo especial que se puede recuperar de una acción personalizada diferida. Una acción personalizada que se ejecuta con privilegios elevados todavía puede devolver el SID del usuario en **la propiedad UserSID.** Para obtener información, vea Obtener información de contexto para acciones personalizadas [de ejecución aplazada.](obtaining-context-information-for-deferred-execution-custom-actions.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 

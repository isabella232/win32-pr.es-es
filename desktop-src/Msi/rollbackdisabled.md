---
description: El instalador establece la propiedad RollbackDisabled cuando se ha deshabilitado la reversión.
ms.assetid: 72215b0f-2fc4-49aa-abf8-3206bdfc765f
title: Propiedad RollbackDisabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1df5b392a69a04811853a449106858445969fed3b2c0598266ff3f8a1bcb51a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039875"
---
# <a name="rollbackdisabled-property"></a>Propiedad RollbackDisabled

El instalador establece la **propiedad RollbackDisabled** cuando se ha deshabilitado la reversión. Los autores de paquetes que necesitan asegurarse de que el instalador no ha deshabilitado la reversión usan **RollbackDisabled.** La **propiedad RollbackDisabled** se puede usar en una expresión condicional que rechaza de forma eficaz continuar con la instalación si se establece la propiedad **RollbackDisabled.**

## <a name="default-value"></a>Valor predeterminado

De forma predeterminada, la reversión está habilitada.

## <a name="remarks"></a>Comentarios

Dado [que la reversión](rollback-custom-actions.md) [y](commit-custom-actions.md) confirmación no se ejecutan mientras la reversión está deshabilitada, el instalador no puede instalar correctamente un paquete que use estos tipos de acciones personalizadas en una transacción durante la instalación. En este caso, el autor del paquete debe incluir una condición mediante DisableRollback que impida que la instalación continúe si la reversión está deshabilitada.

Un administrador puede establecer el valor de directiva DisableRollback como parte de la asignación de la directiva del sistema. Se recomienda a los administradores no deshabilitar la reversión a menos que sea necesario. Para obtener más información sobre el valor de la directiva DisableRollback, vea [Directiva del sistema](system-policy.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Instalación de reversión](rollback-installation.md)
</dt> <dt>

[Directiva del sistema](system-policy.md)
</dt> <dt>

[acciones personalizadas de reversión](rollback-custom-actions.md)
</dt> <dt>

[acciones personalizadas de confirmación](commit-custom-actions.md)
</dt> </dl>

 

 





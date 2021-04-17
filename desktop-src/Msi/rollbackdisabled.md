---
description: El instalador establece la propiedad RollbackDisabled cuando se ha deshabilitado la reversión.
ms.assetid: 72215b0f-2fc4-49aa-abf8-3206bdfc765f
title: Propiedad RollbackDisabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f50c8e344ed4291210afb1714ce97d90b590999
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653469"
---
# <a name="rollbackdisabled-property"></a>Propiedad RollbackDisabled

El instalador establece la propiedad **RollbackDisabled** cuando se ha deshabilitado la reversión. **RollbackDisabled** lo utilizan los autores de paquetes que necesitan asegurarse de que el instalador no haya deshabilitado la reversión. La propiedad **RollbackDisabled** se puede usar en una expresión condicional que evita que continúe con la instalación si se establece la propiedad **RollbackDisabled** .

## <a name="default-value"></a>Valor predeterminado

De forma predeterminada, la reversión está habilitada.

## <a name="remarks"></a>Observaciones

Dado que la [reversión](rollback-custom-actions.md) y la [confirmación](commit-custom-actions.md) no se ejecutan mientras la reversión está deshabilitada, el instalador no puede instalar correctamente un paquete que use estos tipos de acciones personalizadas en una transacción durante la instalación. En este caso, el autor del paquete debe incluir una condición con DisableRollback que impida que la instalación continúe si la reversión está deshabilitada.

Un administrador puede establecer el valor de la Directiva DisableRollback como parte de la asignación de la Directiva del sistema. A los administradores se les aconseja no deshabilitar la reversión a menos que sea necesario. Para obtener más información sobre el valor de directiva de DisableRollback, consulte [Directiva del sistema](system-policy.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Revertir instalación](rollback-installation.md)
</dt> <dt>

[Directiva del sistema](system-policy.md)
</dt> <dt>

[revertir acciones personalizadas](rollback-custom-actions.md)
</dt> <dt>

[Confirmar acciones personalizadas](commit-custom-actions.md)
</dt> </dl>

 

 





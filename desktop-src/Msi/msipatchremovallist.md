---
description: El instalador establece el valor de la propiedad MsiPatchRemovalList en una lista de revisiones que se van a quitar durante la instalación.
ms.assetid: 6e0b391a-d840-4f01-af12-4708ce6c9ce8
title: Propiedad MsiPatchRemovalList
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93df2cdfc658875526c049ca7503e66a5c318df896a604a82c18751ac3358285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065985"
---
# <a name="msipatchremovallist-property"></a>Propiedad MsiPatchRemovalList

El instalador establece el valor de la propiedad **MsiPatchRemovalList** en una lista de revisiones que se van a quitar durante la instalación. Las revisiones se representan en la lista mediante sus GUID de código de revisión separados por punto y coma.

Los desarrolladores pueden usar la propiedad **MsiPatchRemovalList** para crear un paquete o revisión de Windows Installer que realiza acciones [personalizadas](custom-actions.md) en la eliminación de una revisión. La acción personalizada se puede crear en el paquete de instalación original, una revisión que ya se ha aplicado al paquete o una revisión que no es una revisión [que se puede desinstalar.](uninstallable-patches.md) La acción personalizada se puede condicionalizar en la **propiedad MsiPatchRemovalList** en las tablas de secuencia. Vea [Using Properties in Conditional Statements (Uso](using-properties-in-conditional-statements.md) de propiedades en instrucciones condicionales) para obtener más información sobre las acciones de condicionalización.

La acción personalizada puede obtener los GUID de las revisiones que se quitan del valor de la **propiedad MsiPatchRemovalList.** La acción personalizada puede determinar si el estado de instalación de la revisión se aplica, está obsoleto o se reemplaza llamando a la función [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) o a la propiedad [**PatchProperty**](patch-patchproperty.md) del [objeto Patch](patch-object.md).

## <a name="remarks"></a>Comentarios

Para obtener más información sobre cómo quitar revisiones, vea [Quitar revisiones.](removing-patches.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003 o Windows XP. Consulte Windows [Installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





---
description: El instalador establece el valor de la propiedad MsiPatchRemovalList en una lista de revisiones que se están quitando durante la instalación.
ms.assetid: 6e0b391a-d840-4f01-af12-4708ce6c9ce8
title: Propiedad MsiPatchRemovalList
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2af522d9570297f2ff911b501bc543cf4b5971c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670644"
---
# <a name="msipatchremovallist-property"></a>Propiedad MsiPatchRemovalList

El instalador establece el valor de la propiedad **MsiPatchRemovalList** en una lista de revisiones que se están quitando durante la instalación. Las revisiones se representan en la lista mediante sus GUID de código de revisión separados por punto y coma.

Los desarrolladores pueden usar la propiedad **MsiPatchRemovalList** para crear un paquete de Windows Installer o revisión que realice [acciones personalizadas](custom-actions.md) en la eliminación de una revisión. La acción personalizada se puede crear en el paquete de instalación original, en una revisión que ya se haya aplicado al paquete o en una revisión que no sea de [instalación](uninstallable-patches.md). La acción personalizada se puede condicionar en la propiedad **MsiPatchRemovalList** de las tablas de secuencia. Vea [usar propiedades en instrucciones condicionales](using-properties-in-conditional-statements.md) para obtener más información sobre las acciones de condicional.

La acción personalizada puede obtener los GUID de las revisiones que se van a quitar del valor de la propiedad **MsiPatchRemovalList** . La acción personalizada puede determinar si el estado de instalación de la revisión se aplica, está obsoleto o se ha sustituido mediante una llamada a la función [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) o la propiedad [**PatchProperty**](patch-patchproperty.md) del [objeto patch](patch-object.md).

## <a name="remarks"></a>Observaciones

Para obtener más información acerca de cómo quitar revisiones, consulte [quitar revisiones](removing-patches.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer 3,0 o posterior en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





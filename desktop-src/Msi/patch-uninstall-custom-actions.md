---
description: Puede usar la opción de desinstalación de revisión de acción personalizada para especificar que el instalador ejecute la acción personalizada solo cuando se desinstale una revisión.
ms.assetid: c741aa40-ba4c-459e-936a-19c002620c30
title: Revisión de desinstalación de acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90cfffbdb37f1f2fab046b794010a790e9a5212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666463"
---
# <a name="patch-uninstall-custom-actions"></a>Revisión de desinstalación de acciones personalizadas

Puede usar la [opción de desinstalación de revisión de acción personalizada](custom-action-patch-uninstall-option.md) para especificar que el instalador ejecute la acción personalizada solo cuando se desinstale una revisión.

**Windows Installer 4,5 y versiones posteriores:** Puede usar la [opción de desinstalación de revisión de acción personalizada](custom-action-patch-uninstall-option.md) para especificar que el instalador solo ejecute la acción personalizada cuando se desinstale una revisión.

**[Windows Installer 4,0 y versiones anteriores](not-supported-in-windows-installer-4-0.md): * *

La [opción de desinstalación de revisión de acción personalizada](custom-action-patch-uninstall-option.md) no está disponible. No hay ningún método para marcar una [acción personalizada](custom-actions.md) en un paquete de revisión que se ejecute cuando se desinstale la revisión porque el instalador no aplica los paquetes de revisión que se desinstalan.

Para que se ejecute una [acción personalizada](custom-actions.md) cuando se desinstale una revisión determinada, la acción personalizada debe estar presente en la aplicación original o en una revisión para el producto que siempre se aplica.

Los desarrolladores pueden usar la propiedad [**MsiPatchRemovalList**](msipatchremovallist.md) para crear un paquete de Windows Installer o revisión que realice [acciones personalizadas](custom-actions.md) en la eliminación de una revisión. La acción personalizada se puede crear en el paquete de instalación original, en una revisión que ya se haya aplicado al paquete o en una revisión que no sea de [instalación](uninstallable-patches.md). La acción personalizada se puede condicionar en la propiedad **MsiPatchRemovalList** de las tablas de secuencia. Vea [usar propiedades en instrucciones condicionales](using-properties-in-conditional-statements.md) para obtener más información sobre las acciones de condicional.

La acción personalizada puede obtener los GUID de las revisiones que se van a quitar del valor de la propiedad [**MsiPatchRemovalList**](msipatchremovallist.md) . La acción personalizada puede determinar si el estado de instalación de la revisión se aplica, está obsoleto o se ha sustituido mediante una llamada a la propiedad [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) o [**PatchProperty**](patch-patchproperty.md) del [objeto patch](patch-object.md).

Si la acción personalizada requiere metadatos especiales de la revisión, la revisión debe contener una acción personalizada que escriba los metadatos en un registro o ubicación de archivo cuando se aplique la revisión. La acción personalizada en la aplicación original o una revisión aplicada siempre puede obtener la información necesaria para quitar los cambios de la revisión.

Las revisiones que realizan cambios difíciles de deshacer correctamente no deben marcarse como revisiones que no se pueden [instalar](uninstallable-patches.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Secuenciación de revisiones](sequencing-patches.md)
</dt> <dt>

[Quitar revisiones](removing-patches.md)
</dt> <dt>

[Revisiones desinstalables](uninstallable-patches.md)
</dt> <dt>

[Desinstalación de revisiones](uninstalling-patches.md)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 




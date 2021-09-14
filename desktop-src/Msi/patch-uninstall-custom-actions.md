---
description: Puede usar la opción Custom Action Patch Uninstall para especificar que el instalador ejecute la acción personalizada solo cuando se desinstala una revisión.
ms.assetid: c741aa40-ba4c-459e-936a-19c002620c30
title: Acciones personalizadas de desinstalación de revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90cfffbdb37f1f2fab046b794010a790e9a5212
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173669"
---
# <a name="patch-uninstall-custom-actions"></a>Acciones personalizadas de desinstalación de revisiones

Puede usar la opción [Custom Action Patch Uninstall](custom-action-patch-uninstall-option.md) para especificar que el instalador ejecute la acción personalizada solo cuando se desinstala una revisión.

**Windows Installer 4.5 y versiones posteriores:** Puede usar la opción [de desinstalación de revisiones de](custom-action-patch-uninstall-option.md) acción personalizada para especificar que el instalador solo ejecute la acción personalizada cuando se desinstala una revisión.

**[Windows Installer 4.0 y versiones anteriores:](not-supported-in-windows-installer-4-0.md)**

La [opción Custom Action Patch Uninstall](custom-action-patch-uninstall-option.md) no está disponible. No hay ningún método [](custom-actions.md) para marcar una acción personalizada dentro de un paquete de revisión que se ejecute cuando se desinstale la revisión porque el instalador no aplica los paquetes de revisión que se están desinstalando.

Para que una [acción](custom-actions.md) personalizada se ejecute cuando se desinstala una revisión determinada, la acción personalizada debe estar presente en la aplicación original o estar en una revisión para el producto que siempre se aplica.

Los desarrolladores pueden usar la propiedad [**MsiPatchRemovalList**](msipatchremovallist.md) para crear un paquete de Windows Installer o una revisión que realice acciones [personalizadas](custom-actions.md) en la eliminación de una revisión. La acción personalizada se puede crear en el paquete de instalación original, una revisión que ya se ha aplicado al paquete o una revisión que no es una revisión [que se puede desinstalar.](uninstallable-patches.md) La acción personalizada se puede condicionalizar en la **propiedad MsiPatchRemovalList** en las tablas de secuencia. Vea [Using Properties in Conditional Statements (Uso](using-properties-in-conditional-statements.md) de propiedades en instrucciones condicionales) para obtener más información sobre las acciones de condicionalización.

La acción personalizada puede obtener los GUID de las revisiones que se quitan del valor de la [**propiedad MsiPatchRemovalList.**](msipatchremovallist.md) La acción personalizada puede determinar si el estado de instalación de la revisión se aplica, está obsoleto o se reemplaza llamando a [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) o a la propiedad [**PatchProperty**](patch-patchproperty.md) del [objeto Patch](patch-object.md).

Si la acción personalizada requiere metadatos especiales de la revisión, la revisión debe contener una acción personalizada que escriba los metadatos en un registro o una ubicación de archivo cuando se aplique la revisión. La acción personalizada en la aplicación original o una revisión que siempre se aplica puede obtener la información necesaria para quitar los cambios de la revisión.

Las revisiones que realicen cambios difíciles de deshacer correctamente no deben marcarse como revisiones [que se pueden desinstalar.](uninstallable-patches.md)

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

 

 




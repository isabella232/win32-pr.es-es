---
description: Utilice la siguiente marca de opción para especificar que el instalador ejecute la acción personalizada solo cuando se desinstale una revisión. Para establecer la opción, agregue el valor de esta tabla al valor del campo ExtendedType de la tabla CustomAction.
ms.assetid: aa4d9e21-5316-42b5-a22e-c7a5becd3cae
title: Opción de desinstalación de revisión de acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108365876393733f7cc520ae565bb2c5ea7ff3df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653063"
---
# <a name="custom-action-patch-uninstall-option"></a>Opción de desinstalación de revisión de acción personalizada

Utilice la siguiente marca de opción para especificar que el instalador ejecute la acción personalizada solo cuando se desinstale una revisión. Para establecer la opción, agregue el valor de esta tabla al valor del campo ExtendedType de la [tabla CustomAction](customaction-table.md).

**[Windows Installer 4,0 y versiones anteriores](not-supported-in-windows-installer-4-0.md):** No compatible. Esta opción está disponible a partir de Windows Installer 4,5.



| Constante                                | Hexadecimal | Decimal | Descripción                                                    |
|-----------------------------------------|-------------|---------|----------------------------------------------------------------|
| **msidbCustomActionTypePatchUninstall** | 0x8000      | 32 768   | La acción personalizada solo se ejecuta cuando se está desinstalando una revisión. |



 

## <a name="remarks"></a>Observaciones

Este atributo se puede Agregar a una acción personalizada mediante su creación en el paquete de Windows Installer (archivo. msi). Una revisión puede Agregar una nueva acción personalizada con este atributo. Una acción personalizada que tiene este atributo se puede actualizar mediante una revisión. Este atributo no se puede agregar ni quitar en una revisión para una acción personalizada existente.

Si una revisión agrega o actualiza una acción personalizada con este atributo, Windows Installer ejecutará la acción personalizada nueva o actualizada cuando se desinstale la revisión. Windows Installer hace que las actualizaciones de la revisión se desinstalen disponibles para la acción personalizada desinstalar revisión. La revisión debe incluir una [tabla *<PatchGUID>* MsiTransformView](msitransformview.md) para proporcionar esta información a Windows Installer.

Cuando un paquete que contiene una acción personalizada con el atributo **msidbCustomActionTypePatchUninstall** se instala con una versión de instalador anterior a Windows Installer 4,0, el instalador no llama a la acción personalizada cuando se desinstala la revisión. La instalación puede ejecutar la acción personalizada durante la instalación, reparación o actualización del paquete.

Las acciones personalizadas con el atributo **msidbCustomActionTypePatchUninstall** deben estar condicionadas mediante la propiedad [**MSIPATCHREMOVE**](msipatchremove.md) para evitar que la acción personalizada se ejecute al instalar, reparar o actualizar mediante un sistema con Windows Installer 4,0 o una versión anterior. Cuando se instala Windows Installer 4,5 y versiones posteriores, todas las revisiones del sistema que tienen acciones personalizadas marcadas con el atributo **msidbCustomActionTypePatchUninstall** ejecutan la acción personalizada durante la desinstalación de la revisión. Si se quita Windows Installer 4,5 o posterior del sistema, las revisiones pierden la funcionalidad de desinstalación de la revisión de acción personalizada.

Para obtener información sobre la ejecución de una acción personalizada durante la desinstalación de una revisión con una versión anterior a Windows Installer 4,5, vea [revisión de desinstalación de acciones personalizadas](patch-uninstall-custom-actions.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Opciones de ejecución de la acción personalizada In-Script](custom-action-in-script-execution-options.md)
</dt> <dt>

[Referencia de acción personalizada](custom-action-reference.md)
</dt> <dt>

[Acerca de las acciones personalizadas](about-custom-actions.md)
</dt> <dt>

[Uso de acciones personalizadas](using-custom-actions.md)
</dt> <dt>

[MsiTransformView *<PatchGUID>*](msitransformview.md)
</dt> </dl>

 

 




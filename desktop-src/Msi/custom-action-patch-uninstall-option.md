---
description: Use la marca de opción siguiente para especificar que el instalador ejecute la acción personalizada solo cuando se desinstale una revisión. Para establecer la opción, agregue el valor de esta tabla al valor del campo ExtendedType de la tabla CustomAction.
ms.assetid: aa4d9e21-5316-42b5-a22e-c7a5becd3cae
title: Opción de desinstalación de revisión de acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24636181ec8fb9695b9d959a25b055a7e7c21d34
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885038"
---
# <a name="custom-action-patch-uninstall-option"></a>Opción de desinstalación de revisión de acción personalizada

Use la marca de opción siguiente para especificar que el instalador ejecute la acción personalizada solo cuando se desinstale una revisión. Para establecer la opción , agregue el valor de esta tabla al valor del campo ExtendedType de la [tabla CustomAction](customaction-table.md).

**[Windows Installer 4.0 y versiones anteriores:](not-supported-in-windows-installer-4-0.md)** No se admite. Esta opción está disponible a partir de Windows Installer 4.5.



| Constante                                | Hexadecimal | Decimal | Descripción                                                    |
|-----------------------------------------|-------------|---------|----------------------------------------------------------------|
| **msidbCustomActionTypePatchUninstall** | 0x8000      | 32 768   | La acción personalizada solo se ejecuta cuando se desinstala una revisión. |



 

## <a name="remarks"></a>Comentarios

Este atributo se puede agregar a una acción personalizada mediante su creación en el paquete Windows instalador (.msi archivo). Una revisión puede agregar una nueva acción personalizada con este atributo. Una acción personalizada con este atributo se puede actualizar mediante una revisión. Este atributo no se puede agregar ni quitar mediante una revisión a una acción personalizada existente.

Si una revisión agrega o actualiza una acción personalizada con este atributo, Windows Installer ejecuta la acción personalizada nueva o actualizada cuando se desinstala la revisión. Windows El instalador hace que las actualizaciones dentro de la revisión que se va a desinstalar estén disponibles para la acción personalizada de desinstalación de revisiones. La revisión debe incluir [una tabla *&lt; PatchGUID &gt;* de MsiTransformView](msitransformview.md) para proporcionar esta información a Windows Instalador.

Cuando un paquete que contiene una acción personalizada con el atributo **msidbCustomActionTypePatchUninstall** se instala con una versión del instalador anterior a Windows Installer 4.0, el instalador no llama a la acción personalizada cuando se desinstala la revisión. La instalación puede ejecutar la acción personalizada durante la instalación, reparación o actualización del paquete.

Las acciones personalizadas con el atributo **msidbCustomActionTypePatchUninstall** deben estar condicióndas mediante la propiedad [**MSIPATCHREMOVE**](msipatchremove.md) para evitar que la acción personalizada se ejecute al instalar, reparar o actualizar mediante un sistema con Windows Installer 4.0 o versiones anteriores. Cuando se Windows Installer 4.5 y versiones posteriores, todas las revisiones del sistema que tienen acciones personalizadas marcadas con el atributo **msidbCustomActionTypePatchUninstall** ejecutan la acción personalizada durante la desinstalación de revisiones. Si Windows instalador 4.5 o posterior se quita del sistema, las revisiones perderán la funcionalidad de desinstalación de revisiones de acción personalizada.

Para obtener información sobre cómo ejecutar una acción personalizada durante la desinstalación de una revisión con una versión anterior a Windows Installer 4.5, vea Acciones personalizadas de desinstalación de [revisiones.](patch-uninstall-custom-actions.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Opciones de ejecución de In-Script acción personalizada](custom-action-in-script-execution-options.md)
</dt> <dt>

[Referencia de acción personalizada](custom-action-reference.md)
</dt> <dt>

[Acerca de las acciones personalizadas](about-custom-actions.md)
</dt> <dt>

[Uso de acciones personalizadas](using-custom-actions.md)
</dt> <dt>

[MsiTransformView *&lt; PatchGUID &gt;*](msitransformview.md)
</dt> </dl>

 

 




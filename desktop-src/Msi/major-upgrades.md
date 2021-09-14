---
description: Una actualización importante es una actualización completa de un producto que necesita un cambio de la propiedad ProductCode.
ms.assetid: 0c8f2aad-b301-4404-9051-694d97db1a8d
title: Actualizaciones principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7795695072f6c153373db914781ac4b919cd2572
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074413"
---
# <a name="major-upgrades"></a>Actualizaciones principales

Una actualización importante es una actualización completa de un producto que necesita un cambio de la [**propiedad ProductCode.**](productcode.md)

Una actualización principal típica quita una versión anterior de una aplicación e instala una nueva versión. Una actualización principal puede reorganizar el árbol de componentes de características. Para obtener más información, [**vea ProductCode**](productcode.md) y [Changing the Product Code](changing-the-product-code.md).

Durante una actualización importante mediante Windows Installer, el instalador busca en el equipo del usuario aplicaciones relacionadas con la actualización pendiente y, cuando detecta una, recupera la versión de la aplicación instalada del registro del sistema. A continuación, el instalador usa información de la base de datos de actualización para determinar si se debe actualizar la aplicación instalada.

Para habilitar las funcionalidades de actualización del instalador, cada paquete debe tener una [**propiedad UpgradeCode**](upgradecode.md) y una [tabla de actualización](upgrade-table.md). Cada producto independiente o conjunto de productos debe tener su propio **UpgradeCode.** Para obtener más información sobre el uso **de UpgradeCode,** consulte la sección [Using an UpgradeCode](using-an-upgradecode.md). Cada registro de la tabla Actualizar proporciona una combinación del código de actualización, la versión del producto y la información de idioma que se usa para identificar un conjunto de productos afectados por la actualización. Cuando [la acción FindRelatedProducts](findrelatedproducts-action.md) detecta que un producto afectado está instalado en el sistema, anexa el código de producto a una propiedad de la columna ActionProperty de la tabla Upgrade. La [acción RemoveExistingProducts](removeexistingproducts-action.md) y [la acción MigrateFeatureStates](migratefeaturestates-action.md) quitan o migran los productos enumerados en la lista ActionProperty. Los autores de paquetes también pueden seguir el procedimiento descrito en el tema: [Preparar una aplicación para futuras actualizaciones principales.](preparing-an-application-for-future-major-upgrades.md)

Windows Los paquetes de actualización del instalador se pueden crear de forma que las actualizaciones principales no se instalen si el usuario ya tiene instalada una versión más reciente de la aplicación. Para obtener más información sobre cómo crear un paquete que no se instalará en una versión más reciente, vea Impedir que un paquete antiguo se [instale en una versión más reciente.](preventing-an-old-package-from-installing-over-a-newer-version.md)

> [!Note]  
> Windows El instalador usa solo los tres primeros campos de la versión del producto. Consulte [**Propiedad ProductVersion**](productversion.md) para obtener descripciones de estos campos. Si incluye un cuarto campo en la versión del producto, el instalador omite el cuarto campo.

 

Método recomendado para aplicar una actualización principal mediante la instalación del paquete completo para el producto actualizado. Para obtener información sobre cómo aplicar una actualización principal mediante la instalación del [producto,](applying-major-upgrades-by-installing-the-product.md)vea Aplicar actualizaciones principales mediante la instalación del producto .

Una actualización principal aplicada como [paquete de](patch-packages.md) revisión para el producto no se puede secuenciar con otras actualizaciones y no es [una revisión que se pueda desinstalar.](uninstallable-patches.md) Para obtener información sobre cómo aplicar un paquete de revisión de actualización principal a un paquete del instalador de Windows, vea Aplicar actualizaciones principales mediante la aplicación de revisiones a la instalación [local del producto](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md). No se recomienda la aplicación de una actualización principal mediante un paquete de revisión; en su lugar, aplique las actualizaciones principales mediante la instalación del producto completo.

> [!Note]  
> Si se instala una aplicación en el contexto de instalación por usuario [,](installation-context.md)cualquier actualización principal de la aplicación también debe realizarse mediante el contexto por usuario. Si se instala una aplicación en el contexto de instalación por equipo, cualquier actualización principal de la aplicación también debe realizarse mediante el contexto por equipo. El Windows instalación no instalará actualizaciones importantes en el contexto de instalación.

 

Puede condición de acciones personalizadas que se secuencian después de [InstallValidate](installvalidate-action.md) para controlar las actualizaciones principales mediante la [**propiedad UPGRADINGPRODUCTCODE:**](upgradingproductcode.md)

-   Si desea que una acción personalizada se ejecute durante una desinstalación del producto, pero no durante la eliminación del producto mediante una actualización principal, use esta condición.

    REMOVE="ALL" Y NO [ **UPGRADINGPRODUCTCODE**](upgradingproductcode.md)

-   Si desea que una acción personalizada se ejecute solo durante una actualización principal, use esta condición.

    [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md)

 

 




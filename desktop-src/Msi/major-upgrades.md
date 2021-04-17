---
description: Una actualización principal es una actualización completa de un producto que necesita un cambio de la propiedad ProductCode.
ms.assetid: 0c8f2aad-b301-4404-9051-694d97db1a8d
title: Actualizaciones principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7795695072f6c153373db914781ac4b919cd2572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542734"
---
# <a name="major-upgrades"></a>Actualizaciones principales

Una actualización principal es una actualización completa de un producto que necesita un cambio de la propiedad [**ProductCode**](productcode.md) .

Una actualización importante típica quita una versión anterior de una aplicación e instala una nueva versión. Una actualización principal puede reorganizar el árbol de componentes de características. Para obtener más información, vea [**ProductCode**](productcode.md) y [cambiar el código de producto](changing-the-product-code.md).

Durante una actualización importante mediante Windows Installer, el instalador busca en el equipo del usuario las aplicaciones que están relacionadas con la actualización pendiente y, cuando detecta una, recupera la versión de la aplicación instalada del registro del sistema. A continuación, el instalador usa la información de la base de datos de actualización para determinar si se va a actualizar la aplicación instalada.

Para habilitar las funcionalidades de actualización del instalador, cada paquete debe tener una propiedad [**UpgradeCode**](upgradecode.md) y una [tabla de actualización](upgrade-table.md). Cada producto o conjunto de productos independiente debe tener su propio **UpgradeCode**. Para obtener más información sobre el uso de **UpgradeCode** , consulte la sección [uso de UpgradeCode](using-an-upgradecode.md). Cada registro de la tabla de actualización proporciona una combinación del código de actualización, la versión del producto y la información de idioma que se usa para identificar un conjunto de productos afectados por la actualización. Cuando la [acción FindRelatedProducts](findrelatedproducts-action.md) detecta que un producto afectado está instalado en el sistema, anexa el código de producto a una propiedad de la columna ActionProperty de la tabla de actualización. La [acción RemoveExistingProducts](removeexistingproducts-action.md) y la [acción MigrateFeatureStates](migratefeaturestates-action.md) quitan o migran los productos enumerados en la lista ActionProperty. Los autores de paquetes también pueden seguir el procedimiento descrito en el tema [preparación de una aplicación para futuras actualizaciones importantes](preparing-an-application-for-future-major-upgrades.md).

Windows Installer los paquetes de actualización se pueden crear de forma que las actualizaciones principales no se instalarán si el usuario ya tiene instalada una versión más reciente de la aplicación. Para obtener más información sobre cómo crear un paquete que no se instalará en una versión más reciente, vea impedir que se instale [un paquete antiguo en una versión más reciente](preventing-an-old-package-from-installing-over-a-newer-version.md) .

> [!Note]  
> Windows Installer solo utiliza los tres primeros campos de la versión del producto. Vea [**ProductVersion**](productversion.md) (propiedad) para obtener descripciones de estos campos. Si incluye un cuarto campo en la versión del producto, el instalador omite el cuarto campo.

 

El método recomendado para aplicar una actualización principal mediante la instalación del paquete completo para el producto actualizado. Para obtener información acerca de cómo aplicar una actualización principal mediante la instalación del producto, consulte [aplicar actualizaciones principales instalando el producto](applying-major-upgrades-by-installing-the-product.md).

Una actualización importante aplicada como [paquete de revisión](patch-packages.md) para el producto no se puede secuenciar con otras actualizaciones y no es una [revisión desinstalable](uninstallable-patches.md). Para obtener información acerca de cómo aplicar un paquete de revisión de actualización principal a un paquete de Windows Installer [, consulte aplicación de actualizaciones importantes mediante la revisión de la instalación local del producto](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md). No se recomienda la aplicación de una actualización principal mediante un paquete de revisión. en su lugar, aplique las actualizaciones principales instalando el producto completo.

> [!Note]  
> Si se instala una aplicación en el [contexto de instalación](installation-context.md)por usuario, también se debe realizar cualquier actualización importante a la aplicación mediante el contexto por usuario. Si se instala una aplicación en el contexto de instalación por equipo, también se debe realizar cualquier actualización importante a la aplicación mediante el contexto por equipo. En el Windows Installer no se instalarán las actualizaciones principales en el contexto de instalación.

 

Puede condicionar las acciones personalizadas que se secuencian después de [InstallValidate](installvalidate-action.md) para controlar las actualizaciones importantes mediante la propiedad [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) :

-   Si desea que una acción personalizada se ejecute durante la desinstalación del producto, pero no durante la eliminación del producto mediante una actualización principal, use esta condición.

    REMOVE = "ALL" y no [ **UPGRADINGPRODUCTCODE**](upgradingproductcode.md)

-   Si desea que una acción personalizada se ejecute solo durante una actualización principal, use esta condición.

    [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md)

 

 




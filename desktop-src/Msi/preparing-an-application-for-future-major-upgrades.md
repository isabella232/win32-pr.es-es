---
description: Los autores de los paquetes de instalación deben incluir la actualización de la información en sus archivos. msi para asegurarse de que el paquete de instalación puede aprovechar la funcionalidad de actualización completa disponible con el Microsoft Windows Installer.
ms.assetid: 88bb2709-a1bf-4140-a145-ae6bee85dde1
title: Preparación de una aplicación para futuras actualizaciones principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e0dc9ccbee10becc39274e91d2fedeb3707028
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652580"
---
# <a name="preparing-an-application-for-future-major-upgrades"></a>Preparación de una aplicación para futuras actualizaciones principales

Los autores de los paquetes de instalación deben incluir la actualización de la información en sus archivos. msi para asegurarse de que el paquete de instalación puede aprovechar la funcionalidad de actualización completa disponible con el Microsoft Windows Installer.

A todas las aplicaciones, o conjuntos de aplicaciones, se les debe asignar una propiedad [**UpgradeCode**](upgradecode.md) , la propiedad [**ProductVersion**](productversion.md) y la propiedad [**ProductLanguage**](productlanguage.md) . La propiedad [**UpgradeCode**](upgradecode.md) indica una familia de aplicaciones relacionadas que se componen de diferentes versiones y diferentes versiones de idioma del mismo producto. Para obtener más información sobre el uso de la propiedad [**UpgradeCode**](upgradecode.md) , vea [usar un UpgradeCode](using-an-upgradecode.md).

**Preparación de una aplicación para futuras actualizaciones principales**

1.  Determine un nuevo valor de código de paquete para la aplicación. Para obtener más información sobre los códigos de paquete, consulte [códigos de paquete](package-codes.md). Escriba el nuevo código de paquete en la propiedad [**Resumen del número de revisión**](revision-number-summary.md) de la secuencia de información de [Resumen](summary-information-stream.md).
2.  Determine una nueva propiedad [**ProductCode**](productcode.md) para la aplicación. Vea [cambiar el código de producto](changing-the-product-code.md) para obtener más información. Escriba [**ProductCode**](productcode.md) y su valor en la [tabla de propiedades](property-table.md).
3.  Determine la versión de la aplicación y la propiedad [**ProductVersion**](productversion.md) . El [**ProductVersion**](productversion.md) debe aumentar con cada nueva versión de la aplicación. Tenga en cuenta que el instalador solo usa los tres primeros campos de la versión del producto. Si incluye un cuarto campo en la versión del producto, el instalador omite el cuarto campo. Escriba [**ProductVersion**](productversion.md) y su valor en la tabla de propiedades.
4.  Determine el idioma del paquete y la propiedad [**ProductLanguage**](productlanguage.md) . El valor de esta propiedad debe ser un identificador de idioma numérico (LANGID). Escriba [**ProductLanguage**](productlanguage.md) y su valor en la [tabla de propiedades](property-table.md). Tenga en cuenta que la [acción FindRelatedProducts](findrelatedproducts-action.md) usa el lenguaje devuelto por [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa). Para que FindRelatedProducts funcione correctamente, el autor del paquete debe asegurarse de que la propiedad [**ProductLanguage**](productlanguage.md) esté establecida en la tabla de propiedades en un idioma que también aparezca en la propiedad Resumen de la [**plantilla**](template-summary.md) .
5.  Si va a crear un paquete de instalación para la primera versión del producto, use un nuevo [**UpgradeCode**](upgradecode.md). Si el paquete está destinado a una versión más reciente de un producto existente, o si es la misma versión que un producto existente en un idioma diferente, utilice el mismo [**UpgradeCode**](upgradecode.md) que el producto existente. No hay dos productos con el mismo [**ProductVersion**](productversion.md) y el mismo [**ProductLanguage**](productlanguage.md) puede tener el mismo [**UpgradeCode**](upgradecode.md), a menos que uno sea una [pequeña actualización](small-updates.md) del otro.
6.  [**UpgradeCode**](upgradecode.md) tiene el formato de un [GUID](guid.md). Escriba el GUID de [**UpgradeCode**](upgradecode.md) en la tabla de propiedades.

Para obtener más información, vea [impedir la instalación de un paquete antiguo en una versión más reciente](preventing-an-old-package-from-installing-over-a-newer-version.md).

 

 




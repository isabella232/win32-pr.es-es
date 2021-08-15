---
description: Los autores de paquetes de instalación deben incluir información de actualización en sus archivos .msi para asegurarse de que su paquete de instalación puede aprovechar la funcionalidad de actualización completa disponible con Microsoft Windows Installer.
ms.assetid: 88bb2709-a1bf-4140-a145-ae6bee85dde1
title: Preparación de una aplicación para futuras actualizaciones principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c38adc97fce578b48bc721b4265696486351097771cf936efc1e667752a7a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118377356"
---
# <a name="preparing-an-application-for-future-major-upgrades"></a>Preparación de una aplicación para futuras actualizaciones principales

Los autores de paquetes de instalación deben incluir información de actualización en sus archivos .msi para asegurarse de que su paquete de instalación puede aprovechar la funcionalidad de actualización completa disponible con Microsoft Windows Installer.

A cada aplicación, o conjunto de aplicaciones, se le debe asignar una [**propiedad UpgradeCode,**](upgradecode.md) [**una propiedad ProductVersion**](productversion.md) y [**una propiedad ProductLanguage.**](productlanguage.md) La [**propiedad UpgradeCode**](upgradecode.md) indica una familia de aplicaciones relacionadas que consta de diferentes versiones y versiones de idioma diferentes del mismo producto. Para obtener más información sobre el uso [**de la propiedad UpgradeCode,**](upgradecode.md) vea [Using an UpgradeCode](using-an-upgradecode.md).

**Preparación de una aplicación para futuras actualizaciones importantes**

1.  Determine un nuevo valor de código de paquete para la aplicación. Para obtener más información sobre los códigos de paquete, vea [Códigos de paquete .](package-codes.md) Escriba el nuevo código de paquete en la propiedad [**Resumen del**](revision-number-summary.md) número de revisión del flujo de información [de resumen](summary-information-stream.md).
2.  Determine una nueva [**propiedad ProductCode**](productcode.md) para la aplicación. Consulte [Cambio del código de producto](changing-the-product-code.md) para obtener más información. Escriba [**ProductCode y**](productcode.md) su valor en la [tabla Property](property-table.md).
3.  Determine la versión de la aplicación y la [**propiedad ProductVersion.**](productversion.md) [**ProductVersion debe**](productversion.md) aumentar con cada nueva versión de la aplicación. Tenga en cuenta que el instalador solo usa los tres primeros campos de la versión del producto. Si incluye un cuarto campo en la versión del producto, el instalador omite el cuarto campo. Escriba [**ProductVersion**](productversion.md) y su valor en la tabla Property.
4.  Determine el idioma del paquete y la [**propiedad ProductLanguage.**](productlanguage.md) El valor de esta propiedad debe ser un identificador de idioma numérico (LANGID). Escriba [**ProductLanguage y**](productlanguage.md) su valor en la [tabla Property](property-table.md). Tenga en cuenta [que la acción FindRelatedProducts](findrelatedproducts-action.md) usa el lenguaje devuelto [**por MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa). Para que FindRelatedProducts funcione correctamente, el autor del paquete debe asegurarse de que la propiedad [**ProductLanguage**](productlanguage.md) está establecida en la tabla Property en un idioma que también se muestra en la propiedad [**Resumen**](template-summary.md) de plantilla.
5.  Si va a crear un paquete de instalación para la primera versión del producto, use un [**nuevo upgradeCode**](upgradecode.md). Si el paquete está pensado para una versión más reciente de un producto existente o es la misma versión que un producto existente en un idioma diferente, use el mismo [**UpgradeCode**](upgradecode.md) que el producto existente. Ningún dos productos con el mismo [**ProductVersion**](productversion.md) y el mismo [**ProductLanguage**](productlanguage.md) pueden tener el mismo [**UpgradeCode**](upgradecode.md), a menos que uno sea una pequeña [actualización](small-updates.md) del otro.
6.  [**UpgradeCode**](upgradecode.md) tiene el formato de un [GUID.](guid.md) Escriba el GUID [**de UpgradeCode**](upgradecode.md) en la tabla Property.

Para obtener más información, vea [Preventing an Old Package from Installing Over a Newer Version](preventing-an-old-package-from-installing-over-a-newer-version.md).

 

 




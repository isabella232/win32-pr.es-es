---
description: Para usar las propiedades de la instalación, puede obtener y establecer los valores de propiedad de los programas mediante MsiGetProperty y MsiSetProperty e incluir como parte de las instrucciones condicionales en la base de datos de instalación.
ms.assetid: 65fe46d7-16b6-46ef-a440-73f954b03105
title: Obtener y establecer propiedades (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0154b84af656d295b9fa84ebcca881eab1c288f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910946"
---
# <a name="getting-and-setting-properties-windows-installer"></a>Obtener y establecer propiedades (Windows Installer)

Para usar [las propiedades](properties.md) de la instalación, puede obtener y establecer los valores de propiedad de los programas mediante [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) y [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) e incluir como parte de las instrucciones condicionales en la base de datos de instalación.

-   Para obtener una propiedad actual, llame a la función [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) .
-   Para obtener el estado de instalación actual, llame a la función [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) .
-   Para obtener el idioma de la instalación actual, llame a la función [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) .
-   Para establecer una propiedad, llame a la función [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) .
-   Para establecer el estado de la instalación, llame a la función [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode) .
-   Para borrar una propiedad (si se establece en null), establezca el valor de la propiedad en una cadena vacía: "".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Utilizar propiedades](using-properties.md)
</dt> <dt>

[Establecer valores de propiedades públicas en la línea de comandos](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[Borrar una propiedad del instalador](clearing-an-installer-property.md)
</dt> </dl>

 

 




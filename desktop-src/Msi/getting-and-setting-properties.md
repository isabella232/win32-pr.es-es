---
description: Para usar propiedades en la instalación, puede obtener y establecer valores de propiedad de programas mediante MsiGetProperty y MsiSetProperty e incluir como parte de instrucciones condicionales en la base de datos de instalación.
ms.assetid: 65fe46d7-16b6-46ef-a440-73f954b03105
title: Obtener y establecer propiedades (Windows instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0154b84af656d295b9fa84ebcca881eab1c288f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074729"
---
# <a name="getting-and-setting-properties-windows-installer"></a>Obtener y establecer propiedades (Windows instalador)

Para usar [propiedades](properties.md) en la instalación, puede obtener y establecer valores de propiedad de programas mediante [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) y [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) e incluir como parte de instrucciones condicionales en la base de datos de instalación.

-   Para obtener una propiedad actual, llame a la [**función MsiGetProperty.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)
-   Para obtener el estado de instalación actual, llame a [**la función MsiGetMode.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)
-   Para obtener el idioma de la instalación actual, llame a la [**función MsiGetLanguage.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage)
-   Para establecer una propiedad, llame a la [**función MsiSetProperty.**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)
-   Para establecer el estado de instalación, llame a [**la función MsiSetMode.**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode)
-   Para borrar una propiedad (establecerla en Null), establezca el valor de la propiedad en una cadena vacía: "".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Utilizar propiedades](using-properties.md)
</dt> <dt>

[Establecer valores de propiedad pública en la línea de comandos](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[Borrar una propiedad del instalador](clearing-an-installer-property.md)
</dt> </dl>

 

 




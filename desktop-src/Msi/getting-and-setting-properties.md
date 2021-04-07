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
# <a name="getting-and-setting-properties-windows-installer"></a><span data-ttu-id="4e47a-103">Obtener y establecer propiedades (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="4e47a-103">Getting and Setting Properties (Windows Installer)</span></span>

<span data-ttu-id="4e47a-104">Para usar [las propiedades](properties.md) de la instalación, puede obtener y establecer los valores de propiedad de los programas mediante [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) y [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) e incluir como parte de las instrucciones condicionales en la base de datos de instalación.</span><span class="sxs-lookup"><span data-stu-id="4e47a-104">To use [properties](properties.md) in your installation, you can get and set property values from programs using [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) and [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) and include as part of conditional statements in the installation database.</span></span>

-   <span data-ttu-id="4e47a-105">Para obtener una propiedad actual, llame a la función [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) .</span><span class="sxs-lookup"><span data-stu-id="4e47a-105">To obtain a current property, call the [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) function.</span></span>
-   <span data-ttu-id="4e47a-106">Para obtener el estado de instalación actual, llame a la función [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) .</span><span class="sxs-lookup"><span data-stu-id="4e47a-106">To obtain the current installation state, call the [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) function.</span></span>
-   <span data-ttu-id="4e47a-107">Para obtener el idioma de la instalación actual, llame a la función [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) .</span><span class="sxs-lookup"><span data-stu-id="4e47a-107">To obtain the language for the current installation, call the [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) function.</span></span>
-   <span data-ttu-id="4e47a-108">Para establecer una propiedad, llame a la función [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) .</span><span class="sxs-lookup"><span data-stu-id="4e47a-108">To set a property, call the [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) function.</span></span>
-   <span data-ttu-id="4e47a-109">Para establecer el estado de la instalación, llame a la función [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode) .</span><span class="sxs-lookup"><span data-stu-id="4e47a-109">To set the installation state, call the [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode) function.</span></span>
-   <span data-ttu-id="4e47a-110">Para borrar una propiedad (si se establece en null), establezca el valor de la propiedad en una cadena vacía: "".</span><span class="sxs-lookup"><span data-stu-id="4e47a-110">To clear a property (setting it to Null), set the property's value to an empty string: "".</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e47a-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4e47a-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e47a-112">Utilizar propiedades</span><span class="sxs-lookup"><span data-stu-id="4e47a-112">Using Properties</span></span>](using-properties.md)
</dt> <dt>

[<span data-ttu-id="4e47a-113">Establecer valores de propiedades públicas en la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="4e47a-113">Setting Public Property Values on the Command Line</span></span>](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[<span data-ttu-id="4e47a-114">Borrar una propiedad del instalador</span><span class="sxs-lookup"><span data-stu-id="4e47a-114">Clearing an Installer Property</span></span>](clearing-an-installer-property.md)
</dt> </dl>

 

 




---
description: El valor de la propiedad Resumen del número de revisión en el flujo de información de resumen se debe cambiar a un nuevo valor único al localizar una base de datos, porque la base de datos de instalación se está cambiando. Vea códigos de paquete.
ms.assetid: fce292c5-6702-4948-a13a-2a9ccacbd5c9
title: Actualizar una secuencia de información de Resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37c022023f79d8f4d3999db6e11e4cf65b73e1ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424040"
---
# <a name="updating-a-summary-information-stream"></a><span data-ttu-id="94b18-104">Actualizar una secuencia de información de Resumen</span><span class="sxs-lookup"><span data-stu-id="94b18-104">Updating a Summary Information Stream</span></span>

<span data-ttu-id="94b18-105">El valor de la propiedad [**Resumen del número de revisión**](revision-number-summary.md) en el flujo de información de [Resumen](summary-information-stream.md) se debe cambiar a un nuevo valor único al localizar una base de datos, porque la base de datos de instalación se está cambiando.</span><span class="sxs-lookup"><span data-stu-id="94b18-105">The value of the [**Revision Number Summary**](revision-number-summary.md) Property in the [summary information stream](summary-information-stream.md) must be changed to a new, unique value when localizing a database, because the installation database is being changed.</span></span> <span data-ttu-id="94b18-106">Vea [códigos de paquete](package-codes.md).</span><span class="sxs-lookup"><span data-stu-id="94b18-106">See [Package Codes](package-codes.md).</span></span>

<span data-ttu-id="94b18-107">El valor de la propiedad de [**Resumen de plantilla**](template-summary.md) en la secuencia de información de resumen se debe cambiar al identificador de idioma numérico (LANGID) del nuevo lenguaje.</span><span class="sxs-lookup"><span data-stu-id="94b18-107">The value of the [**Template Summary**](template-summary.md) Property in the summary information stream must be changed to the numeric language identifier (LANGID) of the new language.</span></span>

<span data-ttu-id="94b18-108">Si las cadenas de texto descriptivos de la secuencia de información de resumen se localizan en el nuevo idioma, la propiedad de Resumen de página de [**códigos**](codepage-summary.md) debe establecerse en la página de códigos correcta para el nuevo lenguaje.</span><span class="sxs-lookup"><span data-stu-id="94b18-108">If the descriptive text strings in the summary information stream are localized to the new language, the [**Codepage Summary**](codepage-summary.md) Property must be set to the correct code page for the new language.</span></span>

<span data-ttu-id="94b18-109">Puede modificar la secuencia de información de resumen del paquete localizado siguiendo el mismo procedimiento que en [Agregar información de Resumen](adding-summary-information.md).</span><span class="sxs-lookup"><span data-stu-id="94b18-109">You may modify the summary information stream of the localized package by the same procedure as in [Adding Summary Information](adding-summary-information.md).</span></span> <span data-ttu-id="94b18-110">También se proporciona un ejemplo en el que se muestra el uso de los métodos de información de Resumen de la base de datos en el SDK de Windows Installer como la utilidad WiSumInf.vbs.</span><span class="sxs-lookup"><span data-stu-id="94b18-110">An example demonstrating the use of the database summary information methods is also provided in the Windows Installer SDK as the utility WiSumInf.vbs.</span></span> <span data-ttu-id="94b18-111">Para obtener más información acerca de WiSumInf.vbs, vea [administrar información de Resumen](manage-summary-information.md).</span><span class="sxs-lookup"><span data-stu-id="94b18-111">For more information about WiSumInf.vbs, see [Manage Summary Information](manage-summary-information.md).</span></span>

[<span data-ttu-id="94b18-112">Continuar</span><span class="sxs-lookup"><span data-stu-id="94b18-112">Continue</span></span>](adding-localized-resources.md)

 

 




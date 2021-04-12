---
description: WMI implementa una técnica que permite almacenar varias versiones localizadas de la misma clase en el repositorio.
ms.assetid: 01e1cee5-d882-45b6-ac93-68533c2c6c9d
ms.tgt_platform: multiple
title: Localizar información de clase WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9f1a7e34c3ba230655ebba4c070981a8dab901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361278"
---
# <a name="localizing-wmi-class-information"></a><span data-ttu-id="b9e58-103">Localizar información de clase WMI</span><span class="sxs-lookup"><span data-stu-id="b9e58-103">Localizing WMI Class Information</span></span>

<span data-ttu-id="b9e58-104">WMI implementa una técnica que permite almacenar varias versiones localizadas de la misma clase en el repositorio.</span><span class="sxs-lookup"><span data-stu-id="b9e58-104">WMI implements a technique that allows multiple localized versions of the same class to be stored in the repository.</span></span>

<span data-ttu-id="b9e58-105">La definición de clase se divide en las siguientes versiones:</span><span class="sxs-lookup"><span data-stu-id="b9e58-105">The class definition is separated into the following versions:</span></span>

-   <span data-ttu-id="b9e58-106">Versión independiente del lenguaje que solo contiene una definición de clase básica.</span><span class="sxs-lookup"><span data-stu-id="b9e58-106">A language-neutral version that contains only a basic class definition.</span></span>
-   <span data-ttu-id="b9e58-107">Una versión específica del idioma que contiene información localizada, como descripciones de propiedades específicas de una configuración regional.</span><span class="sxs-lookup"><span data-stu-id="b9e58-107">A language-specific version that contains localized information, such as property descriptions that are specific to a locale.</span></span>

<span data-ttu-id="b9e58-108">Las definiciones de clase específicas del lenguaje se almacenan en un espacio de nombres secundario debajo del espacio de nombres que contiene una definición de clase básica independiente del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="b9e58-108">The language-specific class definitions are stored in a child namespace beneath the namespace that contains a language-neutral basic class definition.</span></span>

<span data-ttu-id="b9e58-109">Cuando se solicita una definición de clase localizada para una configuración regional específica, WMI combina la definición de clase básica y la información de clase localizada para formar una clase localizada completa.</span><span class="sxs-lookup"><span data-stu-id="b9e58-109">When you request a localized class definition for a specific locale, WMI combines the basic class definition and the localized class information to form a complete localized class.</span></span> <span data-ttu-id="b9e58-110">Puede obtener una versión localizada de una clase WMI si especifica una configuración regional cuando se conecta a WMI y establece una marca que indica que desea información localizada.</span><span class="sxs-lookup"><span data-stu-id="b9e58-110">You can get a localized version of a WMI class by specifying a locale when you connect to WMI and setting a flag that indicates that you want localized information.</span></span> <span data-ttu-id="b9e58-111">Después, WMI combina la información de la versión independiente del lenguaje y de las versiones específicas del lenguaje de la definición de clase para formar una clase localizada.</span><span class="sxs-lookup"><span data-stu-id="b9e58-111">WMI then merges the information from the language-neutral and the language-specific versions of the class definition to form a localized class.</span></span>

<span data-ttu-id="b9e58-112">Las clases WMI que contienen información localizada se marcan con el calificador de **modificación** y se denominan clases modificadas. una clase admite información localizada si tiene este calificador.</span><span class="sxs-lookup"><span data-stu-id="b9e58-112">WMI classes that contain localized information are marked with the **Amendment** qualifier and are called amended classes; a class supports localized information if it has this qualifier.</span></span> <span data-ttu-id="b9e58-113">Puede determinar la configuración regional para la que se ha localizado la clase comprobando otro calificador denominado [**configuración regional**](swbemobjectpath-locale.md).</span><span class="sxs-lookup"><span data-stu-id="b9e58-113">You can determine which locale the class has been localized for by checking for another qualifier called [**Locale**](swbemobjectpath-locale.md).</span></span> <span data-ttu-id="b9e58-114">El calificador de configuración regional contiene un identificador de localización (LCID de Windows) que identifica una configuración regional.</span><span class="sxs-lookup"><span data-stu-id="b9e58-114">The locale qualifier contains a localization identifier (Windows LCID) that identifies a locale.</span></span> <span data-ttu-id="b9e58-115">Por ejemplo, la configuración regional de inglés americano es 0xC0A.</span><span class="sxs-lookup"><span data-stu-id="b9e58-115">For example, the locale for American English is 0x409.</span></span> <span data-ttu-id="b9e58-116">Si un calificador de una clase modificada contiene información localizada, contiene el tipo de calificador **corregido** .</span><span class="sxs-lookup"><span data-stu-id="b9e58-116">If a qualifier in an amended class contains localized information, it contains the **amended** qualifier flavor.</span></span>

<span data-ttu-id="b9e58-117">La localización de WMI incluye las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="b9e58-117">WMI localization includes the following tasks:</span></span>

-   [<span data-ttu-id="b9e58-118">Crear definiciones de clase localizadas</span><span class="sxs-lookup"><span data-stu-id="b9e58-118">Creating localized class definitions</span></span>](creating-localized-class-definitions.md)
-   [<span data-ttu-id="b9e58-119">Compilar archivos MOF localizados</span><span class="sxs-lookup"><span data-stu-id="b9e58-119">Compiling localized MOF files</span></span>](compiling-localized-mof-files.md)
-   [<span data-ttu-id="b9e58-120">Localizar valores de propiedad</span><span class="sxs-lookup"><span data-stu-id="b9e58-120">Localizing property values</span></span>](localizing-property-values.md)
-   [<span data-ttu-id="b9e58-121">Recuperar clases modificadas</span><span class="sxs-lookup"><span data-stu-id="b9e58-121">Retrieving amended classes</span></span>](retrieving-amended-classes.md)

<span data-ttu-id="b9e58-122">Para obtener más información, vea Consideraciones de la [clase modificada](amended-class-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="b9e58-122">For more information, see [Amended Class Considerations](amended-class-considerations.md).</span></span>

 

 




---
description: Uso de datos de configuración regional persistentes
ms.assetid: f62402d6-31de-4ff7-9538-7925a007a089
title: Uso de datos de configuración regional persistentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4fe4990da53e4db9f71b2feffbd9eb40aedee9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913694"
---
# <a name="using-persistent-locale-data"></a><span data-ttu-id="78a5e-103">Uso de datos de configuración regional persistentes</span><span class="sxs-lookup"><span data-stu-id="78a5e-103">Using Persistent Locale Data</span></span>

<span data-ttu-id="78a5e-104">Una aplicación globalizada suele persistir o transmitir datos, por ejemplo, la hora y la fecha.</span><span class="sxs-lookup"><span data-stu-id="78a5e-104">A globalized application often persists or transmits data, for example, time and date.</span></span> <span data-ttu-id="78a5e-105">A la hora de decidir cómo debe controlar la aplicación la persistencia de los datos, recuerde que no se garantiza que los datos sean los mismos desde un equipo a otro o entre las ejecuciones de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="78a5e-105">When deciding how your application should handle data persistence, remember that data is not guaranteed to be the same from computer to computer or between runs of the application.</span></span> <span data-ttu-id="78a5e-106">Esto se aplica a las [configuraciones regionales](locales-and-languages.md) que se envían con Windows y a las [configuraciones regionales personalizadas](custom-locales.md).</span><span class="sxs-lookup"><span data-stu-id="78a5e-106">This is true for both [locales](locales-and-languages.md) that ship with Windows and [custom locales](custom-locales.md).</span></span>

<span data-ttu-id="78a5e-107">El diseño de la aplicación debe tener en cuenta una serie de cambios en los datos relacionados con la configuración regional que se pueden producir.</span><span class="sxs-lookup"><span data-stu-id="78a5e-107">Design of the application must take into account a variety of locale-related data changes that can occur.</span></span> <span data-ttu-id="78a5e-108">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="78a5e-108">For example:</span></span>

-   <span data-ttu-id="78a5e-109">Los símbolos de moneda pueden cambiar a medida que los países adoptan el euro.</span><span class="sxs-lookup"><span data-stu-id="78a5e-109">Currency symbols can change as countries adopt the Euro.</span></span>
-   <span data-ttu-id="78a5e-110">Las preferencias regionales pueden cambiar.</span><span class="sxs-lookup"><span data-stu-id="78a5e-110">Regional preferences can change.</span></span> <span data-ttu-id="78a5e-111">Por ejemplo, el formato d/m/y puede cambiar al formato m/d/y para una configuración regional determinada.</span><span class="sxs-lookup"><span data-stu-id="78a5e-111">For example, the format d/m/y might change to the format m/d/y for a particular locale.</span></span>
-   <span data-ttu-id="78a5e-112">La ortografía de los nombres de los días puede cambiar debido a las reformas de la ortografía.</span><span class="sxs-lookup"><span data-stu-id="78a5e-112">The spelling of day names can change due to spelling reforms.</span></span> <span data-ttu-id="78a5e-113">Además, el uso de mayúsculas y minúsculas puede cambiar para los nombres de mes o día.</span><span class="sxs-lookup"><span data-stu-id="78a5e-113">Additionally, casing can change for month or day names.</span></span>

## <a name="use-locale-independent-formats-for-storage-and-data-interchange"></a><span data-ttu-id="78a5e-114">Usar formatos de Locale-Independent para el almacenamiento y el intercambio de datos</span><span class="sxs-lookup"><span data-stu-id="78a5e-114">Use Locale-Independent Formats for Storage and Data Interchange</span></span>

<span data-ttu-id="78a5e-115">Una aplicación que conserva los datos debe usar formatos independientes de la configuración regional para el almacenamiento y el intercambio de datos.</span><span class="sxs-lookup"><span data-stu-id="78a5e-115">An application that persists data should use locale-independent formats for storage and data interchange.</span></span> <span data-ttu-id="78a5e-116">Algunos ejemplos son los formatos codificados de forma rígida o estándar. el [nombre de configuración regional de configuración \_ \_ ](locale-name-constants.md)regional invariable y los formatos de almacenamiento binario.</span><span class="sxs-lookup"><span data-stu-id="78a5e-116">Examples are hard-coded or standard formats; the invariant locale [LOCALE\_NAME\_INVARIANT](locale-name-constants.md); and binary storage formats.</span></span>

<span data-ttu-id="78a5e-117">Si se requieren datos de ordenación persistentes, la aplicación debe usar la función [**comparestringordinal (**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) .</span><span class="sxs-lookup"><span data-stu-id="78a5e-117">If persistent sorting data is required, the application must use the [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) function.</span></span> <span data-ttu-id="78a5e-118">Recuerde que un formato invariable no permanece invariable para la [ordenación](sorting.md), solo para los datos de la configuración regional y del calendario.</span><span class="sxs-lookup"><span data-stu-id="78a5e-118">Remember that an invariant format does not remain invariant for [sorting](sorting.md), only for locale and calendar data.</span></span>

## <a name="use-the-user-default-locale-for-data-presentation"></a><span data-ttu-id="78a5e-119">Usar la configuración regional predeterminada del usuario para la presentación de datos</span><span class="sxs-lookup"><span data-stu-id="78a5e-119">Use the User Default Locale for Data Presentation</span></span>

<span data-ttu-id="78a5e-120">Para presentar datos persistentes, lo mejor es que la aplicación vuelva a dar formato a los datos mediante la configuración regional predeterminada del usuario.</span><span class="sxs-lookup"><span data-stu-id="78a5e-120">To present persistent data, it is best for the application to reformat the data using the user default locale.</span></span> <span data-ttu-id="78a5e-121">El uso de esta configuración regional permite invalidaciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="78a5e-121">Use of this locale allows user overrides.</span></span> <span data-ttu-id="78a5e-122">Para obtener más información, vea [configuración \_ \_ predeterminada de usuario regional](locale-user-default.md).</span><span class="sxs-lookup"><span data-stu-id="78a5e-122">For more information, see [LOCALE\_USER\_DEFAULT](locale-user-default.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="78a5e-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="78a5e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78a5e-124">Uso de la compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="78a5e-124">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="78a5e-125">Configuraciones regionales personalizadas</span><span class="sxs-lookup"><span data-stu-id="78a5e-125">Custom Locales</span></span>](custom-locales.md)
</dt> <dt>

[<span data-ttu-id="78a5e-126">Ordenación</span><span class="sxs-lookup"><span data-stu-id="78a5e-126">Sorting</span></span>](sorting.md)
</dt> </dl>

 

 




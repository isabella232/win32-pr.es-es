---
description: En este tema se proporciona información general conceptual de la tecnología de interfaz de usuario multilingüe (MUI), la compatibilidad con la plataforma que proporciona para habilitar experiencias de usuario multilingües y las ventajas que ofrece el ecosistema de Windows.
ms.assetid: ef828da8-61cd-43d9-a5fe-e09a1f8af5c7
title: Información general sobre MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674cb5e0fee4e7b8d3990a99f13f981c4a8c5803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562469"
---
# <a name="overview-of-mui"></a><span data-ttu-id="214e9-103">Información general sobre MUI</span><span class="sxs-lookup"><span data-stu-id="214e9-103">Overview of MUI</span></span>

<span data-ttu-id="214e9-104">En este tema se proporciona información general conceptual de la tecnología de interfaz de usuario multilingüe (MUI), la compatibilidad con la plataforma que proporciona para habilitar experiencias de usuario multilingües y las ventajas que ofrece el ecosistema de Windows.</span><span class="sxs-lookup"><span data-stu-id="214e9-104">This topic provides a conceptual overview of the Multilingual User Interface (MUI) technology, the platform support it provides for enabling multilingual user experiences, and the benefits it offers to the Windows ecosystem.</span></span>

<span data-ttu-id="214e9-105">En esta página:</span><span class="sxs-lookup"><span data-stu-id="214e9-105">On this page:</span></span>

-   [<span data-ttu-id="214e9-106">La necesidad de la informática multilingüe</span><span class="sxs-lookup"><span data-stu-id="214e9-106">The need for multilingual computing</span></span>](#the-need-for-multilingual-computing)
-   [<span data-ttu-id="214e9-107">El rol de MUI en la habilitación de la informática multilingüe</span><span class="sxs-lookup"><span data-stu-id="214e9-107">The role of MUI in enabling multilingual computing</span></span>](#the-role-of-mui-in-enabling-multilingual-computing)
-   [<span data-ttu-id="214e9-108">Conceptos básicos de MUI</span><span class="sxs-lookup"><span data-stu-id="214e9-108">Core concepts of MUI</span></span>](#core-concepts-of-mui)
-   [<span data-ttu-id="214e9-109">Historial de MUI en Windows</span><span class="sxs-lookup"><span data-stu-id="214e9-109">History of MUI in Windows</span></span>](#history-of-mui-in-windows)
-   [<span data-ttu-id="214e9-110">Ventajas de la tecnología MUI</span><span class="sxs-lookup"><span data-stu-id="214e9-110">Benefits of MUI technology</span></span>](#benefits-of-mui-technology)

## <a name="the-need-for-multilingual-computing"></a><span data-ttu-id="214e9-111">La necesidad de la informática multilingüe</span><span class="sxs-lookup"><span data-stu-id="214e9-111">The need for multilingual computing</span></span>

<span data-ttu-id="214e9-112">Para beneficiarse de las oportunidades de crecimiento que presentan los mercados internacionales, las plataformas y las aplicaciones de Microsoft admiten más idiomas, culturas y mercados que nunca.</span><span class="sxs-lookup"><span data-stu-id="214e9-112">To benefit from the growth opportunities presented by international markets, Microsoft's platforms and applications support more languages, cultures and markets than ever before.</span></span>

<span data-ttu-id="214e9-113">Los detalles de idioma, referencia cultural y mercado siguen siendo extremadamente relevantes para los usuarios internacionales, a pesar de aumentar las tendencias de globalización.</span><span class="sxs-lookup"><span data-stu-id="214e9-113">Language, culture, and market specifics are still extremely relevant to international users, despite increasing globalization trends.</span></span> <span data-ttu-id="214e9-114">En el gráfico circular siguiente se muestra que los hablantes que no están en inglés todavía componen el 91,5 por ciento de la población del mundo.</span><span class="sxs-lookup"><span data-stu-id="214e9-114">The following pie chart shows that non-English speakers still make up 91.5 percent of the world's population.</span></span>

![gráfico circular con tres segmentos; la etiqueta "hablantes no inglesas 91,5%" es enormemente mayor que las otras dos combinadas](images/overview-of-mui-fig1.gif)

<span data-ttu-id="214e9-116">En todo el mundo, hay 193 países y más de 6.900 idiomas viviendo conocidos en uso hoy en día.</span><span class="sxs-lookup"><span data-stu-id="214e9-116">Worldwide, there are 193 countries and over 6,900 known living languages in use today.</span></span> <span data-ttu-id="214e9-117">En inglés, a pesar de su rol como lenguaje empresarial del mundo, solo se habla del 8,5% de la población del mundo como primer o segundo idioma.</span><span class="sxs-lookup"><span data-stu-id="214e9-117">English, despite its role as the world's business language, is only spoken by 8.5% of the world's population as a first or second language.</span></span> <span data-ttu-id="214e9-118">Para proporcionar información nativa al 94% de la población del mundo, esta información debe estar disponible en el 347 (aproximadamente un 5%). de los idiomas del mundo que tienen al menos un millón de oradores.</span><span class="sxs-lookup"><span data-stu-id="214e9-118">To provide native information to 94% of the world's population, this information would need to be available in the 347 (about 5%) of the world's languages that have at least a million speakers.</span></span> <span data-ttu-id="214e9-119">Esto es especialmente cierto cuando las tendencias de globalización han aumentado las expectativas de estos usuarios con respecto a la tecnología y su disponibilidad en sus mercados.</span><span class="sxs-lookup"><span data-stu-id="214e9-119">This is especially true as globalization trends have increased the expectations of these users regarding technology and its availability in their markets.</span></span>

<span data-ttu-id="214e9-120">La necesidad de localizar software en más idiomas ha aumentado a lo largo de los años y Microsoft ahora proporciona Windows Vista y otros productos en más idiomas que nunca.</span><span class="sxs-lookup"><span data-stu-id="214e9-120">The need to localize software in more languages has increased over the years and Microsoft is now providing Windows Vista and other products in more languages than ever.</span></span> <span data-ttu-id="214e9-121">Esta evolución está especialmente clara en Microsoft Windows, ya que ha pasado de admitir 30 idiomas con Windows 98 a casi 100 con Windows Vista, como se muestra en el siguiente gráfico de barras.</span><span class="sxs-lookup"><span data-stu-id="214e9-121">This evolution is especially clear with Microsoft Windows, as it has gone from supporting 30 languages with Windows 98 to almost 100 with Windows Vista, as illustrated in the following bar chart.</span></span>

![gráfico de barras que muestra que el número de idiomas es mucho mayor en Windows Vista que en Windows 98 o Windows XP](images/overview-of-mui-fig2.gif)

<span data-ttu-id="214e9-123">*Figura 2: número de idiomas admitidos por las versiones de Microsoft Windows*</span><span class="sxs-lookup"><span data-stu-id="214e9-123">*Figure 2—Number of languages supported by Microsoft Windows releases*</span></span>

## <a name="the-role-of-mui-in-enabling-multilingual-computing"></a><span data-ttu-id="214e9-124">El rol de MUI en la habilitación de la informática multilingüe</span><span class="sxs-lookup"><span data-stu-id="214e9-124">The role of MUI in enabling multilingual computing</span></span>

<span data-ttu-id="214e9-125">Como se explicó en la sección anterior, la [globalización](glossary-for-understanding-mui.md) y la [localización](glossary-for-understanding-mui.md) de las aplicaciones se han convertido en una necesidad en un mundo más globalmente integrado.</span><span class="sxs-lookup"><span data-stu-id="214e9-125">As discussed in the previous section, [globalization](glossary-for-understanding-mui.md) and [localization](glossary-for-understanding-mui.md) of applications have become a necessity in a more globally integrated world.</span></span> <span data-ttu-id="214e9-126">En concreto, a medida que más y más empresas van a ser globales, ya sea internamente o a través de sus redes empresariales, la necesidad de aplicaciones multilingües aumenta drásticamente.</span><span class="sxs-lookup"><span data-stu-id="214e9-126">In particular, as more and more enterprises are going global, either internally or through their business networks, the need for multi-lingual applications is increasing dramatically.</span></span> <span data-ttu-id="214e9-127">Por lo tanto, son los obstáculos en los que estas empresas se encuentran actualmente en la implementación global de estas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="214e9-127">So are the hurdles that these companies currently face in deploying these applications globally.</span></span>

<span data-ttu-id="214e9-128">Proporcionar compatibilidad con más idiomas para los sistemas operativos Windows, así como con aplicaciones de software compiladas para la plataforma Windows, requiere nuevas estrategias que permiten implementar todos los escenarios principales con una sobrecarga de ingeniería mínima.</span><span class="sxs-lookup"><span data-stu-id="214e9-128">Providing support for more languages for Windows operating systems, as well as software applications built for the Windows platform, requires new strategies which enable all major scenarios to be implemented with minimal engineering overhead.</span></span>

<span data-ttu-id="214e9-129">La tecnología MUI está destinada a desarrolladores y proveedores de software independientes que pretenden compilar y admitir aplicaciones multilingües para la plataforma Windows.</span><span class="sxs-lookup"><span data-stu-id="214e9-129">MUI technology is targeted at developers and ISVs aiming to build and support multilingual applications for the Windows platform.</span></span> <span data-ttu-id="214e9-130">MUI también es de importancia fundamental para los OEM y las empresas, que pueden aprovecharlo para implementar el sistema operativo Windows y agregar aplicaciones a los equipos en distintos idiomas a través de la implementación de una sola imagen.</span><span class="sxs-lookup"><span data-stu-id="214e9-130">MUI is also of key significance to OEMs and enterprises, who can leverage it to deploy the Windows operating system and add applications to computers across different languages through single image deployment.</span></span>

## <a name="core-concepts-of-mui"></a><span data-ttu-id="214e9-131">Conceptos básicos de MUI</span><span class="sxs-lookup"><span data-stu-id="214e9-131">Core concepts of MUI</span></span>

<span data-ttu-id="214e9-132">La idea fundamental que subyace a MUI es [separar el almacenamiento de recursos localizables del código fuente](mui-fundamental-concepts-explained.md)de la aplicación, de modo que pueda diseñar cualquier aplicación multilingüe como una combinación de un archivo binario principal independiente del lenguaje y un conjunto de archivos de recursos localizados específicos del idioma.</span><span class="sxs-lookup"><span data-stu-id="214e9-132">The fundamental idea behind MUI is to [separate the storage of localizable resources from application source code](mui-fundamental-concepts-explained.md), so as to be able to architect any multilingual application as a combination of a language-neutral core binary and a set of language-specific localized resource files.</span></span>

<span data-ttu-id="214e9-133">Una vez que el código fuente de la aplicación se almacena de forma independiente de los recursos localizados, es fácil [cargar dinámicamente los recursos localizados adecuados](mui-fundamental-concepts-explained.md) para un determinado contexto de la aplicación en función de una lógica que tenga en cuenta la configuración del sistema, el usuario y el nivel de aplicación para el idioma de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="214e9-133">Once application source code is stored separately from the localized resources, it becomes easy to [dynamically load the appropriate localized resources](mui-fundamental-concepts-explained.md) for a given application context based on a logic that takes into account system, user and application-level settings for the user interface language.</span></span>

<span data-ttu-id="214e9-134">Estos atributos fundamentales de MUI ayudan a facilitar escenarios empresariales como los siguientes:</span><span class="sxs-lookup"><span data-stu-id="214e9-134">These fundamental attributes of MUI help facilitate business scenarios such as:</span></span>

-   <span data-ttu-id="214e9-135">Un modelo de localización mejorado para la interfaz de usuario y el contenido de la ayuda, a través de la separación física del código fuente de la aplicación y los recursos localizables.</span><span class="sxs-lookup"><span data-stu-id="214e9-135">An improved localization model for user interface and help content, via the physical separation of application source code and localizable resources.</span></span>
-   <span data-ttu-id="214e9-136">Tratar los recursos localizables como contenido dinámico y cargarlos según la configuración del idioma de la interfaz de usuario y las preferencias de reserva.</span><span class="sxs-lookup"><span data-stu-id="214e9-136">Treating the localizable resources as dynamic content and loading them according to the UI language settings and fallback preferences.</span></span> <span data-ttu-id="214e9-137">Esto permite escenarios como los siguientes:</span><span class="sxs-lookup"><span data-stu-id="214e9-137">This enables scenarios such as:</span></span>
    -   <span data-ttu-id="214e9-138">Cambiar de un idioma de interfaz de usuario a otro en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="214e9-138">Switching from one UI language to another one at run-time.</span></span>
    -   <span data-ttu-id="214e9-139">Crear imágenes de implementación única regional o internacional que cubran un conjunto de idiomas para OEM y empresas.</span><span class="sxs-lookup"><span data-stu-id="214e9-139">Creating regional or worldwide single deployment images that cover a set of languages for OEMs and enterprises.</span></span>

## <a name="history-of-mui-in-windows"></a><span data-ttu-id="214e9-140">Historial de MUI en Windows</span><span class="sxs-lookup"><span data-stu-id="214e9-140">History of MUI in Windows</span></span>

<span data-ttu-id="214e9-141">El nivel de soporte técnico disponible para una experiencia de usuario multilingüe en el nivel del sistema operativo Windows y para el desarrollo de aplicaciones multilingües en la plataforma Windows ha evolucionado a lo largo del tiempo y a través de las diferentes versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="214e9-141">The level of support available for a multilingual user experience at the Windows operating system level and for multilingual application development on the Windows platform has evolved over time and across the different versions of Windows.</span></span>

<span data-ttu-id="214e9-142">La funcionalidad admitida antes de que [Windows Vista](evolution-of-mui-support-across-windows-versions.md) era bastante básica, con imágenes de Windows de un solo idioma y una opción para agregar paquetes de interfaz de usuario multilingüe en escenarios específicos.</span><span class="sxs-lookup"><span data-stu-id="214e9-142">The supported functionality [before Windows Vista](evolution-of-mui-support-across-windows-versions.md) was fairly basic, with single-language Windows images and an option to add-on Multilingual User Interface Packs in specific scenarios.</span></span> <span data-ttu-id="214e9-143">No hay compatibilidad para desarrolladores de aplicaciones multilingües.</span><span class="sxs-lookup"><span data-stu-id="214e9-143">No developer support for multilingual applications was available.</span></span>

<span data-ttu-id="214e9-144">[Con Windows Vista](evolution-of-mui-support-across-windows-versions.md), Microsoft ha realizado una inversión significativa en mui y Windows Vista se ha creado desde el principio en una plataforma MUI.</span><span class="sxs-lookup"><span data-stu-id="214e9-144">[With Windows Vista](evolution-of-mui-support-across-windows-versions.md), Microsoft made a significant investment in MUI, and Windows Vista is built from the ground up on a MUI platform.</span></span> <span data-ttu-id="214e9-145">Aunque esto representa un avance importante en la estrategia de localización de Windows, ya que es un componente clave para que Microsoft proporcione Windows en más idiomas que nunca, es primero y más importante para los usuarios, desarrolladores y clientes de Windows.</span><span class="sxs-lookup"><span data-stu-id="214e9-145">While this represents a major advance in Windows localization strategy, as it is a key enabler for Microsoft to provide Windows in more languages than ever before, it is first and foremost a great advance for Windows users, developers, and customers.</span></span> <span data-ttu-id="214e9-146">Proporciona varias ventajas principales como las siguientes:</span><span class="sxs-lookup"><span data-stu-id="214e9-146">It provides several major benefits such as:</span></span>

-   <span data-ttu-id="214e9-147">Un sistema operativo independiente del lenguaje con compatibilidad integrada con MUI.</span><span class="sxs-lookup"><span data-stu-id="214e9-147">A language-neutral operating system with built-in support for MUI.</span></span>
-   <span data-ttu-id="214e9-148">Empaquetado, implementación e instalación configurables para admitir escenarios multilingües.</span><span class="sxs-lookup"><span data-stu-id="214e9-148">Configurable packaging, deployment, and installation to support multilingual scenarios.</span></span>
-   <span data-ttu-id="214e9-149">Implementación de una sola imagen con varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="214e9-149">Single-image deployment with multiple languages.</span></span>
-   <span data-ttu-id="214e9-150">Modelo de servicio mejorado en el que el código ejecutable se puede actualizar independientemente de los recursos.</span><span class="sxs-lookup"><span data-stu-id="214e9-150">An improved servicing model where the executable code can be updated independently of the resources.</span></span>
-   <span data-ttu-id="214e9-151">Compatibilidad del desarrollador con la creación de aplicaciones multilingües.</span><span class="sxs-lookup"><span data-stu-id="214e9-151">Developer support for building multilingual applications.</span></span>

<span data-ttu-id="214e9-152">En la tabla siguiente se proporciona información general detallada sobre la compatibilidad de la plataforma Windows con MUI:</span><span class="sxs-lookup"><span data-stu-id="214e9-152">The following table provides a detailed overview of the Windows platform support for MUI:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="214e9-153">Category</span><span class="sxs-lookup"><span data-stu-id="214e9-153">Category</span></span></th>
<th><span data-ttu-id="214e9-154">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="214e9-154">Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="214e9-155">Versiones admitidas de Windows (solo compatibilidad con sistema operativo)</span><span class="sxs-lookup"><span data-stu-id="214e9-155">Supported Windows versions (OS support only)</span></span></td>
<td><ul>
<li><span data-ttu-id="214e9-156">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="214e9-156">Windows 2000 Professional</span></span></li>
<li><span data-ttu-id="214e9-157">Familia de servidores de Windows 2000</span><span class="sxs-lookup"><span data-stu-id="214e9-157">Windows 2000 Server family</span></span></li>
<li><span data-ttu-id="214e9-158">Windows XP Professional</span><span class="sxs-lookup"><span data-stu-id="214e9-158">Windows XP Professional</span></span></li>
<li><span data-ttu-id="214e9-159">Windows XP Tablet PC Edition</span><span class="sxs-lookup"><span data-stu-id="214e9-159">Windows XP Tablet PC Edition</span></span></li>
<li><span data-ttu-id="214e9-160">Familia de Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="214e9-160">Windows Server 2003 family</span></span></li>
<li><span data-ttu-id="214e9-161">Windows XP Embedded</span><span class="sxs-lookup"><span data-stu-id="214e9-161">Windows XP Embedded</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="214e9-162">Versiones admitidas de Windows (compatibilidad con aplicaciones de SO &)</span><span class="sxs-lookup"><span data-stu-id="214e9-162">Supported Windows versions (OS & application support)</span></span></td>
<td><ul>
<li><span data-ttu-id="214e9-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="214e9-163">Windows Vista</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="214e9-164">Versiones no admitidas de Windows</span><span class="sxs-lookup"><span data-stu-id="214e9-164">Unsupported Windows versions</span></span></td>
<td><ul>
<li><span data-ttu-id="214e9-165">Windows 9x</span><span class="sxs-lookup"><span data-stu-id="214e9-165">Windows 9x</span></span></li>
<li><span data-ttu-id="214e9-166">Windows me</span><span class="sxs-lookup"><span data-stu-id="214e9-166">Windows Me</span></span></li>
<li><span data-ttu-id="214e9-167">Windows XP Home Edition</span><span class="sxs-lookup"><span data-stu-id="214e9-167">Windows XP Home Edition</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="benefits-of-mui-technology"></a><span data-ttu-id="214e9-168">Ventajas de la tecnología MUI</span><span class="sxs-lookup"><span data-stu-id="214e9-168">Benefits of MUI technology</span></span>

<span data-ttu-id="214e9-169">MUI tiene un efecto positivo en varios aspectos del ecosistema de Windows:</span><span class="sxs-lookup"><span data-stu-id="214e9-169">MUI positively impacts multiple aspects of the Windows ecosystem:</span></span>

-   <span data-ttu-id="214e9-170">[Ventajas para los desarrolladores](benefits-of-mui-explained.md): se ofrecen numerosas ventajas a los desarrolladores de aplicaciones por la disponibilidad de la compatibilidad de la API de MUI para compilar aplicaciones multilingües modeladas en los mismos principios que la compatibilidad multilingüe en el propio sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="214e9-170">[Benefits for Developers](benefits-of-mui-explained.md): Numerous benefits are offered to application developers by the availability of MUI API support to build multilingual applications modeled on the same principles as the multilingual support in the core Windows operating system itself.</span></span> <span data-ttu-id="214e9-171">Entre las ventajas se incluye lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="214e9-171">These benefits include:</span></span>
    -   <span data-ttu-id="214e9-172">La capacidad de proporcionar una experiencia de visualización de lenguaje que sea coherente con la que ofrece el propio sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="214e9-172">The ability to provide a display language experience that is consistent with what the operating system itself offers.</span></span>
    -   <span data-ttu-id="214e9-173">La capacidad de ampliar fácilmente la compatibilidad de idioma para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="214e9-173">The ability to easily extend the language support for an application.</span></span>
    -   <span data-ttu-id="214e9-174">La capacidad de mantener y atender la aplicación fácilmente.</span><span class="sxs-lookup"><span data-stu-id="214e9-174">The ability to easily maintain and service the application.</span></span>
    -   <span data-ttu-id="214e9-175">La capacidad de habilitar la implementación de una sola imagen de las aplicaciones por parte de los OEM.</span><span class="sxs-lookup"><span data-stu-id="214e9-175">The ability to enable single-image deployment of applications by OEMs.</span></span>
-   <span data-ttu-id="214e9-176">[Ventajas para empresas](benefits-of-mui-explained.md): la principal ventaja que ofrece MUI para empresas es la capacidad de implementar, respaldar y mantener la misma imagen multilingüe en todo el mundo con una única instalación.</span><span class="sxs-lookup"><span data-stu-id="214e9-176">[Benefits for Enterprises](benefits-of-mui-explained.md): The major benefit that MUI offers for enterprises is the ability to roll out, support, and maintain the same multilingual image worldwide with a single installation.</span></span> <span data-ttu-id="214e9-177">Otro logro importante es la capacidad de admitir escritorios multilingües que ofrecen una interacción sin problemas a los usuarios con diferentes preferencias de idioma.</span><span class="sxs-lookup"><span data-stu-id="214e9-177">Another significant win is the ability to support multilingual desktops that offer seamless interaction to users with different language preferences.</span></span>
-   <span data-ttu-id="214e9-178">[Ventajas para los OEM](benefits-of-mui-explained.md): la principal ventaja para los OEM es la instalación de imagen única que mui habilita, con compatibilidad para varios idiomas, lo que permite una administración más eficaz del inventario.</span><span class="sxs-lookup"><span data-stu-id="214e9-178">[Benefits for OEMs](benefits-of-mui-explained.md): The major benefit for OEMs is the single image installation that MUI enables, with support for multiple languages, which enables a more effective management of inventory.</span></span> <span data-ttu-id="214e9-179">Los OEM también se benefician de la compatibilidad de MUI con el desarrollo de aplicaciones, ya que les permite proporcionar aplicaciones de valor agregado en sus imágenes mientras se benefician de la instalación de una sola imagen, siempre y cuando estas aplicaciones estén habilitadas para MUI.</span><span class="sxs-lookup"><span data-stu-id="214e9-179">OEMs also benefit from the MUI support for application development, as it enables them to provide value-add applications on their images while benefiting from the single image installation, as long as these applications are MUI-enabled.</span></span>

 

 





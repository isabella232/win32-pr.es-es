---
title: Compatibilidad con temas de contraste alto
description: En este tema se compara la compatibilidad con los temas de contraste alto de Windows 8 con la de versiones anteriores de Windows y se explica cómo se admiten los temas de contraste alto en una aplicación de Windows 8.
ms.assetid: 6E4F1198-E69C-4C60-B3B0-2702AECAA203
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2068d64b585f302f578296c9e156895c23b9bce9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904839"
---
# <a name="supporting-high-contrast-themes"></a><span data-ttu-id="467a9-103">Compatibilidad con temas de contraste alto</span><span class="sxs-lookup"><span data-stu-id="467a9-103">Supporting High Contrast Themes</span></span>

<span data-ttu-id="467a9-104">En este tema se compara la compatibilidad con los temas de contraste alto de Windows 8 con la de versiones anteriores de Windows y se explica cómo se admiten los temas de contraste alto en una aplicación de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="467a9-104">This topic compares the support for high contrast themes in Windows 8 to that of previous versions of Windows, and explains how to support high contrast themes in a Windows 8 application.</span></span>

<span data-ttu-id="467a9-105">Incluye las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="467a9-105">It includes the following sections.</span></span>

-   [<span data-ttu-id="467a9-106">Información general de la compatibilidad con temas de contraste alto</span><span class="sxs-lookup"><span data-stu-id="467a9-106">Overview of Support for High Contrast Themes</span></span>](#overview-of-support-for-high-contrast-themes)
-   [<span data-ttu-id="467a9-107">Compatibilidad con temas de contraste alto en Windows 8 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="467a9-107">Supporting High Contrast Themes in Windows 8 and later</span></span>](#supporting-high-contrast-themes-in-windows-8-and-later)
-   [<span data-ttu-id="467a9-108">Agregar una sección de compatibilidad al manifiesto de aplicación</span><span class="sxs-lookup"><span data-stu-id="467a9-108">Adding a Compatibility Section to Your Application Manifest</span></span>](#adding-a-compatibility-section-to-your-application-manifest)
-   [<span data-ttu-id="467a9-109">Detección de contraste alto en versiones anteriores de Windows</span><span class="sxs-lookup"><span data-stu-id="467a9-109">Detecting High Contrast in Previous Versions of Windows</span></span>](#detecting-high-contrast-in-previous-versions-of-windows)
-   [<span data-ttu-id="467a9-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="467a9-110">Related topics</span></span>](#related-topics)

## <a name="overview-of-support-for-high-contrast-themes"></a><span data-ttu-id="467a9-111">Información general de la compatibilidad con temas de contraste alto</span><span class="sxs-lookup"><span data-stu-id="467a9-111">Overview of Support for High Contrast Themes</span></span>

<span data-ttu-id="467a9-112">Windows 7 y versiones anteriores admiten dos modelos de ti, incluido el modelo clásico de Windows heredado y los estilos visuales actuales.</span><span class="sxs-lookup"><span data-stu-id="467a9-112">Windows 7 and earlier support two theming models, including the legacy Windows classic model, and the current visual styles.</span></span> <span data-ttu-id="467a9-113">El modelo clásico de Windows se ha mantenido a través de Windows 7 principalmente para admitir los diversos temas de contraste alto.</span><span class="sxs-lookup"><span data-stu-id="467a9-113">The Windows classic model has been retained through Windows 7 mainly to support the various high contrast themes.</span></span> <span data-ttu-id="467a9-114">Sin embargo, el modelo clásico de Windows tiene varias desventajas:</span><span class="sxs-lookup"><span data-stu-id="467a9-114">However, the Windows classic model has a number of drawbacks:</span></span>

-   <span data-ttu-id="467a9-115">No se admiten temas que usan estilos visuales, como Windows Aero.</span><span class="sxs-lookup"><span data-stu-id="467a9-115">No support for themes that use visual styles, such as Windows Aero.</span></span> <span data-ttu-id="467a9-116">Los usuarios de los temas de contraste alto deben usar la interfaz de usuario clásica de Windows.</span><span class="sxs-lookup"><span data-stu-id="467a9-116">Users of high contrast themes must use the Windows classic UI.</span></span>
-   <span data-ttu-id="467a9-117">No se admiten las características de la interfaz de usuario que se basan en Administrador de ventanas de escritorio (DWM) para ejecutarse, como las vistas previas en miniatura y el ampliador de pantalla completa que se presentó en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="467a9-117">No support for UI features that rely on Desktop Window Manager (DWM) to run, such as thumbnail previews and the full screen magnifier that was introduced in Windows 7.</span></span>
-   <span data-ttu-id="467a9-118">Los desarrolladores deben mantener dos rutas de acceso de código independientes para admitir los dos modelos de cada una de ellas.</span><span class="sxs-lookup"><span data-stu-id="467a9-118">Developers must maintain two separate code paths to support the two different theming models.</span></span>

<span data-ttu-id="467a9-119">En Windows 8 y versiones posteriores, los siguientes cambios en el modelo de los procedimientos abordan los inconvenientes anteriores:</span><span class="sxs-lookup"><span data-stu-id="467a9-119">In Windows 8 and later, the following changes to the theming model address the previous drawbacks:</span></span>

-   <span data-ttu-id="467a9-120">Ya no se admite el modelo de ti clásico de Windows, lo que permite a los desarrolladores mantener solo una ruta de acceso al código para las aplicaciones destinadas solo a Windows 8.</span><span class="sxs-lookup"><span data-stu-id="467a9-120">The Windows classic theming model is no longer supported, enabling developers to maintain just one code path for applications that target only Windows 8.</span></span>
-   <span data-ttu-id="467a9-121">Dado que los estilos visuales y DWM están activados en Windows 8, los usuarios de alto contraste tienen acceso a características como las vistas previas de miniaturas y el ampliador de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="467a9-121">Because visual styles and DWM are on in Windows 8, high contrast users have access to features such as thumbnail previews and the full-screen magnifier.</span></span>
-   <span data-ttu-id="467a9-122">Los estilos visuales admiten la configuración de los colores de varios elementos de la interfaz de usuario, lo que permite a los usuarios de contraste alto personalizar la interfaz de usuario para adaptarse a las necesidades y preferencias individuales.</span><span class="sxs-lookup"><span data-stu-id="467a9-122">Visual styles support setting the colors of various UI elements, enabling high contrast users to customize the UI to accommodate individual needs and preferences.</span></span>
-   <span data-ttu-id="467a9-123">Windows 8 incluye compatibilidad con las aplicaciones existentes que están diseñadas para usar temas de contraste alto basados en el modelo de temas clásicos de Windows.</span><span class="sxs-lookup"><span data-stu-id="467a9-123">Windows 8 includes compatibility support for existing applications that are designed to use high contrast themes based on the Windows classic theming model.</span></span>

## <a name="supporting-high-contrast-themes-in-windows-8-and-later"></a><span data-ttu-id="467a9-124">Compatibilidad con temas de contraste alto en Windows 8 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="467a9-124">Supporting High Contrast Themes in Windows 8 and later</span></span>

<span data-ttu-id="467a9-125">En Windows 8, dado que los estilos visuales están activados en el modo de contraste alto, la compatibilidad con los temas de contraste alto es sencilla siempre y cuando se tengan en cuentan las siguientes directrices.</span><span class="sxs-lookup"><span data-stu-id="467a9-125">In Windows 8, because visual styles are on in high contrast mode, supporting high contrast themes is straightforward as long as you heed the following guidelines.</span></span>

-   <span data-ttu-id="467a9-126">Tamaños de fuente y control.</span><span class="sxs-lookup"><span data-stu-id="467a9-126">Font and control sizes.</span></span> <span data-ttu-id="467a9-127">Para asegurarse de que la interfaz de usuario es accesible para los usuarios con discapacidades, establezca tamaños de fuente según la configuración de tema actual.</span><span class="sxs-lookup"><span data-stu-id="467a9-127">To ensure that your UI is accessible to users with disabilities, set font sizes according to the current theme settings.</span></span> <span data-ttu-id="467a9-128">Establezca el tamaño de los controles para que sea al menos el tamaño predeterminado.</span><span class="sxs-lookup"><span data-stu-id="467a9-128">Set the size of controls to be at least the default size.</span></span>
-   <span data-ttu-id="467a9-129">Colorea.</span><span class="sxs-lookup"><span data-stu-id="467a9-129">Colors.</span></span> <span data-ttu-id="467a9-130">Evite el uso de colores codificados de forma rígida.</span><span class="sxs-lookup"><span data-stu-id="467a9-130">Avoid using hard-coded colors.</span></span> <span data-ttu-id="467a9-131">En su lugar, use los colores del sistema porque se basan en el tema actual.</span><span class="sxs-lookup"><span data-stu-id="467a9-131">Instead, use the system colors because they are based on the current theme.</span></span> <span data-ttu-id="467a9-132">El uso de colores personalizados puede interferir con los colores de los temas de contraste alto y reemplazarlos.</span><span class="sxs-lookup"><span data-stu-id="467a9-132">Using custom colors can interfere with and override the colors in the high contrast themes.</span></span>
-   <span data-ttu-id="467a9-133">Manifiesto de aplicación.</span><span class="sxs-lookup"><span data-stu-id="467a9-133">Application manifest.</span></span> <span data-ttu-id="467a9-134">Las aplicaciones diseñadas para trabajar con los nuevos temas de contraste alto deben tener definida una sección de compatibilidad de aplicaciones en su manifiesto que contenga los GUID de compatibilidad de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="467a9-134">Applications designed to work with the new high contrast themes should have an application compatibility section defined in their manifest that contains the Windows 8 compatibility GUIDs.</span></span> <span data-ttu-id="467a9-135">De lo contrario, Windows supone que la aplicación está diseñada para una versión anterior de Windows y representa la interfaz de usuario de la aplicación mediante la simulación del modelo de los Windows clásico.</span><span class="sxs-lookup"><span data-stu-id="467a9-135">Otherwise, Windows assumes that the application is designed for an older version of Windows and renders the application UI by simulating the Windows classic theming model.</span></span>

## <a name="adding-a-compatibility-section-to-your-application-manifest"></a><span data-ttu-id="467a9-136">Agregar una sección de compatibilidad al manifiesto de aplicación</span><span class="sxs-lookup"><span data-stu-id="467a9-136">Adding a Compatibility Section to Your Application Manifest</span></span>

<span data-ttu-id="467a9-137">Un manifiesto de aplicación es un archivo XML que describe los requisitos de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="467a9-137">An application manifest is an XML file that describes the requirements for an application.</span></span> <span data-ttu-id="467a9-138">La sección de compatibilidad del manifiesto identifica las versiones de Windows compatibles con la aplicación.</span><span class="sxs-lookup"><span data-stu-id="467a9-138">The compatibility section of the manifest identifies the versions of Windows supported by the application.</span></span> <span data-ttu-id="467a9-139">En la sección compatibilidad se usan los siguientes GUID para identificar las distintas versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="467a9-139">The following GUIDs are used in the compatibility section to identify the various versions of Windows.</span></span>

| <span data-ttu-id="467a9-140">Versión</span><span class="sxs-lookup"><span data-stu-id="467a9-140">Version</span></span>       | <span data-ttu-id="467a9-141">GUID</span><span class="sxs-lookup"><span data-stu-id="467a9-141">GUID</span></span>                                   |
|---------------|----------------------------------------|
| <span data-ttu-id="467a9-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="467a9-142">Windows Vista</span></span> | <span data-ttu-id="467a9-143">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span><span class="sxs-lookup"><span data-stu-id="467a9-143">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span></span> |
| <span data-ttu-id="467a9-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="467a9-144">Windows 7</span></span>     | <span data-ttu-id="467a9-145">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span><span class="sxs-lookup"><span data-stu-id="467a9-145">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span></span> |
| <span data-ttu-id="467a9-146">Windows 8</span><span class="sxs-lookup"><span data-stu-id="467a9-146">Windows 8</span></span>     | <span data-ttu-id="467a9-147">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span><span class="sxs-lookup"><span data-stu-id="467a9-147">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span></span> |



 

<span data-ttu-id="467a9-148">La sección de compatibilidad puede especificar varias versiones de Windows, pero cada una debe estar contenida dentro de su propia `<supportedOS/>` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="467a9-148">The compatibility section can specify multiple versions of Windows, but each must be contained within its own `<supportedOS/>` tag.</span></span> <span data-ttu-id="467a9-149">En el ejemplo siguiente se muestra un manifiesto de aplicación que especifica Windows 7 y Windows 8 en la sección de compatibilidad:</span><span class="sxs-lookup"><span data-stu-id="467a9-149">The following example shows an application manifest that specifies Windows 7 and Windows 8 in the compatibility section:</span></span>


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!--The ID below indicates application support for Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>

            <!--The ID below indicates application support for Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        </application>
    </compatibility>
</assembly>
```



<span data-ttu-id="467a9-150">Si una aplicación no tiene un manifiesto de compatibilidad, se supone que es una aplicación de Windows Vista y no usa controles con temas en el área cliente cuando está activo un tema de contraste alto.</span><span class="sxs-lookup"><span data-stu-id="467a9-150">If an application does not have a compatibility manifest, it is assumed to be a Windows Vista application and does not use themed controls in the client area when a high contrast theme is active.</span></span> <span data-ttu-id="467a9-151">Además, el comportamiento de algunas funciones de estilos visuales se ve afectado.</span><span class="sxs-lookup"><span data-stu-id="467a9-151">Also, the behavior of some visual styles functions are affected.</span></span> <span data-ttu-id="467a9-152">Por ejemplo, [**IsThemeActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive), [**IsCompositionActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive)y [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) devuelven false, mientras que [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) y [**OpenThemeDataEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) devuelven un identificador nulo.</span><span class="sxs-lookup"><span data-stu-id="467a9-152">For example, [**IsThemeActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive), [**IsCompositionActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive), and [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) return FALSE, while [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) and [**OpenThemeDataEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) return a NULL handle.</span></span> <span data-ttu-id="467a9-153">Esto es para la compatibilidad con la compatibilidad, de modo que las aplicaciones compiladas antes de Windows 8 todavía pueden representar su interfaz de usuario en el mismo aspecto que el modo de contraste alto de las versiones anteriores de Windows en las que los estilos visuales no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="467a9-153">This is for compatibility support, so that applications built before Windows 8 can still render their UI in the same look as the high contrast mode of previous versions of Windows where visual styles are not available.</span></span>

<span data-ttu-id="467a9-154">En Windows 8, la aplicación sigue recibiendo las ventajas de la composición del escritorio.</span><span class="sxs-lookup"><span data-stu-id="467a9-154">On Windows 8, the application still receives the benefits of desktop composition.</span></span> <span data-ttu-id="467a9-155">Esto significa, por ejemplo, que las aplicaciones de facilidad de uso, como el ampliador de pantalla completa, no dependen del estado del manifiesto de una aplicación individual.</span><span class="sxs-lookup"><span data-stu-id="467a9-155">This means, for example, that usability applications such as the full screen magnifier don't depend on the status of an individual application's manifest.</span></span> <span data-ttu-id="467a9-156">La aplicación de facilidad de uso sigue funcionando en el modo de contraste alto con una aplicación que no se identifica como compatible con Windows 8 en su manifiesto.</span><span class="sxs-lookup"><span data-stu-id="467a9-156">The usability application continues to work in high contrast mode with an application that does not identify itself as Windows 8 compatible in its manifest.</span></span>

<span data-ttu-id="467a9-157">En las imágenes siguientes se muestra un cuadro de diálogo simple en contraste alto en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="467a9-157">The following images show a simple dialog box in high contrast on Windows 7.</span></span>

![cuadro de diálogo contraste de hig](images/win7-high-contrast.png)

<span data-ttu-id="467a9-159">En esta imagen se muestra el mismo cuadro de diálogo en contraste alto en Windows 8, pero con la compatibilidad de Windows 7 especificada en el manifiesto de aplicación:</span><span class="sxs-lookup"><span data-stu-id="467a9-159">This image shows the same dialog box in high contrast on Windows 8, but with Windows 7 compatibility specified in the application manifest:</span></span>

![W8 cuadro de diálogo contraste alto](images/win7-compat.png)

<span data-ttu-id="467a9-161">En esta imagen se muestra el mismo cuadro de diálogo en contraste alto en Windows 8, con Windows 8 especificado en el manifiesto de aplicación:</span><span class="sxs-lookup"><span data-stu-id="467a9-161">This image shows the same dialog box in high contrast on Windows 8, with Windows 8 specified in the application manifest:</span></span>

![W8 cuadro de diálogo de contraste alto con manifiesto](images/win8-manifest.png)

## <a name="detecting-high-contrast-in-previous-versions-of-windows"></a><span data-ttu-id="467a9-163">Detección de contraste alto en versiones anteriores de Windows</span><span class="sxs-lookup"><span data-stu-id="467a9-163">Detecting High Contrast in Previous Versions of Windows</span></span>

<span data-ttu-id="467a9-164">Las aplicaciones que se ejecutan en versiones anteriores de Windows no tienen acceso a los nuevos temas de contraste alto.</span><span class="sxs-lookup"><span data-stu-id="467a9-164">Applications running on previous versions of Windows do not have access to the new high contrast themes.</span></span> <span data-ttu-id="467a9-165">Si la aplicación necesita ejecutarse en versiones anteriores de, debe incluir la compatibilidad para representar la interfaz de usuario en alta contraWindowsst en el modelo de Windows clásico.</span><span class="sxs-lookup"><span data-stu-id="467a9-165">If your application needs to run on previous versions of , you should include support for rendering your UI in high contraWindowsst in the Windows classic theming model.</span></span> <span data-ttu-id="467a9-166">La aplicación puede determinar si un tema de contraste alto está activo mediante una llamada a la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) con la marca **SPI \_ GETHIGHCONTRAST** .</span><span class="sxs-lookup"><span data-stu-id="467a9-166">Your application can determine whether a high contrast theme is active by calling the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function with the **SPI\_GETHIGHCONTRAST** flag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="467a9-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="467a9-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="467a9-168">Habilitar los estilos visuales</span><span class="sxs-lookup"><span data-stu-id="467a9-168">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> <dt>

[<span data-ttu-id="467a9-169">Estilos visuales</span><span class="sxs-lookup"><span data-stu-id="467a9-169">Visual Styles</span></span>](themes-overview.md)
</dt> </dl>

 

 
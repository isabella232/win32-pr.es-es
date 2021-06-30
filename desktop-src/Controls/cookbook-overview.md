---
title: Habilitar los estilos visuales
description: En este tema se explica cómo configurar la aplicación para asegurarse de que los controles comunes se muestran en el estilo visual preferido del usuario.
ms.assetid: eb6c2469-25b9-43c4-a6ca-391a7b2859b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4673d0a47f42f557e09f4afe46131cd48bad1b0
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102174"
---
# <a name="enabling-visual-styles"></a><span data-ttu-id="c2442-103">Habilitar los estilos visuales</span><span class="sxs-lookup"><span data-stu-id="c2442-103">Enabling Visual Styles</span></span>

<span data-ttu-id="c2442-104">En este tema se explica cómo configurar la aplicación para asegurarse de que los controles comunes se muestran en el estilo visual preferido del usuario.</span><span class="sxs-lookup"><span data-stu-id="c2442-104">This topic explains how to configure your application to ensure that common controls are displayed in the user's preferred visual style.</span></span>

<span data-ttu-id="c2442-105">En este tema se incluyen las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="c2442-105">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="c2442-106">Usar manifiestos o directivas para asegurarse de que los estilos visuales se pueden aplicar a las aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c2442-106">Using Manifests or Directives to Ensure That Visual Styles Can Be Applied to Applications</span></span>](#using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications)
-   [<span data-ttu-id="c2442-107">Usar ComCtl32.dll versión 6 en una aplicación que solo usa extensiones estándar</span><span class="sxs-lookup"><span data-stu-id="c2442-107">Using ComCtl32.dll Version 6 in an Application That Uses Only Standard Extensions</span></span>](#using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions)
-   [<span data-ttu-id="c2442-108">Usar ComCtl32 versión 6 en Panel de control o un archivo DLL que ejecuta RunDll32.exe</span><span class="sxs-lookup"><span data-stu-id="c2442-108">Using ComCtl32 Version 6 in Control Panel or a DLL That Is Run by RunDll32.exe</span></span>](#using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe)
-   [<span data-ttu-id="c2442-109">Agregar compatibilidad con el estilo visual a una extensión, un complemento, un complemento MMC o un archivo DLL que se incorpora a un proceso</span><span class="sxs-lookup"><span data-stu-id="c2442-109">Adding Visual Style Support to an Extension, Plug-in, MMC Snap-in or a DLL That Is Brought into a Process</span></span>](#adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process)
-   [<span data-ttu-id="c2442-110">Desactivar estilos visuales</span><span class="sxs-lookup"><span data-stu-id="c2442-110">Turning Off Visual Styles</span></span>](#turning-off-visual-styles)
-   [<span data-ttu-id="c2442-111">Usar estilos visuales con contenido HTML</span><span class="sxs-lookup"><span data-stu-id="c2442-111">Using Visual Styles with HTML Content</span></span>](#using-visual-styles-with-html-content)
-   [<span data-ttu-id="c2442-112">Cuando no se aplican estilos visuales</span><span class="sxs-lookup"><span data-stu-id="c2442-112">When Visual Styles are not Applied</span></span>](#when-visual-styles-are-not-applied)
-   [<span data-ttu-id="c2442-113">Hacer que la aplicación sea compatible con versiones anteriores de Windows</span><span class="sxs-lookup"><span data-stu-id="c2442-113">Making Your Application Compatible with Earlier Versions of Windows</span></span>](#making-your-application-compatible-with-earlier-versions-of-windows)
-   [<span data-ttu-id="c2442-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c2442-114">Related topics</span></span>](#related-topics)

## <a name="using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications"></a><span data-ttu-id="c2442-115">Usar manifiestos o directivas para asegurarse de que los estilos visuales se pueden aplicar a las aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c2442-115">Using Manifests or Directives to Ensure That Visual Styles Can Be Applied to Applications</span></span>

<span data-ttu-id="c2442-116">Para permitir que la aplicación use estilos visuales, debe usar ComCtl32.dll versión 6 o posterior.</span><span class="sxs-lookup"><span data-stu-id="c2442-116">To enable your application to use visual styles, you must use ComCtl32.dll version 6 or later.</span></span> <span data-ttu-id="c2442-117">Dado que la versión 6 no es redistribuible, solo está disponible cuando la aplicación se ejecuta en una versión de Windows que la contiene.</span><span class="sxs-lookup"><span data-stu-id="c2442-117">Because version 6 is not redistributable, it is available only when your application is running on a version of Windows that contains it.</span></span> <span data-ttu-id="c2442-118">Windows se suministra con las versiones 5 y 6.</span><span class="sxs-lookup"><span data-stu-id="c2442-118">Windows ships with both version 5 and version 6.</span></span> <span data-ttu-id="c2442-119">ComCtl32.dll versión 6 contiene los controles de usuario y los controles comunes.</span><span class="sxs-lookup"><span data-stu-id="c2442-119">ComCtl32.dll version 6 contains both the user controls and the common controls.</span></span> <span data-ttu-id="c2442-120">De forma predeterminada, las aplicaciones usan los controles de usuario definidos en User32.dll y los controles comunes definidos en ComCtl32.dll versión 5.</span><span class="sxs-lookup"><span data-stu-id="c2442-120">By default, applications use the user controls defined in User32.dll and the common controls defined in ComCtl32.dll version 5.</span></span> <span data-ttu-id="c2442-121">Para obtener una lista de las versiones de DLL y sus plataformas de distribución, vea [Versiones de control comunes](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="c2442-121">For a list of DLL versions and their distribution platforms, see [Common Control Versions](common-control-versions.md).</span></span>

<span data-ttu-id="c2442-122">Si desea que la aplicación use estilos visuales, debe agregar un manifiesto de aplicación o una directiva del compilador que indique que se debe usar ComCtl32.dll versión 6 si está disponible.</span><span class="sxs-lookup"><span data-stu-id="c2442-122">If you want your application to use visual styles, you must add an application manifest or compiler directive that indicates that ComCtl32.dll version 6 should be used if it is available.</span></span>

<span data-ttu-id="c2442-123">Un manifiesto de aplicación permite a una aplicación especificar qué versiones de un ensamblado requiere.</span><span class="sxs-lookup"><span data-stu-id="c2442-123">An application manifest enables an application to specify which versions of an assembly it requires.</span></span> <span data-ttu-id="c2442-124">En Microsoft Win32, un ensamblado es un conjunto de archivos DLL y una lista de objetos con control de versiones que se encuentran dentro de esos archivos DLL.</span><span class="sxs-lookup"><span data-stu-id="c2442-124">In Microsoft Win32, an assembly is a set of DLLs and a list of versionable objects that are contained within those DLLs.</span></span>

<span data-ttu-id="c2442-125">Los manifiestos se escriben en XML.</span><span class="sxs-lookup"><span data-stu-id="c2442-125">Manifests are written in XML.</span></span> <span data-ttu-id="c2442-126">El nombre del archivo de manifiesto de aplicación es el nombre del ejecutable seguido de la extensión de nombre de archivo .manifest; por ejemplo, MyApp.exe.manifest.</span><span class="sxs-lookup"><span data-stu-id="c2442-126">The name of the application manifest file is the name of your executable followed by the file name extension .manifest; for example, MyApp.exe.manifest.</span></span> <span data-ttu-id="c2442-127">En el siguiente manifiesto de ejemplo se muestra que la primera sección describe el propio manifiesto.</span><span class="sxs-lookup"><span data-stu-id="c2442-127">The following sample manifest shows that the first section describes the manifest itself.</span></span> <span data-ttu-id="c2442-128">En la tabla siguiente se muestran los atributos establecidos por el **elemento assemblyIdentity** en la sección de descripción del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="c2442-128">The following table shows the attributes set by the **assemblyIdentity** element in the manifest description section.</span></span>



| <span data-ttu-id="c2442-129">Atributo</span><span class="sxs-lookup"><span data-stu-id="c2442-129">Attribute</span></span>             | <span data-ttu-id="c2442-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2442-130">Description</span></span>                                                                                                                 |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2442-131">version</span><span class="sxs-lookup"><span data-stu-id="c2442-131">version</span></span>               | <span data-ttu-id="c2442-132">Versión del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="c2442-132">Version of the manifest.</span></span> <span data-ttu-id="c2442-133">La versión debe tener el formato major.minor.revision.build (es decir, n.n.n.n, donde n <=65535).</span><span class="sxs-lookup"><span data-stu-id="c2442-133">The version must be in the form major.minor.revision.build (that is, n.n.n.n, where n <=65535).</span></span> |
| <span data-ttu-id="c2442-134">processorArchitecture</span><span class="sxs-lookup"><span data-stu-id="c2442-134">processorArchitecture</span></span> | <span data-ttu-id="c2442-135">Procesador para el que se desarrolla la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2442-135">Processor for which your application is developed.</span></span>                                                                          |
| <span data-ttu-id="c2442-136">name</span><span class="sxs-lookup"><span data-stu-id="c2442-136">name</span></span>                  | <span data-ttu-id="c2442-137">Incluye el nombre de la empresa, el nombre del producto y el nombre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2442-137">Includes company name, product name and application name.</span></span>                                                                   |
| <span data-ttu-id="c2442-138">type</span><span class="sxs-lookup"><span data-stu-id="c2442-138">type</span></span>                  | <span data-ttu-id="c2442-139">Tipo de aplicación, como Win32.</span><span class="sxs-lookup"><span data-stu-id="c2442-139">Type of your application, such as Win32.</span></span>                                                                                    |



 

<span data-ttu-id="c2442-140">El manifiesto de ejemplo también proporciona una descripción de la aplicación y especifica las dependencias de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2442-140">The sample manifest also provides a description of your application and specifies application dependencies.</span></span> <span data-ttu-id="c2442-141">En la tabla siguiente se muestran los atributos establecidos por el **elemento assemblyIdentity** en la sección de dependencia.</span><span class="sxs-lookup"><span data-stu-id="c2442-141">The following table shows the attributes set by the **assemblyIdentity** element in the dependency section.</span></span>



| <span data-ttu-id="c2442-142">Atributo</span><span class="sxs-lookup"><span data-stu-id="c2442-142">Attribute</span></span>             | <span data-ttu-id="c2442-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2442-143">Description</span></span>                                      |
|-----------------------|--------------------------------------------------|
| <span data-ttu-id="c2442-144">type</span><span class="sxs-lookup"><span data-stu-id="c2442-144">type</span></span>                  | <span data-ttu-id="c2442-145">Tipo del componente de dependencia, como Win32.</span><span class="sxs-lookup"><span data-stu-id="c2442-145">Type of the dependency component, such as Win32.</span></span> |
| <span data-ttu-id="c2442-146">name</span><span class="sxs-lookup"><span data-stu-id="c2442-146">name</span></span>                  | <span data-ttu-id="c2442-147">Nombre del componente.</span><span class="sxs-lookup"><span data-stu-id="c2442-147">Name of the component.</span></span>                           |
| <span data-ttu-id="c2442-148">version</span><span class="sxs-lookup"><span data-stu-id="c2442-148">version</span></span>               | <span data-ttu-id="c2442-149">Versión del componente.</span><span class="sxs-lookup"><span data-stu-id="c2442-149">Version of the component.</span></span>                        |
| <span data-ttu-id="c2442-150">processorArchitecture</span><span class="sxs-lookup"><span data-stu-id="c2442-150">processorArchitecture</span></span> | <span data-ttu-id="c2442-151">Procesador para el que está diseñado el componente.</span><span class="sxs-lookup"><span data-stu-id="c2442-151">Processor that the component is designed for.</span></span>    |
| <span data-ttu-id="c2442-152">Publickeytoken</span><span class="sxs-lookup"><span data-stu-id="c2442-152">publicKeyToken</span></span>        | <span data-ttu-id="c2442-153">Token de clave usado con este componente.</span><span class="sxs-lookup"><span data-stu-id="c2442-153">Key token used with this component.</span></span>              |
| <span data-ttu-id="c2442-154">language</span><span class="sxs-lookup"><span data-stu-id="c2442-154">language</span></span>              | <span data-ttu-id="c2442-155">Idioma del componente.</span><span class="sxs-lookup"><span data-stu-id="c2442-155">Language of the component.</span></span>                       |



 

<span data-ttu-id="c2442-156">A continuación se muestra un ejemplo de un archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="c2442-156">Following is an example of a manifest file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c2442-157">Establezca la entrada **processorArchitecture** en **"X86"** si la aplicación tiene como destino la plataforma Windows de 32 bits o **en "amd64"** si la aplicación tiene como destino la plataforma windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c2442-157">Set the **processorArchitecture** entry to **"X86"** if your application targets the 32 bit Windows platform, or to **"amd64"** if your application targets the 64 bit Windows platform.</span></span> <span data-ttu-id="c2442-158">También puede especificar **\* "",** lo que garantiza que todas las plataformas están destinadas, como se muestra en los ejemplos siguientes.</span><span class="sxs-lookup"><span data-stu-id="c2442-158">You can also specify **"\*"**, which ensures that all platforms are targeted, as shown in the following examples.</span></span>

 


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity
    version="1.0.0.0"
    processorArchitecture="*"
    name="CompanyName.ProductName.YourApplication"
    type="win32"
/>
<description>Your application description here.</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="*"
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
</assembly>
```



<span data-ttu-id="c2442-159">Si usa Microsoft Visual C++ 2005 o posterior, puede agregar la siguiente directiva del compilador al código fuente en lugar de crear manualmente un manifiesto.</span><span class="sxs-lookup"><span data-stu-id="c2442-159">If you are using Microsoft Visual C++ 2005 or later, you can add the following compiler directive to your source code instead of manually creating a manifest.</span></span> <span data-ttu-id="c2442-160">Para mejorar la legibilidad, la directiva se divide en varias líneas aquí.</span><span class="sxs-lookup"><span data-stu-id="c2442-160">For readability, the directive is broken into several lines here.</span></span>


```C++
#pragma comment(linker,"\"/manifestdependency:type='win32' \
name='Microsoft.Windows.Common-Controls' version='6.0.0.0' \
processorArchitecture='*' publicKeyToken='6595b64144ccf1df' language='*'\"")
```



<span data-ttu-id="c2442-161">En los temas siguientes se describen los pasos para aplicar estilos visuales a diferentes tipos de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="c2442-161">The following topics describe the steps for applying visual styles to different types of applications.</span></span> <span data-ttu-id="c2442-162">Observe que el formato del manifiesto es el mismo en cada caso.</span><span class="sxs-lookup"><span data-stu-id="c2442-162">Notice that the manifest format is the same in each case.</span></span>

## <a name="using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions"></a><span data-ttu-id="c2442-163">Usar ComCtl32.dll versión 6 en una aplicación que solo usa extensiones estándar</span><span class="sxs-lookup"><span data-stu-id="c2442-163">Using ComCtl32.dll Version 6 in an Application That Uses Only Standard Extensions</span></span>

<span data-ttu-id="c2442-164">A continuación se muestran ejemplos de aplicaciones que no usan extensiones de terceros.</span><span class="sxs-lookup"><span data-stu-id="c2442-164">The following are examples of applications that do not use third-party extensions.</span></span>

-   <span data-ttu-id="c2442-165">Calculadora</span><span class="sxs-lookup"><span data-stu-id="c2442-165">Calculator</span></span>
-   <span data-ttu-id="c2442-166">FreeCell (en Windows Vista y Windows 7)</span><span class="sxs-lookup"><span data-stu-id="c2442-166">FreeCell (in Windows Vista and Windows 7)</span></span>
-   <span data-ttu-id="c2442-167">Minesweeper (en Windows Vista y Windows 7)</span><span class="sxs-lookup"><span data-stu-id="c2442-167">Minesweeper (in Windows Vista and Windows 7)</span></span>
-   <span data-ttu-id="c2442-168">Bloc de notas</span><span class="sxs-lookup"><span data-stu-id="c2442-168">Notepad</span></span>
-   <span data-ttu-id="c2442-169">Porrón (en Windows Vista y Windows 7)</span><span class="sxs-lookup"><span data-stu-id="c2442-169">Solitaire (in Windows Vista and Windows 7)</span></span>

<span data-ttu-id="c2442-170">**Para crear un manifiesto y permitir que la aplicación use estilos visuales.**</span><span class="sxs-lookup"><span data-stu-id="c2442-170">**To create a manifest and enable your application to use visual styles.**</span></span>

1.  <span data-ttu-id="c2442-171">Vincule a ComCtl32.lib y llame a [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span><span class="sxs-lookup"><span data-stu-id="c2442-171">Link to ComCtl32.lib and call [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span></span>
2.  <span data-ttu-id="c2442-172">Agregue un archivo denominado YourApp.exe.manifest al árbol de origen que tenga el formato de manifiesto XML.</span><span class="sxs-lookup"><span data-stu-id="c2442-172">Add a file called YourApp.exe.manifest to your source tree that has the XML manifest format.</span></span>
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  <span data-ttu-id="c2442-173">Agregue el manifiesto al archivo de recursos de la aplicación como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="c2442-173">Add the manifest to your application's resource file as follows:</span></span>
    ```C++
    CREATEPROCESS_MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.exe.manifest"
    ```

    

    > [!Note]  
    > <span data-ttu-id="c2442-174">Al agregar la entrada anterior al recurso, debe formatearla en una línea.</span><span class="sxs-lookup"><span data-stu-id="c2442-174">When you add the previous entry to the resource you must format it on one line.</span></span> <span data-ttu-id="c2442-175">Como alternativa, puede colocar el archivo de manifiesto XML en el mismo directorio que el archivo ejecutable de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2442-175">Alternatively, you can place the XML manifest file in the same directory as your application's executable file.</span></span> <span data-ttu-id="c2442-176">El sistema operativo cargará primero el manifiesto desde el sistema de archivos y, a continuación, comprobará la sección de recursos del ejecutable.</span><span class="sxs-lookup"><span data-stu-id="c2442-176">The operating system will load the manifest from the file system first, then check the resource section of the executable.</span></span> <span data-ttu-id="c2442-177">La versión del sistema de archivos tiene prioridad.</span><span class="sxs-lookup"><span data-stu-id="c2442-177">The file system version takes precedence.</span></span>

     

<span data-ttu-id="c2442-178">Al compilar la aplicación, el manifiesto se agregará como un recurso binario.</span><span class="sxs-lookup"><span data-stu-id="c2442-178">When you build your application, the manifest will be added as a binary resource.</span></span>

## <a name="using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe"></a><span data-ttu-id="c2442-179">Usar ComCtl32 versión 6 en Panel de control o un archivo DLL ejecutado por RunDll32.exe</span><span class="sxs-lookup"><span data-stu-id="c2442-179">Using ComCtl32 Version 6 in Control Panel or a DLL That Is Run by RunDll32.exe</span></span>

<span data-ttu-id="c2442-180">**Para crear un manifiesto y permitir que la aplicación use estilos visuales.**</span><span class="sxs-lookup"><span data-stu-id="c2442-180">**To create a manifest and enable your application to use visual styles.**</span></span>

1.  <span data-ttu-id="c2442-181">Vincule a ComCtl32.lib y llame a [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span><span class="sxs-lookup"><span data-stu-id="c2442-181">Link to ComCtl32.lib and call [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span></span>
2.  <span data-ttu-id="c2442-182">Agregue un archivo denominado YourApp.cpl.manifest al árbol de origen que tenga el formato de manifiesto XML.</span><span class="sxs-lookup"><span data-stu-id="c2442-182">Add a file called YourApp.cpl.manifest to your source tree that has the XML manifest format.</span></span>
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  <span data-ttu-id="c2442-183">Agregue el manifiesto al archivo de recursos de la aplicación como id. de recurso 123.</span><span class="sxs-lookup"><span data-stu-id="c2442-183">Add the manifest to your application's resource file as resource ID 123.</span></span>

> [!Note]  
> <span data-ttu-id="c2442-184">Al crear una aplicación Panel de control, coló hay que colocarla en la categoría adecuada.</span><span class="sxs-lookup"><span data-stu-id="c2442-184">When you author a Control Panel application, place it in the appropriate category.</span></span> <span data-ttu-id="c2442-185">Panel de control ahora admite la categorización de Panel de control aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="c2442-185">Control Panel now supports categorization of Control Panel applications.</span></span> <span data-ttu-id="c2442-186">Esto significa que Panel de control a las aplicaciones se les pueden asignar identificadores y separarse en áreas de tareas, como Agregar o quitar programas, Apariencia y temas, o Fecha, Hora, Idioma y Opciones regionales.</span><span class="sxs-lookup"><span data-stu-id="c2442-186">This means that Control Panel applications can be assigned identifiers and separated into task areas such as Add or Remove Programs, Appearance and Themes, or Date, Time, Language, and Regional Options.</span></span>

 

## <a name="adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process"></a><span data-ttu-id="c2442-187">Agregar compatibilidad de estilo visual a una extensión, un complemento, un complemento MMC o un archivo DLL que se incorpora a un proceso</span><span class="sxs-lookup"><span data-stu-id="c2442-187">Adding Visual Style Support to an Extension, Plug-in, MMC Snap-in or a DLL That Is Brought into a Process</span></span>

<span data-ttu-id="c2442-188">Se puede agregar compatibilidad con estilos visuales a una extensión, un complemento, un complemento MMC o un archivo DLL que se lleva a un proceso.</span><span class="sxs-lookup"><span data-stu-id="c2442-188">Support for visual styles can be added to an extension, plug-in, MMC snap-in, or a DLL that is brought into a process.</span></span> <span data-ttu-id="c2442-189">Por ejemplo, siga estos pasos para agregar compatibilidad con estilos visuales para un complemento Microsoft Management Console (MMC).</span><span class="sxs-lookup"><span data-stu-id="c2442-189">For example, use the following steps to add visual styles support for an Microsoft Management Console (MMC) snap-in.</span></span>

1.  <span data-ttu-id="c2442-190">Compile el complemento con la marca -DISOLATION AWARE ENABLED o inserte la siguiente instrucción antes de \_ \_ incluir la instrucción \# "windows.h".</span><span class="sxs-lookup"><span data-stu-id="c2442-190">Compile your snap-in with the -DISOLATION\_AWARE\_ENABLED flag or insert the following statement before the \#include "windows.h" statement.</span></span>

    ```C++
    #define ISOLATION_AWARE_ENABLED 1
    ```

    

    <span data-ttu-id="c2442-191">Para obtener más información sobre ISOLATION \_ AWARE \_ ENABLED, vea [Aislar componentes](/windows/desktop/SbsCs/isolating-components).</span><span class="sxs-lookup"><span data-stu-id="c2442-191">For more information about ISOLATION\_AWARE\_ENABLED, see [Isolating Components](/windows/desktop/SbsCs/isolating-components).</span></span>

2.  <span data-ttu-id="c2442-192">Incluya el archivo de encabezado de control común en el origen del complemento.</span><span class="sxs-lookup"><span data-stu-id="c2442-192">Include the common control header file in your snap-in source.</span></span>
    ```C++
    #include <commctrl.h>
    ```

    

3.  <span data-ttu-id="c2442-193">Agregue un archivo denominado YourApp.manifest al árbol de origen que use el formato de manifiesto XML.</span><span class="sxs-lookup"><span data-stu-id="c2442-193">Add a file called YourApp.manifest to your source tree that uses the XML manifest format.</span></span>
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

4.  <span data-ttu-id="c2442-194">Agregue el manifiesto al archivo de recursos del complemento.</span><span class="sxs-lookup"><span data-stu-id="c2442-194">Add the manifest to your snap-in's resource file.</span></span> <span data-ttu-id="c2442-195">Consulte [Using ComCtl32 Version 6 in an Application That Uses Extensions, Plug-ins,](/previous-versions//ms649781(v=vs.85)) or a DLL That Is Brought into a Process (Uso de ComCtl32 versión 6 en una aplicación que usa extensiones, complementos o un archivo DLL que se incorpora a un proceso) para obtener más información sobre cómo agregar un manifiesto a un archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c2442-195">See [Using ComCtl32 Version 6 in an Application That Uses Extensions, Plug-ins, or a DLL That Is Brought into a Process](/previous-versions//ms649781(v=vs.85)) for details on adding a manifest to a resource file.</span></span>

## <a name="turning-off-visual-styles"></a><span data-ttu-id="c2442-196">Desactivar estilos visuales</span><span class="sxs-lookup"><span data-stu-id="c2442-196">Turning Off Visual Styles</span></span>

<span data-ttu-id="c2442-197">Puede desactivar los estilos visuales de un control o de todos los controles de una ventana llamando a la [**función SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="c2442-197">You can turn off visual styles for a control or for all controls in a window by calling the [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) function as follows:</span></span>


```C++
SetWindowTheme(hwnd, L" ", L" ");
```



<span data-ttu-id="c2442-198">En el ejemplo anterior, *hwnd* es el identificador de la ventana en la que se deshabilitan los estilos visuales.</span><span class="sxs-lookup"><span data-stu-id="c2442-198">In the previous example, *hwnd* is the handle of the window in which to disable visual styles.</span></span> <span data-ttu-id="c2442-199">Después de la llamada, el control se representa sin estilos visuales.</span><span class="sxs-lookup"><span data-stu-id="c2442-199">After the call, the control renders without visual styles.</span></span>

## <a name="using-visual-styles-with-html-content"></a><span data-ttu-id="c2442-200">Usar estilos visuales con contenido HTML</span><span class="sxs-lookup"><span data-stu-id="c2442-200">Using Visual Styles with HTML Content</span></span>

<span data-ttu-id="c2442-201">Las páginas HTML que modifican Hojas de estilo CSS (CSS) como el fondo o el borde no tienen estilos visuales aplicados.</span><span class="sxs-lookup"><span data-stu-id="c2442-201">HTML pages that modify the Cascading Style Sheets (CSS) properties such as background or border do not have visual styles applied to them.</span></span> <span data-ttu-id="c2442-202">Muestran el atributo CSS especificado.</span><span class="sxs-lookup"><span data-stu-id="c2442-202">They display the specified CSS attribute.</span></span> <span data-ttu-id="c2442-203">Cuando se especifica como parte del contenido, la mayoría de las propiedades CSS se aplican a los elementos que tienen estilos visuales aplicados.</span><span class="sxs-lookup"><span data-stu-id="c2442-203">When specified as part of the content, most CSS properties do apply to elements that have visual styles applied.</span></span>

<span data-ttu-id="c2442-204">De forma predeterminada, los estilos visuales se aplican a controles HTML intrínsecos en las páginas mostradas en Microsoft Internet Explorer 6 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="c2442-204">By default, visual styles are applied to intrinsic HTML controls on pages displayed in Microsoft Internet Explorer 6 and later versions.</span></span> <span data-ttu-id="c2442-205">Para desactivar los estilos visuales de una página HTML, agregue una etiqueta META a</span><span class="sxs-lookup"><span data-stu-id="c2442-205">To turn off visual styles for an HTML page, add a META tag to the</span></span> <head> <span data-ttu-id="c2442-206">.</span><span class="sxs-lookup"><span data-stu-id="c2442-206">section.</span></span> <span data-ttu-id="c2442-207">Esta técnica también se aplica al contenido empaquetado como aplicaciones HTML (HTA).</span><span class="sxs-lookup"><span data-stu-id="c2442-207">This technique also applies to content packaged as HTML Applications (HTAs).</span></span> <span data-ttu-id="c2442-208">Para desactivar los estilos visuales, la etiqueta META debe ser la siguiente:</span><span class="sxs-lookup"><span data-stu-id="c2442-208">To turn off visual styles, the META tag must be as follows:</span></span>


```
<META HTTP-EQUIV="MSThemeCompatible" CONTENT="no">
```



> [!Note]  
> <span data-ttu-id="c2442-209">Si la configuración del explorador y la configuración de etiqueta no están de acuerdo, la página no aplicará estilos visuales.</span><span class="sxs-lookup"><span data-stu-id="c2442-209">If the browser setting and the tag setting do not agree, the page will not apply visual styles.</span></span> <span data-ttu-id="c2442-210">Por ejemplo, si la etiqueta META se establece en "no" y el explorador está establecido para habilitar estilos visuales, los estilos visuales no se aplicarán a la página.</span><span class="sxs-lookup"><span data-stu-id="c2442-210">For example, if the META tag is set to "no" and the browser is set to enable visual styles, visual styles will not be applied to the page.</span></span> <span data-ttu-id="c2442-211">Sin embargo, si el explorador o la etiqueta META se establecen en "sí" y no se especifica el otro elemento, se aplicarán estilos visuales.</span><span class="sxs-lookup"><span data-stu-id="c2442-211">However, if either the browser or META tag is set to "yes" and the other item is not specified, visual styles will be applied.</span></span>

 

<span data-ttu-id="c2442-212">Los estilos visuales pueden cambiar el diseño del contenido.</span><span class="sxs-lookup"><span data-stu-id="c2442-212">Visual styles might change the layout of your content.</span></span> <span data-ttu-id="c2442-213">Además, si establece determinados atributos en controles HTML intrínsecos, como el ancho de un botón, es posible que la etiqueta del botón sea ilegible en determinados estilos visuales.</span><span class="sxs-lookup"><span data-stu-id="c2442-213">Also, if you set certain attributes on intrinsic HTML controls, such as the width of a button, you might find that the label on the button is unreadable under certain visual styles.</span></span>

<span data-ttu-id="c2442-214">Debe probar exhaustivamente el contenido mediante estilos visuales para determinar si la aplicación de estilos visuales tiene un efecto adverso en el contenido y el diseño.</span><span class="sxs-lookup"><span data-stu-id="c2442-214">You must thoroughly test your content using visual styles to determine whether applying visual styles has an adverse effect on your content and layout.</span></span>

## <a name="when-visual-styles-are-not-applied"></a><span data-ttu-id="c2442-215">Cuando no se aplican estilos visuales</span><span class="sxs-lookup"><span data-stu-id="c2442-215">When Visual Styles are not Applied</span></span>

<span data-ttu-id="c2442-216">Para evitar aplicar estilos visuales a una ventana de nivel superior, dé a la ventana una región que no sea NULL (**SetWindowRgn**).</span><span class="sxs-lookup"><span data-stu-id="c2442-216">To avoid applying visual styles to a top level window, give the window a non-null region (**SetWindowRgn**).</span></span> <span data-ttu-id="c2442-217">El sistema supone que una ventana con una región que no es NULL es una ventana especializada que no usa estilos visuales.</span><span class="sxs-lookup"><span data-stu-id="c2442-217">The system assumes that a window with a non-NULL region is a specialized window that does not use visual styles.</span></span> <span data-ttu-id="c2442-218">Una ventana secundaria asociada a una ventana de nivel superior que no sea de estilos visuales puede seguir aplicando estilos visuales aunque la ventana primaria no lo haga.</span><span class="sxs-lookup"><span data-stu-id="c2442-218">A child window associated with a non-visual-styles top level window may still apply visual styles even though the parent window does not.</span></span>

<span data-ttu-id="c2442-219">Si desea deshabilitar el uso de estilos visuales para todas las ventanas de la aplicación, llame a [**SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) y no pase la marca STAP \_ ALLOW \_ NONCLIENT.</span><span class="sxs-lookup"><span data-stu-id="c2442-219">If you want to disable the use of visual styles for all windows in your application, call [**SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) and do not pass the STAP\_ALLOW\_NONCLIENT flag.</span></span> <span data-ttu-id="c2442-220">Si una aplicación no llama a **SetThemeAppProperties,** los valores de marca asumidos son STAP \_ ALLOW \_ NONCLIENT \| STAP \_ ALLOW CONTROLS \_ \| STAP ALLOW \_ \_ WEBCONTENT.</span><span class="sxs-lookup"><span data-stu-id="c2442-220">If an application does not call **SetThemeAppProperties**, the assumed flag values are STAP\_ALLOW\_NONCLIENT \| STAP\_ALLOW\_CONTROLS \| STAP\_ALLOW\_WEBCONTENT.</span></span> <span data-ttu-id="c2442-221">Los valores asumidos hacen que se aplique un estilo visual al área no cliente, los controles y el contenido web.</span><span class="sxs-lookup"><span data-stu-id="c2442-221">The assumed values cause the nonclient area, the controls, and web content to have a visual style applied.</span></span>

## <a name="making-your-application-compatible-with-earlier-versions-of-windows"></a><span data-ttu-id="c2442-222">Hacer que la aplicación sea compatible con versiones anteriores de Windows</span><span class="sxs-lookup"><span data-stu-id="c2442-222">Making Your Application Compatible with Earlier Versions of Windows</span></span>

<span data-ttu-id="c2442-223">Gran parte de la arquitectura de estilo visual está diseñada para facilitar el envío del producto en versiones anteriores de Windows que no admiten cambiar la apariencia de los controles.</span><span class="sxs-lookup"><span data-stu-id="c2442-223">Much of the visual style architecture is designed to make it simple to continue to ship your product on earlier versions of Windows that do not support changing the appearance of controls.</span></span> <span data-ttu-id="c2442-224">Al enviar una aplicación para más de un sistema operativo, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c2442-224">When shipping an application for more than one operating system, be aware of the following:</span></span>

-   <span data-ttu-id="c2442-225">En las versiones de Windows anteriores a Windows 8, los estilos visuales están desactivados cuando el contraste alto está on.</span><span class="sxs-lookup"><span data-stu-id="c2442-225">In versions of Windows prior to Windows 8, visual styles are off when high contrast is on.</span></span> <span data-ttu-id="c2442-226">Para admitir el contraste alto, una aplicación heredada que admite estilos visuales debe proporcionar una ruta de acceso de código independiente para dibujar correctamente los elementos de la interfaz de usuario en contraste alto.</span><span class="sxs-lookup"><span data-stu-id="c2442-226">To support high contrast, a legacy application that supports visual styles needs to provide a separate code path to properly draw UI elements in high contrast.</span></span> <span data-ttu-id="c2442-227">En Windows 8, el contraste alto forma parte de los estilos visuales; sin embargo, una aplicación de Windows 8 (una que incluya el GUID de Windows 8 en la sección de compatibilidad de su manifiesto de aplicación) todavía necesita proporcionar una ruta de acceso de código independiente para representarse correctamente en contraste alto en Windows 7 una vez anterior.</span><span class="sxs-lookup"><span data-stu-id="c2442-227">In Windows 8, high contrast is a part of visual styles; however, a Windows 8 application (one that includes the Windows 8 GUID in compatibility section of its application manifest) still needs to provide a separate code path to render correctly in high contrast on Windows 7 an earlier.</span></span>
-   <span data-ttu-id="c2442-228">Si usa las características de ComCtl32.dll versión 6, como la vista de icono o el control de vínculo, debe controlar el caso en el que esos controles no están disponibles en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="c2442-228">If you use the features in ComCtl32.dll version 6, such as the tile view or link control, you must handle the case where those controls are not available on your user's computer.</span></span> <span data-ttu-id="c2442-229">ComCtl32.dll versión 6 no es redistribuible.</span><span class="sxs-lookup"><span data-stu-id="c2442-229">ComCtl32.dll version 6 is not redistributable.</span></span>
-   <span data-ttu-id="c2442-230">Pruebe la aplicación para asegurarse de que no se basa en las características de ComCtl32.dll versión 6 sin comprobar primero la versión actual.</span><span class="sxs-lookup"><span data-stu-id="c2442-230">Test your application to make sure you are not relying on features of ComCtl32.dll version 6 without first checking for the current version.</span></span>
-   <span data-ttu-id="c2442-231">No vincule a UxTheme.lib.</span><span class="sxs-lookup"><span data-stu-id="c2442-231">Do not link to UxTheme.lib.</span></span>
-   <span data-ttu-id="c2442-232">Escribir código de control de errores para instancias de cuando los estilos visuales no funcionan según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="c2442-232">Write error-handling code for instances when visual styles do not work as expected.</span></span>
-   <span data-ttu-id="c2442-233">La instalación del manifiesto de la aplicación en versiones anteriores no afectará a la representación de controles.</span><span class="sxs-lookup"><span data-stu-id="c2442-233">Installing your application's manifest in earlier versions will not affect the rendering of controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2442-234">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c2442-234">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2442-235">Estilos visuales</span><span class="sxs-lookup"><span data-stu-id="c2442-235">Visual Styles</span></span>](themes-overview.md)
</dt> </dl>

 

 

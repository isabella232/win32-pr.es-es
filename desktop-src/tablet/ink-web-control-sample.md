---
description: En este ejemplo se muestra cómo crear un control con tinta habilitada para su uso en un explorador Web. En el ejemplo se toma el ejemplo de formulario de notificaciones automáticas original y se convierte en un control que se coloca en una página web.
ms.assetid: 7a9e304c-57ef-41a3-83be-2b2d31435da8
title: Ejemplo de control Web de entrada manuscrita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101537c4cc7b42181cf8d9ff177a5854c5b84054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715083"
---
# <a name="ink-web-control-sample"></a><span data-ttu-id="cd082-104">Ejemplo de control Web de entrada manuscrita</span><span class="sxs-lookup"><span data-stu-id="cd082-104">Ink Web Control Sample</span></span>

<span data-ttu-id="cd082-105">En este ejemplo se muestra cómo crear un control con tinta habilitada para su uso en un explorador Web.</span><span class="sxs-lookup"><span data-stu-id="cd082-105">This sample shows how to create an ink-enabled control for use in a Web browser.</span></span> <span data-ttu-id="cd082-106">En el ejemplo se toma el [ejemplo de formulario de notificaciones automáticas](auto-claims-form-sample.md) original y se convierte en un control que se coloca en una página web.</span><span class="sxs-lookup"><span data-stu-id="cd082-106">The sample takes the original [Auto Claims Form Sample](auto-claims-form-sample.md) and turns it into a control that is put on a Web page.</span></span>

<span data-ttu-id="cd082-107">Para obtener más información sobre el uso de entradas manuscritas en la web, consulte [entrada de lápiz en la web](ink-on-the-web.md).</span><span class="sxs-lookup"><span data-stu-id="cd082-107">For more information about using ink on the Web, see [Ink on the Web](ink-on-the-web.md).</span></span>

## <a name="modifications-to-the-original-sample-project"></a><span data-ttu-id="cd082-108">Modificaciones en el proyecto de ejemplo original</span><span class="sxs-lookup"><span data-stu-id="cd082-108">Modifications to the Original Sample Project</span></span>

<span data-ttu-id="cd082-109">Este ejemplo consta de una solución que incluye dos proyectos y un archivo HTML.</span><span class="sxs-lookup"><span data-stu-id="cd082-109">This sample consists of a solution that includes two projects and an HTML file.</span></span> <span data-ttu-id="cd082-110">El primer proyecto, autoclaims, es un \# proyecto de biblioteca de controles de Microsoft Visual C (un control de usuario).</span><span class="sxs-lookup"><span data-stu-id="cd082-110">The first project, AutoClaims, is a Microsoft Visual C\# Control Library project (a User Control).</span></span> <span data-ttu-id="cd082-111">El código fuente de este control es casi idéntico al del ejemplo autoclaims con dos diferencias:</span><span class="sxs-lookup"><span data-stu-id="cd082-111">The source code for this control is almost identical to that of the AutoClaims sample with two differences:</span></span>

-   <span data-ttu-id="cd082-112">La `AutoClaims` clase de este ejemplo hereda de la clase [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) en lugar de la clase [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="cd082-112">The `AutoClaims` class in this sample inherits from the [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) class rather than the [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) class.</span></span>

    ```C++
    public class AutoClaims : System.Windows.Forms.UserControl 
    ```

    

-   <span data-ttu-id="cd082-113">La clase autoclaims de este ejemplo tiene un método público agregado, `DisposeResources` que elimina los controles secundarios internos que se usan para recopilar la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="cd082-113">The AutoClaims Class in this sample has an added public method, `DisposeResources` that disposes of the internal child controls used for collecting ink.</span></span> <span data-ttu-id="cd082-114">La página web en la que se usa el control debe llamar a este método cuando la página termina de usar el control.</span><span class="sxs-lookup"><span data-stu-id="cd082-114">This method must be called by thewebpageon which the control is used when that page is finished using the control.</span></span>

## <a name="referencing-the-control-in-html"></a><span data-ttu-id="cd082-115">Hacer referencia al control en HTML</span><span class="sxs-lookup"><span data-stu-id="cd082-115">Referencing the Control in HTML</span></span>

<span data-ttu-id="cd082-116">La solución incluye un archivo HTML, default.htm.</span><span class="sxs-lookup"><span data-stu-id="cd082-116">The solution includes an HTML file, default.htm.</span></span> <span data-ttu-id="cd082-117">Este archivo es la página a la que navega el explorador para cargar el control.</span><span class="sxs-lookup"><span data-stu-id="cd082-117">This file is the page that the browser navigates to in order to load the control.</span></span> <span data-ttu-id="cd082-118">El archivo contiene una <object> etiqueta que hace referencia al control.</span><span class="sxs-lookup"><span data-stu-id="cd082-118">The file contains an <object> tag that references the control.</span></span> <span data-ttu-id="cd082-119">También incluye un script al que se llama cuando la página se descarga, tal como se indica en la presencia del atributo onload = " `OnUnload()` " en el</span><span class="sxs-lookup"><span data-stu-id="cd082-119">It also includes a script that is called when the page unloads, as indicated by the presence of the onload=" `OnUnload()` " attribute in the</span></span> <body> <span data-ttu-id="cd082-120">.</span><span class="sxs-lookup"><span data-stu-id="cd082-120">tag.</span></span> <span data-ttu-id="cd082-121">Esta función llama al `DisposeResources` método en el control para asegurarse de que todos los recursos se liberan correctamente en el cierre.</span><span class="sxs-lookup"><span data-stu-id="cd082-121">This function calls the `DisposeResources` method on the control to make sure that all resources are properly released at shutdown.</span></span>


```C++
<html>
    <script language="jscript">
        // Release any resources held by the AutoClaims control
        function OnUnload()
        {
            autoClaimsControl.DisposeResources();
        }
    </script>
    <head>
        <title>AutoClaims (Web Control)</title>
    </head>
    <body onunload="OnUnload()">
        <object 
          id="autoClaimsControl" 
          classid="AutoClaims.dll#AutoClaims.AutoClaims">
        </object>
    </body>
</html> 
```



<span data-ttu-id="cd082-122">Observe el formato del valor del atributo classid para la <object> etiqueta.</span><span class="sxs-lookup"><span data-stu-id="cd082-122">Notice the format of the classid attribute value for the <object> tag.</span></span> <span data-ttu-id="cd082-123">Asigna un nombre al ensamblado, seguido de un \# separador de signo y, a continuación, el espacio de nombres que contiene el control y, a continuación, el nombre de clase del control.</span><span class="sxs-lookup"><span data-stu-id="cd082-123">It names the assembly, followed with a \# sign separator, and then the namespace that contains the control and then the class name of the control.</span></span>

<span data-ttu-id="cd082-124">Un control de usuario real probablemente incluye métodos adicionales que se usan para conservar o enviar los datos recopilados en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cd082-124">A real-world user control would likely include additional methods used to persist or send the data collected in the application.</span></span>

## <a name="the-autoclaims_webcontrol-project"></a><span data-ttu-id="cd082-125">Proyecto WebControl de autoclaims \_</span><span class="sxs-lookup"><span data-stu-id="cd082-125">The AutoClaims\_WebControl Project</span></span>

<span data-ttu-id="cd082-126">El \_ proyecto WebControl Webclaims es un proyecto de implementación que crea una configuración que agrega una raíz virtual, \_ WebControl WebControl en el servidor Web cuando está instalado.</span><span class="sxs-lookup"><span data-stu-id="cd082-126">The AutoClaims\_WebControl project is a Deployment Project that creates a setup that adds a virtual root, AutoClaims\_WebControl, on the Web server when installed.</span></span> <span data-ttu-id="cd082-127">El control y el archivo HTML se colocan en esta raíz virtual.</span><span class="sxs-lookup"><span data-stu-id="cd082-127">The control and the HTML file are placed in this virtual root.</span></span>

> [!Note]  
> <span data-ttu-id="cd082-128">Los ejemplos web compilados no se instalan con la opción de instalación predeterminada para el SDK.</span><span class="sxs-lookup"><span data-stu-id="cd082-128">The compiled web samples are not installed by the default installation option for the SDK.</span></span> <span data-ttu-id="cd082-129">Debe completar una instalación personalizada y seleccionar la subopción "ejemplos web precompilados" para instalarlas.</span><span class="sxs-lookup"><span data-stu-id="cd082-129">You must complete a custom installation and select the "Pre-compiled Web Samples" sub-option to install them.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="cd082-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cd082-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd082-131">Ejemplo de formulario de notificaciones automáticas</span><span class="sxs-lookup"><span data-stu-id="cd082-131">Auto Claims Form Sample</span></span>](auto-claims-form-sample.md)
</dt> <dt>

[<span data-ttu-id="cd082-132">Entrada manuscrita en la web</span><span class="sxs-lookup"><span data-stu-id="cd082-132">Ink on the Web</span></span>](ink-on-the-web.md)
</dt> </dl>

 

 

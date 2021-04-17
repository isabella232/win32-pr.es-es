---
title: Habilitar el registro
description: Habilitar el registro
ms.assetid: 50fc1d71-b650-4ba5-a6e1-631c0b9fe8ad
keywords:
- Administrador de dispositivos de Windows Media, registro
- Administrador de dispositivos, registro
- aplicaciones de escritorio, registro
- proveedores de servicios, registro
- Guía de programación, registro
- logging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e95be13e93a5a58bb728d5600c6fdea9801ec2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695273"
---
# <a name="enabling-logging"></a><span data-ttu-id="f62df-109">Habilitar el registro</span><span class="sxs-lookup"><span data-stu-id="f62df-109">Enabling Logging</span></span>

<span data-ttu-id="f62df-110">Windows Media Administrador de dispositivos proporciona un objeto de registro que puede guardar información en un archivo de texto en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="f62df-110">Windows Media Device Manager provides a logging object that can save information to a text file at run time.</span></span> <span data-ttu-id="f62df-111">Los desarrolladores de aplicaciones y proveedores de servicios pueden utilizar este objeto para almacenar los mensajes en un archivo de registro mientras se ejecuta su aplicación o proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="f62df-111">Developers of both applications and service providers can use this object to store messages in a log file while their application or service provider is running.</span></span> <span data-ttu-id="f62df-112">Este objeto es especialmente útil cuando se administran archivos protegidos con DRM, ya que Windows Media Administrador de dispositivos no le permitirá asociar un depurador a un proceso que controle archivos protegidos con DRM.</span><span class="sxs-lookup"><span data-stu-id="f62df-112">This object is especially useful when handling DRM-protected files, because Windows Media Device Manager will not allow you to attach a debugger to a process that is handling DRM-protected files.</span></span>

<span data-ttu-id="f62df-113">El registrador es un objeto COM con el identificador de clase CLSID \_ WMDMLogger que expone una interfaz, [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span><span class="sxs-lookup"><span data-stu-id="f62df-113">The logger is a COM object with the class ID CLSID\_WMDMLogger that exposes one interface, [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span></span> <span data-ttu-id="f62df-114">Los componentes no necesitan un certificado para usar el objeto de registro.</span><span class="sxs-lookup"><span data-stu-id="f62df-114">Components do not need a certificate to use the logging object.</span></span>

<span data-ttu-id="f62df-115">De forma predeterminada, Windows Media Administrador de dispositivos mantiene un archivo de registro, independientemente de si una aplicación usa **IWMDMLogger**.</span><span class="sxs-lookup"><span data-stu-id="f62df-115">By default, Windows Media Device Manager maintains a log file, regardless of whether an application uses **IWMDMLogger**.</span></span> <span data-ttu-id="f62df-116">Este archivo de registro es un archivo de texto simple y cada entrada incluye una entrada precedida por una marca de tiempo con el formato AAAAMMDDHHMMSS, con hora local de 24 horas.</span><span class="sxs-lookup"><span data-stu-id="f62df-116">This log file is a simple text file, and each entry includes an entry preceded by a time stamp in the format YYYYMMDDHHMMSS, using 24-hour local time.</span></span> <span data-ttu-id="f62df-117">Windows Media Administrador de dispositivos registra todas las llamadas API, junto con las entradas que agregue llamando a mensajes **IWMDMLogger** .</span><span class="sxs-lookup"><span data-stu-id="f62df-117">Windows Media Device Manager logs all API calls, along with any entries you add by calling **IWMDMLogger** messages.</span></span> <span data-ttu-id="f62df-118">Todas las entradas del archivo de registro se anexan al archivo hasta que se llama a [**RESET**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-reset) , o el archivo supera su tamaño máximo.</span><span class="sxs-lookup"><span data-stu-id="f62df-118">All log file entries are appended to the file until [**Reset**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-reset) is called, or the file exceeds its maximum size.</span></span> <span data-ttu-id="f62df-119">El archivo se cierra automáticamente después de cada operación de registro.</span><span class="sxs-lookup"><span data-stu-id="f62df-119">The file is closed automatically after each logging operation.</span></span> <span data-ttu-id="f62df-120">El mismo archivo de registro se utiliza para entradas de la aplicación y entradas del sistema.</span><span class="sxs-lookup"><span data-stu-id="f62df-120">The same log file is used for application entries and system entries.</span></span>

<span data-ttu-id="f62df-121">En los pasos siguientes se muestra cómo usar el objeto de registro:</span><span class="sxs-lookup"><span data-stu-id="f62df-121">The following steps show how to use the logging object:</span></span>

1.  <span data-ttu-id="f62df-122">Incluya wmdmlog. h en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="f62df-122">Include wmdmlog.h in your project.</span></span>
2.  <span data-ttu-id="f62df-123">Cree un objeto de registro llamando a **CoCreateInstance**(CLSID \_ WMDMLogger) y solicite la interfaz **IWMDMLogger** .</span><span class="sxs-lookup"><span data-stu-id="f62df-123">Create a logging object by calling **CoCreateInstance**(CLSID\_WMDMLogger) and requesting the **IWMDMLogger** interface.</span></span> <span data-ttu-id="f62df-124">Asigne el puntero de interfaz a una variable global.</span><span class="sxs-lookup"><span data-stu-id="f62df-124">Assign the interface pointer to a global variable.</span></span>
3.  <span data-ttu-id="f62df-125">Compruebe que el registro está habilitado mediante una llamada a [**IWMDMLogger:: IsEnabled**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-isenabled); Si no es así, habilítelo llamando a [**IWMDMLogger:: enable**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-enable).</span><span class="sxs-lookup"><span data-stu-id="f62df-125">Verify that logging is enabled by calling [**IWMDMLogger::IsEnabled**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-isenabled); if it is not, enable it by calling [**IWMDMLogger::Enable**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-enable).</span></span>
4.  <span data-ttu-id="f62df-126">Especifique un nombre y un tamaño de archivo de registro personalizados.</span><span class="sxs-lookup"><span data-stu-id="f62df-126">Specify a custom log file name and size.</span></span> <span data-ttu-id="f62df-127">Esto se hace mediante una llamada a [**IWMDMLogger:: SetLogFileName**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setlogfilename) y [**IWMDMLogger:: SetSizeParams**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setsizeparams).</span><span class="sxs-lookup"><span data-stu-id="f62df-127">This is done by calling [**IWMDMLogger::SetLogFileName**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setlogfilename) and [**IWMDMLogger::SetSizeParams**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setsizeparams).</span></span>
5.  <span data-ttu-id="f62df-128">En los puntos del código en los que desea crear una entrada en el registro, llame a [**IWMDMLogger:: LogDword**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logdword) para registrar cadenas que contengan variables (este método es similar a **wsprintf** en la forma en que le permite dar formato a una cadena que contiene un valor de variable), o llamar a [**IWMDMLogger:: LogString**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logstring) para registrar cadenas de constantes.</span><span class="sxs-lookup"><span data-stu-id="f62df-128">At points in your code where you want to make an entry in the log, call either [**IWMDMLogger::LogDword**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logdword) to log strings containing variables (this method is similar to **wsprintf** in the way it allows you to format a string containing a variable value), or call [**IWMDMLogger::LogString**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logstring) to log constant strings.</span></span>

<span data-ttu-id="f62df-129">Para ver un ejemplo de código, vea las páginas de referencia de los métodos de [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span><span class="sxs-lookup"><span data-stu-id="f62df-129">For example code, see the reference pages for the methods of [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f62df-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f62df-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f62df-131">**Tareas comunes a las aplicaciones y proveedores de servicios**</span><span class="sxs-lookup"><span data-stu-id="f62df-131">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





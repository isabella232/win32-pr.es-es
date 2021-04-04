---
description: Hay dos ejemplos de WSDAPI incluidos en el Windows SDK para Windows Server 2008.
ms.assetid: 156b79ef-1f05-4ef1-9df9-81fe81c73ca7
title: Ejemplos de WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed088c43f9617da062d5e4fb4f0343f74e3bcbc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812368"
---
# <a name="wsdapi-samples"></a><span data-ttu-id="8f5dd-103">Ejemplos de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="8f5dd-103">WSDAPI Samples</span></span>

<span data-ttu-id="8f5dd-104">Hay dos ejemplos de WSDAPI incluidos en el Windows SDK para Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-104">There are two WSDAPI samples included with the Windows SDK for Windows Server 2008.</span></span> <span data-ttu-id="8f5dd-105">El código fuente de los ejemplos se puede encontrar en <Windows SDK Install Folder> \\ ejemplos \\ Web \\ WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-105">The source code for the samples can be found in <Windows SDK Install Folder>\\Samples\\Web\\WSDAPI.</span></span> <span data-ttu-id="8f5dd-106">Esta versión del SDK está disponible en el [centro de descarga](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span><span class="sxs-lookup"><span data-stu-id="8f5dd-106">This version of the SDK is available from the [Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span></span> <span data-ttu-id="8f5dd-107">Los ejemplos no están disponibles en el SDK de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-107">The samples are not available in the Windows Vista SDK.</span></span>

<span data-ttu-id="8f5dd-108">El ejemplo stock quote (que se encuentra en <Windows SDK Install Folder> \\ Samples \\ Web \\ WSDAPI \\ StockQuote) muestra un servicio con funcionalidad básica de mensajería.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-108">The stock quote sample (located in <Windows SDK Install Folder>\\Samples\\Web\\WSDAPI\\StockQuote) demonstrates a service with basic messaging functionality.</span></span> <span data-ttu-id="8f5dd-109">El ejemplo de servicio de archivo ( <Windows SDK Install Folder> \\ que se encuentra en ejemplos \\ Web \\ WSDAPI \\ FileService) muestra un servicio con funcionalidad avanzada, como mensajería asincrónica, datos adjuntos y eventos.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-109">The file service sample (located in <Windows SDK Install Folder>\\Samples\\Web\\WSDAPI\\FileService) demonstrates a service with advanced functionality, such as asynchronous messaging, attachments, and eventing.</span></span>

<span data-ttu-id="8f5dd-110">Ambos ejemplos incluyen los siguientes tipos de archivos.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-110">Both samples include the following types of files.</span></span>

-   <span data-ttu-id="8f5dd-111">Archivos WSDL que contienen las descripciones del servicio.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-111">WSDL files that contain the service descriptions.</span></span>
-   <span data-ttu-id="8f5dd-112">[Archivos de configuración de WsdCodeGen](wsdcodegen-configuration-file.md) que se usan para generar código WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-112">[WsdCodeGen configuration files](wsdcodegen-configuration-file.md) used to generate WSDAPI code.</span></span>
-   <span data-ttu-id="8f5dd-113">Archivos de encabezado y código fuente de C++ generados.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-113">Generated C++ header and source files.</span></span>
-   <span data-ttu-id="8f5dd-114">Archivos de implementación de cliente y servicio.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-114">Client and service implementation files.</span></span>
-   <span data-ttu-id="8f5dd-115">Archivos de proyecto y de solución de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-115">Visual Studio project and solution files.</span></span>

<span data-ttu-id="8f5dd-116">Ambos ejemplos implementan hosts de dispositivo ([**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)), proxy de dispositivo ([**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)) y proxy de servicio ([**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy)).</span><span class="sxs-lookup"><span data-stu-id="8f5dd-116">Both samples implement device hosts ([**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)), device proxies ([**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)), and service proxies ([**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy)).</span></span> <span data-ttu-id="8f5dd-117">Además, el ejemplo de servicio de archivo muestra el uso de mensajería asincrónica ([**IWSDAsyncCallback**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasynccallback), [**IWSDAsyncResult**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasyncresult)), datos adjuntos ([**IWSDInboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdinboundattachment), [**IWSDOutboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdoutboundattachment)) y eventos.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-117">In addition, the file service sample demonstrates the use of asynchronous messaging ([**IWSDAsyncCallback**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasynccallback), [**IWSDAsyncResult**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasyncresult)), attachments ([**IWSDInboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdinboundattachment), [**IWSDOutboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdoutboundattachment)) and eventing.</span></span>

<span data-ttu-id="8f5dd-118">Los archivos FileServiceContract. vcproj y StockQuoteContract. vcproj incluidos con los ejemplos llaman a [WsdCodeGen](web-services-for-devices-code-generator.md) para generar el encabezado y los archivos de código fuente de C++ a partir del archivo WSDL especificado en el archivo de configuración de WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-118">The FileServiceContract.vcproj and StockQuoteContract.vcproj files included with the samples call [WsdCodeGen](web-services-for-devices-code-generator.md) to generate C++ header and source files from the WSDL file specified in the WsdCodeGen configuration file.</span></span> <span data-ttu-id="8f5dd-119">Esto significa que, si se cambia el archivo de configuración WSDL o WsdCodeGen de ejemplo y se vuelve a generar el proyecto de ejemplo, WsdCodeGen genera automáticamente nuevos archivos de encabezado y de origen que reflejan los cambios.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-119">This means that if the sample WSDL or WsdCodeGen configuration file is changed and the sample project is rebuilt, WsdCodeGen automatically generates new header and source files that reflect the changes.</span></span> <span data-ttu-id="8f5dd-120">Este es el método preferido para compilar aplicaciones de WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-120">This is the preferred method for building WSDAPI applications.</span></span> <span data-ttu-id="8f5dd-121">Normalmente, se llama a WsdCodeGen desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-121">WsdCodeGen is usually called from the command line.</span></span> <span data-ttu-id="8f5dd-122">Abra el \* archivo. vcproj pertinente para ver las llamadas de la línea de comandos de WsdCodeGen de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8f5dd-122">Open the relevant \*.vcproj file to view the example WsdCodeGen command line calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f5dd-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8f5dd-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f5dd-124">Desarrollo de aplicaciones WSD en Windows</span><span class="sxs-lookup"><span data-stu-id="8f5dd-124">WSD Application Development on Windows</span></span>](wsd-application-development-on-windows.md)
</dt> </dl>

 

 




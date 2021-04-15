---
description: Cuando una aplicación habilitada para SOAP se ha exportado desde un servidor en modo proxy, los clientes que la importan pueden tener acceso automáticamente a los métodos de los componentes que contiene, de forma remota, como servicios web ofrecidos por el servidor en modo de objeto activado en el cliente (CAO). Esto le permite implementar fácilmente la funcionalidad de una aplicación COM+ a través de una red como servicio Web XML.
ms.assetid: 7f4783f7-4f53-4f0b-bb64-ae7903097d6c
title: Importar una aplicación SOAP-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9faca91a726caea765d4b2ca227ddba0ff3a2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539303"
---
# <a name="importing-a-soap-enabled-application"></a><span data-ttu-id="a2bfa-104">Importar una aplicación SOAP-Enabled</span><span class="sxs-lookup"><span data-stu-id="a2bfa-104">Importing a SOAP-Enabled Application</span></span>

<span data-ttu-id="a2bfa-105">Cuando una aplicación habilitada para SOAP se ha [exportado](exporting-a-soap-enabled-application.md) desde un servidor en modo proxy, los clientes que la importan pueden tener acceso automáticamente a los métodos de los componentes que contiene, de forma remota, como servicios web ofrecidos por el servidor en modo de objeto activado en el cliente (CaO).</span><span class="sxs-lookup"><span data-stu-id="a2bfa-105">When a SOAP-enabled application has been [exported](exporting-a-soap-enabled-application.md) from a server in proxy mode, clients that import it can automatically access the methods of the components it contains, remotely, as web services offered by the server in client-activated object (CAO) mode.</span></span> <span data-ttu-id="a2bfa-106">Esto le permite implementar fácilmente la funcionalidad de una aplicación COM+ a través de una red como servicio Web XML.</span><span class="sxs-lookup"><span data-stu-id="a2bfa-106">This allows you to very easily deploy the functionality of a COM+ application across a network as an XML web service.</span></span>

<span data-ttu-id="a2bfa-107">Cuando se utilizan en el cliente los componentes de una aplicación importada de esta manera, no se ejecutan en el cliente, sino que se accede a ellos de forma remota mediante el servicio Web XML proporcionado por el servidor desde el que se exportó la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a2bfa-107">When the components of an application imported in this way are used on the client, they do not run on the client but instead are accessed remotely by using the XML web service provided by the server from which the application was exported.</span></span> <span data-ttu-id="a2bfa-108">Para obtener información detallada sobre el uso de los componentes de una aplicación importada de esta manera, vea [obtener acceso a los servicios Web XML en el modo de Cao](accessing-xml-web-services-in-cao-mode.md).</span><span class="sxs-lookup"><span data-stu-id="a2bfa-108">For details on using the components of an application imported in this way, see [Accessing XML Web Services in CAO Mode](accessing-xml-web-services-in-cao-mode.md).</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="a2bfa-109">Herramienta administrativa Servicios de componentes</span><span class="sxs-lookup"><span data-stu-id="a2bfa-109">Component Services Administrative Tool</span></span>

<span data-ttu-id="a2bfa-110">Para importar una aplicación habilitada para SOAP en un cliente de, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="a2bfa-110">To import a SOAP-enabled application into a client, use the following steps:</span></span>

1.  <span data-ttu-id="a2bfa-111">En el árbol de consola de la herramienta administrativa Servicios de componentes, en **servicios de componentes**, abra la carpeta asociada al equipo cliente en el que desea instalar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a2bfa-111">In the console tree of the Component Services administrative tool, under **Component Services**, open the folder associated with the client computer on which you want to install the application.</span></span>

2.  <span data-ttu-id="a2bfa-112">Haga clic con el botón secundario en la carpeta **aplicaciones com+** del cliente y elija **nuevo**.</span><span class="sxs-lookup"><span data-stu-id="a2bfa-112">Right-click the client's **COM+ Applications** folder, and then choose **New**.</span></span> <span data-ttu-id="a2bfa-113">Aparece el **Asistente para instalación de aplicaciones com+** .</span><span class="sxs-lookup"><span data-stu-id="a2bfa-113">The **COM+ Application Install Wizard** appears.</span></span>

3.  <span data-ttu-id="a2bfa-114">En el **Asistente para instalación de aplicaciones com+**, haga clic en **instalar aplicaciones creadas previamente**.</span><span class="sxs-lookup"><span data-stu-id="a2bfa-114">In the **COM+ Application Install Wizard**, click **Install pre-built application(s)**.</span></span>

4.  <span data-ttu-id="a2bfa-115">Examine la red para buscar o especificar la ruta de acceso de red del archivo MSI en el servidor desde el que desea instalar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a2bfa-115">Browse the network to locate or specify the network path of the MSI file on the server from which you want to install the application.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="a2bfa-116">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="a2bfa-116">Visual Basic</span></span>

<span data-ttu-id="a2bfa-117">No corresponde.</span><span class="sxs-lookup"><span data-stu-id="a2bfa-117">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="a2bfa-118">C/C++</span><span class="sxs-lookup"><span data-stu-id="a2bfa-118">C/C++</span></span>

<span data-ttu-id="a2bfa-119">No corresponde.</span><span class="sxs-lookup"><span data-stu-id="a2bfa-119">Does not apply.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2bfa-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2bfa-120">Remarks</span></span>

<span data-ttu-id="a2bfa-121">Los componentes COM se identifican mediante un GUID, que cambia si se vuelven a compilar los componentes.</span><span class="sxs-lookup"><span data-stu-id="a2bfa-121">COM components are identified by a GUID, which changes if the components are recompiled.</span></span> <span data-ttu-id="a2bfa-122">Si se vuelve a compilar un componente COM configurado que se expone como un servicio Web XML, las aplicaciones cliente que lo utilicen se interrumpirán.</span><span class="sxs-lookup"><span data-stu-id="a2bfa-122">If a configured COM component that is exposed as an XML web service is recompiled, client applications that use it will break.</span></span> <span data-ttu-id="a2bfa-123">Por lo tanto, cuando se vuelve a compilar un componente que se expone como un servicio Web XML, los clientes deben volver a importar las aplicaciones que usan el componente.</span><span class="sxs-lookup"><span data-stu-id="a2bfa-123">Therefore, when a component that is exposed as an XML web service is recompiled, clients should re-import the applications that use the component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2bfa-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a2bfa-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2bfa-125">Introducción al servicio SOAP de COM+</span><span class="sxs-lookup"><span data-stu-id="a2bfa-125">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="a2bfa-126">Crear servicios Web XML</span><span class="sxs-lookup"><span data-stu-id="a2bfa-126">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="a2bfa-127">Exportar una aplicación SOAP-Enabled</span><span class="sxs-lookup"><span data-stu-id="a2bfa-127">Exporting a SOAP-Enabled Application</span></span>](exporting-a-soap-enabled-application.md)
</dt> </dl>

 

 




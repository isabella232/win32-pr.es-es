---
description: Cuando se utiliza COM+ para crear un servicio Web XML, el servicio puede ser utilizado por cualquier cliente autorizado, incluidos los que no usan COM+ ni siquiera Microsoft Windows.
ms.assetid: c40031a6-f3de-4ef4-b9aa-3f49e57da5b4
title: Exportar una aplicación SOAP-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5c92029f431fc06964f233c5746c283821d11c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907352"
---
# <a name="exporting-a-soap-enabled-application"></a><span data-ttu-id="a2a70-103">Exportar una aplicación SOAP-Enabled</span><span class="sxs-lookup"><span data-stu-id="a2a70-103">Exporting a SOAP-Enabled Application</span></span>

<span data-ttu-id="a2a70-104">Cuando se utiliza COM+ para crear un servicio Web XML, el servicio puede ser utilizado por cualquier cliente autorizado, incluidos los que no usan COM+ ni siquiera Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a2a70-104">When you use COM+ to create an XML web service, that service can be used by any authorized client, including those not using COM+ or even Microsoft Windows.</span></span> <span data-ttu-id="a2a70-105">Sin embargo, el uso de un servicio Web COM+ en el modo de objetos activados en el cliente (CAO) desde una aplicación cliente COM+ es especialmente fácil.</span><span class="sxs-lookup"><span data-stu-id="a2a70-105">However, using a COM+ web service in client-activated object (CAO) mode from a COM+ client application is especially easy.</span></span> <span data-ttu-id="a2a70-106">Simplemente exporte la aplicación habilitada para SOAP en modo proxy y, a continuación, [impórtela](importing-a-soap-enabled-application.md) en el cliente para el que desea obtener acceso al servicio Web XML correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a2a70-106">Just export the SOAP-enabled application in proxy mode, and then [import](importing-a-soap-enabled-application.md) it into the client for which you want to access the corresponding XML web service.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="a2a70-107">Herramienta administrativa Servicios de componentes</span><span class="sxs-lookup"><span data-stu-id="a2a70-107">Component Services Administrative Tool</span></span>

<span data-ttu-id="a2a70-108">Para exportar una aplicación habilitada para SOAP desde un servidor, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="a2a70-108">To export a SOAP-enabled application from a server, use the following steps:</span></span>

1.  <span data-ttu-id="a2a70-109">En el árbol de consola de la herramienta administrativa Servicios de componentes, en **servicios de componentes**, abra la carpeta **aplicaciones com+** asociada con el equipo que desea administrar.</span><span class="sxs-lookup"><span data-stu-id="a2a70-109">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you want to manage.</span></span>

2.  <span data-ttu-id="a2a70-110">Haga clic con el botón secundario en el componente que desee exponer como un servicio Web XML y elija **exportar**.</span><span class="sxs-lookup"><span data-stu-id="a2a70-110">Right-click the component you want to expose as an XML web service, and choose **Export**.</span></span> <span data-ttu-id="a2a70-111">Aparece el **Asistente para la exportación de aplicaciones com+** .</span><span class="sxs-lookup"><span data-stu-id="a2a70-111">The **COM+ Application Export Wizard** appears.</span></span>

3.  <span data-ttu-id="a2a70-112">En el cuadro de texto con la etiqueta **Escriba la ruta de acceso completa y el nombre del archivo de la aplicación que se va a crear**, escriba la ruta de acceso completa y el nombre del archivo MSI que contendrá la aplicación exportada, o haga clic en **examinar** para seleccionar la ruta de acceso completa y el nombre de archivo mediante un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a2a70-112">In the text box labeled **Enter the full path and filename for the application file to be created**, enter the full path and filename for the MSI file that will contain the exported application, or click **Browse** to select the full path and filename using a dialog box.</span></span>

4.  <span data-ttu-id="a2a70-113">En **exportar como**, seleccione el botón de radio **aplicación proxy: instalar en otros equipos para habilitar el acceso a este equipo** .</span><span class="sxs-lookup"><span data-stu-id="a2a70-113">Under **Export As**, select the **Application Proxy – Install on other machines to enable access to this machine** radio button.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="a2a70-114">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="a2a70-114">Visual Basic</span></span>

<span data-ttu-id="a2a70-115">No corresponde.</span><span class="sxs-lookup"><span data-stu-id="a2a70-115">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="a2a70-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="a2a70-116">C/C++</span></span>

<span data-ttu-id="a2a70-117">No corresponde.</span><span class="sxs-lookup"><span data-stu-id="a2a70-117">Does not apply.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2a70-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a2a70-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2a70-119">Introducción al servicio SOAP de COM+</span><span class="sxs-lookup"><span data-stu-id="a2a70-119">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="a2a70-120">Crear servicios Web XML</span><span class="sxs-lookup"><span data-stu-id="a2a70-120">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="a2a70-121">Importar una aplicación SOAP-Enabled</span><span class="sxs-lookup"><span data-stu-id="a2a70-121">Importing a SOAP-Enabled Application</span></span>](importing-a-soap-enabled-application.md)
</dt> </dl>

 

 




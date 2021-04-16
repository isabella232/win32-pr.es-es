---
title: Configuración del servicio de nombres
description: A partir de Windows 2000, al instalar el Windows SDK, el programa de instalación selecciona automáticamente Microsoft Locator como proveedor de servicio de nombres. Puede cambiar el proveedor de servicios de nombres a través del panel de control.
ms.assetid: bd72ca2f-bb93-4057-a877-be755a88719d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c1c895aecb3bdf74189461cd6aa9ee814b2d68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486778"
---
# <a name="configuring-the-name-service"></a><span data-ttu-id="bd7f7-104">Configuración del servicio de nombres</span><span class="sxs-lookup"><span data-stu-id="bd7f7-104">Configuring the Name Service</span></span>

<span data-ttu-id="bd7f7-105">A partir de Windows 2000, al instalar el Windows SDK, el programa de instalación selecciona automáticamente Microsoft Locator como proveedor de servicio de nombres.</span><span class="sxs-lookup"><span data-stu-id="bd7f7-105">Starting with Windows 2000, when you install the Windows SDK, the setup program automatically selects Microsoft Locator as the name service provider.</span></span> <span data-ttu-id="bd7f7-106">Puede cambiar el proveedor de servicios de nombres a través del panel de control.</span><span class="sxs-lookup"><span data-stu-id="bd7f7-106">You can change the name service provider through Control Panel.</span></span>

<span data-ttu-id="bd7f7-107">El equipo host que ejecuta NSID actúa como puerta de enlace al Servicio de directorio de celdas de DCE, pasando llamadas a la función NSI entre equipos que ejecutan sistemas operativos de Microsoft y equipos DCE.</span><span class="sxs-lookup"><span data-stu-id="bd7f7-107">The host computer that runs the nsid acts as a gateway to the DCE Cell Directory Service, passing NSI function calls between computers that run Microsoft operating systems and DCE computers.</span></span> <span data-ttu-id="bd7f7-108">Una dirección de red puede tener hasta 80 caracteres, por ejemplo, 11.1.9.169 es una dirección válida.</span><span class="sxs-lookup"><span data-stu-id="bd7f7-108">A network address can be up to 80 characters—for example, 11.1.9.169 is a valid address.</span></span>

> [!Note]  
> <span data-ttu-id="bd7f7-109">Para configurar los CD de DCE como proveedor de servicios de nombres, debe tener el producto de los CD de DCE de Digital Equipment Corporation.</span><span class="sxs-lookup"><span data-stu-id="bd7f7-109">You must have the Digital Equipment Corporation DCE CDS product to configure the DCE CDS as your name service provider.</span></span> <span data-ttu-id="bd7f7-110">Consulte la documentación proporcionada por Digital Equipment Corporation para obtener información acerca de los CD de DCE.</span><span class="sxs-lookup"><span data-stu-id="bd7f7-110">See the documentation provided by Digital Equipment Corporation for information about DCE CDS.</span></span>

 

<span data-ttu-id="bd7f7-111">**Para volver a configurar el proveedor de servicios de nombres**</span><span class="sxs-lookup"><span data-stu-id="bd7f7-111">**To reconfigure the name service provider**</span></span>

1.  <span data-ttu-id="bd7f7-112">En el panel de control, haga clic en el icono **conexiones de red** .</span><span class="sxs-lookup"><span data-stu-id="bd7f7-112">In Control Panel, click the **Network Connections** icon.</span></span> <span data-ttu-id="bd7f7-113">Aparece la ventana **conexiones de red** .</span><span class="sxs-lookup"><span data-stu-id="bd7f7-113">The **Network Connections** window appears.</span></span>
2.  <span data-ttu-id="bd7f7-114">Seleccione la conexión de red que desea configurar, haga clic con el botón secundario y seleccione **propiedades** en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="bd7f7-114">Select the network connection to configure, right-click, and select **Properties** from the context menu.</span></span> <span data-ttu-id="bd7f7-115">Aparece el cuadro de diálogo Propiedades de la **conexión** .</span><span class="sxs-lookup"><span data-stu-id="bd7f7-115">The **Connection Properties** dialog appears.</span></span>
3.  <span data-ttu-id="bd7f7-116">En el cuadro de diálogo **propiedades de conexión** , seleccione **cliente para redes de Microsoft** y haga clic en el botón **propiedades** .</span><span class="sxs-lookup"><span data-stu-id="bd7f7-116">In the **Connection Properties** dialog, select **Client for Microsoft Networks** and click the **Properties** button.</span></span> <span data-ttu-id="bd7f7-117">Aparece el cuadro **de diálogo Propiedades de cliente para Microsoft Network** .</span><span class="sxs-lookup"><span data-stu-id="bd7f7-117">The **Client for Microsoft Network Properties** dialog appears.</span></span>
4.  <span data-ttu-id="bd7f7-118">En el cuadro de diálogo **propiedades de cliente para Microsoft Network** , abra el menú desplegable **proveedor de servicios de nombres** y seleccione un proveedor de nombres de la lista.</span><span class="sxs-lookup"><span data-stu-id="bd7f7-118">In the **Client for Microsoft Network Properties** dialog, open the **Name service provider** drop-down and select a name provider from the list.</span></span>
    1.  <span data-ttu-id="bd7f7-119">Al seleccionar localizador de Microsoft, haga clic en Aceptar.</span><span class="sxs-lookup"><span data-stu-id="bd7f7-119">When you select Microsoft Locator, click OK.</span></span> <span data-ttu-id="bd7f7-120">A continuación, se completa el proceso de configuración.</span><span class="sxs-lookup"><span data-stu-id="bd7f7-120">The configuration process is then complete.</span></span>
    2.  <span data-ttu-id="bd7f7-121">Al seleccionar el Servicio de directorio de celdas DCE, en el cuadro **dirección de red** , escriba el nombre del equipo host que ejecuta el demonio NSI (NSID) y, a continuación, haga clic en Aceptar.</span><span class="sxs-lookup"><span data-stu-id="bd7f7-121">When you select the DCE Cell Directory Service, in the **Network Address** box, type the name of the host computer that runs the NSI daemon (nsid), and then click OK.</span></span>

<span data-ttu-id="bd7f7-122">**Para volver a configurar el proveedor de servicios de nombres para Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="bd7f7-122">**To reconfigure the name service provider for Windows 2000**</span></span>

1.  <span data-ttu-id="bd7f7-123">En el panel de control, haga clic en el icono **red** .</span><span class="sxs-lookup"><span data-stu-id="bd7f7-123">In Control Panel, click the **Network** icon.</span></span>

    <span data-ttu-id="bd7f7-124">Aparece el cuadro de diálogo **red** .</span><span class="sxs-lookup"><span data-stu-id="bd7f7-124">The **Network** dialog box appears.</span></span>

2.  <span data-ttu-id="bd7f7-125">En el cuadro de diálogo **red** , haga clic en **configurar**.</span><span class="sxs-lookup"><span data-stu-id="bd7f7-125">In the **Network** dialog box, click **Configure**.</span></span>
3.  <span data-ttu-id="bd7f7-126">En la lista **NetworkSoftware** , seleccione **configuración de RPC**.</span><span class="sxs-lookup"><span data-stu-id="bd7f7-126">In the **NetworkSoftware** list, select **RPC Configuration**.</span></span>

    <span data-ttu-id="bd7f7-127">Aparece el cuadro de diálogo **configuración de proveedor de servicio de nombres de RPC** .</span><span class="sxs-lookup"><span data-stu-id="bd7f7-127">The **RPC Name Service Provider Configuration** dialog box appears.</span></span>

4.  <span data-ttu-id="bd7f7-128">En el cuadro de diálogo **configuración de proveedor de servicio de nombres RPC** , seleccione un proveedor de servicios de nombres de la lista.</span><span class="sxs-lookup"><span data-stu-id="bd7f7-128">In the **RPC Name Service Provider Configuration** dialog box, select a name service provider from the list.</span></span>
    1.  <span data-ttu-id="bd7f7-129">Al seleccionar localizador de Microsoft, haga clic en Aceptar.</span><span class="sxs-lookup"><span data-stu-id="bd7f7-129">When you select Microsoft Locator, click OK.</span></span> <span data-ttu-id="bd7f7-130">A continuación, se completa el proceso de configuración.</span><span class="sxs-lookup"><span data-stu-id="bd7f7-130">The configuration process is then complete.</span></span>
    2.  <span data-ttu-id="bd7f7-131">Al seleccionar el Servicio de directorio de celdas DCE, en el cuadro **dirección de red** , escriba el nombre del equipo host que ejecuta el demonio NSI (NSID) y, a continuación, haga clic en Aceptar.</span><span class="sxs-lookup"><span data-stu-id="bd7f7-131">When you select the DCE Cell Directory Service, in the **Network Address** box, type the name of the host computer that runs the NSI daemon (nsid), and then click OK.</span></span>

 

 





---
title: Requisitos de IIS para cargas de BITS
description: En el caso de las cargas, BITS requiere IIS 6,0 en Windows Server 2003 y IIS 7,0 en Windows Server 2008; BITS no admite IIS 5,1 en Windows XP.
ms.assetid: 8ab07af5-3b59-4c98-8e57-f614deb8b594
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fc1eb9bae86e7bb2635b3a250e8a9efe1bc630
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773656"
---
# <a name="iis-requirements-for-bits-uploads"></a><span data-ttu-id="68e34-103">Requisitos de IIS para cargas de BITS</span><span class="sxs-lookup"><span data-stu-id="68e34-103">IIS Requirements for BITS Uploads</span></span>

<span data-ttu-id="68e34-104">En el caso de las cargas, BITS requiere IIS 6,0 en Windows Server 2003 y IIS 7,0 en Windows Server 2008; BITS no admite IIS 5,1 en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="68e34-104">For uploads, BITS requires IIS 6.0 on Windows Server 2003, and IIS 7.0 on Windows Server 2008; BITS does not support IIS 5.1 on Windows XP.</span></span> <span data-ttu-id="68e34-105">El directorio virtual de IIS debe estar habilitado para cargas y tener las extensiones de IIS de BITS configuradas.</span><span class="sxs-lookup"><span data-stu-id="68e34-105">The IIS virtual directory must be enabled for uploads and have the BITS IIS extensions configured.</span></span>

<span data-ttu-id="68e34-106">**Instalaciones básicas de Windows Server:** No se admiten las extensiones de IIS de BITS.</span><span class="sxs-lookup"><span data-stu-id="68e34-106">**Core installations of Windows Server:** BITS IIS extensions are not supported.</span></span>

<span data-ttu-id="68e34-107">En Windows Server 2008, use el **Administrador del servidor** para instalar la característica extensiones de servidor bits.</span><span class="sxs-lookup"><span data-stu-id="68e34-107">On Windows Server 2008, use the **Server Manager** to install the BITS Server Extensions feature.</span></span> <span data-ttu-id="68e34-108">En **Administrador del servidor**, haga clic en **características** en el panel izquierdo.</span><span class="sxs-lookup"><span data-stu-id="68e34-108">From **Server Manager**, click **Features** in the left pane.</span></span> <span data-ttu-id="68e34-109">En el **Asistente para agregar características**, compruebe extensiones de servidor bits.</span><span class="sxs-lookup"><span data-stu-id="68e34-109">In the **Add Features Wizard**, check BITS Server Extensions.</span></span> <span data-ttu-id="68e34-110">Tenga en cuenta que los roles de compatibilidad con la administración de IIS 6 deben estar instalados.</span><span class="sxs-lookup"><span data-stu-id="68e34-110">Note that the IIS 6 Management Compatibility roles must be installed.</span></span>

<span data-ttu-id="68e34-111">En Windows Server 2003, use el **Asistente para componentes de Windows** para instalar la extensión de servidor bits.</span><span class="sxs-lookup"><span data-stu-id="68e34-111">On Windows Server 2003, use the **Windows Components Wizard** to install the BITS server extension.</span></span> <span data-ttu-id="68e34-112">En el **Panel de control**, seleccione **Agregar o quitar programas**.</span><span class="sxs-lookup"><span data-stu-id="68e34-112">From **Control Panel**, select **Add or Remove Programs**.</span></span> <span data-ttu-id="68e34-113">A continuación, seleccione **Agregar o quitar componentes de Windows** para mostrar el **Asistente para componentes de Windows**.</span><span class="sxs-lookup"><span data-stu-id="68e34-113">Then, select **Add/Remove Windows Components** to display the **Windows Components Wizard**.</span></span> <span data-ttu-id="68e34-114">La extensión de servidor BITS es un subcomponente de Internet Information Services (IIS), que es un subcomponente del servidor de aplicaciones Web.</span><span class="sxs-lookup"><span data-stu-id="68e34-114">The BITS server extension is a subcomponent of Internet Information Services (IIS) which is a sub-component of Web Application Server.</span></span>

> [!Note]  
> <span data-ttu-id="68e34-115">Si se reinicia el servicio IISAdmin, el proceso de trabajo de IIS se debe reciclar antes de que el servicio BITS pueda reanudar las cargas.</span><span class="sxs-lookup"><span data-stu-id="68e34-115">If the IISAdmin service is restarted, the IIS worker process must be recycled before the BITS service can resume uploads.</span></span> <span data-ttu-id="68e34-116">El proceso de trabajo de IIS se puede reciclar manualmente mediante la utilidad de línea de comandos **IISReset.exe** .</span><span class="sxs-lookup"><span data-stu-id="68e34-116">The IIS worker process can be manually recycled by using the **IISReset.exe** command line utility.</span></span>

 

<span data-ttu-id="68e34-117">Para obtener información sobre cómo configurar IIS para cargas, consulte [configuración del servidor para cargas](setting-up-the-server-for-uploads.md).</span><span class="sxs-lookup"><span data-stu-id="68e34-117">For information on configuring IIS for uploads, see [Setting Up the Server for Uploads](setting-up-the-server-for-uploads.md).</span></span>

<span data-ttu-id="68e34-118">Para obtener más información sobre las propiedades que BITS agrega a IIS, consulte [configuración del servidor bits para trabajos de carga](bits-server-settings-for-upload-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="68e34-118">For details on the properties that BITS adds to IIS, see [BITS Server Settings for Upload Jobs](bits-server-settings-for-upload-jobs.md).</span></span>

 

 





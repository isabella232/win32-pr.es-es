---
title: Conexión web a Escritorio remoto
description: Conexión web a Escritorio remoto es una aplicación web formada por un control ActiveX y una página de conexión de ejemplo.
ms.assetid: f9d252b0-205a-47df-9eca-d5744c09e079
ms.tgt_platform: multiple
keywords:
- Conexión web a Escritorio remoto Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Protocolo de escritorio remoto (RDP), información general sobre Conexión web a Escritorio remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bb1e8f562e3e5c47c6050f550fe3c7090446be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676419"
---
# <a name="remote-desktop-web-connection"></a><span data-ttu-id="a7e8c-105">Conexión web a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="a7e8c-105">Remote Desktop Web Connection</span></span>

<span data-ttu-id="a7e8c-106">Conexión web a Escritorio remoto es una aplicación web formada por un control ActiveX y una página de conexión de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a7e8c-106">Remote Desktop Web Connection is a web application consisting of an ActiveX control and a sample connection page.</span></span> <span data-ttu-id="a7e8c-107">Al implementar Conexión web a Escritorio remoto en un servidor Web, puede proporcionar conectividad de cliente a los servidores host de sesión de Escritorio remoto (host de sesión de escritorio remoto) y a otros equipos con Internet Explorer y TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="a7e8c-107">When you deploy Remote Desktop Web Connection on a web server, you can provide client connectivity to Remote Desktop Session Host (RD Session Host) servers and other computers using Internet Explorer and TCP/IP.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a7e8c-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="a7e8c-108">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="a7e8c-109">Requisitos para Conexión web a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="a7e8c-109">Requirements for Remote Desktop Web Connection</span></span>](requirements-for-remote-desktop-web-connection.md)
</dt> <dd>

<span data-ttu-id="a7e8c-110">Enumera los requisitos de un Conexión web a Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="a7e8c-110">Lists the requirements for a Remote Desktop Web Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="a7e8c-111">Canales virtuales con scripts</span><span class="sxs-lookup"><span data-stu-id="a7e8c-111">Scriptable virtual channels</span></span>](scriptable-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="a7e8c-112">Describe los cambios en el modelo de programación para implementar aplicaciones de canal virtual proporcionadas por el Terminal Services Cliente avanzado (TSAC).</span><span class="sxs-lookup"><span data-stu-id="a7e8c-112">Describes changes to the programming model for implementing virtual channel applications that are provided by the Terminal Services Advanced Client (TSAC).</span></span>

</dd> </dl>

<span data-ttu-id="a7e8c-113">El material de referencia de Conexión web a Escritorio remoto se incluye en la sección de [referencia de conexión web a escritorio remoto](remote-desktop-web-connection-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="a7e8c-113">The reference material for Remote Desktop Web Connection is included in the [Remote Desktop Web Connection Reference](remote-desktop-web-connection-reference.md) section.</span></span>

<span data-ttu-id="a7e8c-114">Para más información, consulte los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="a7e8c-114">For more information, see these topics:</span></span>

-   [<span data-ttu-id="a7e8c-115">Implementación de canales virtuales con scripts mediante Conexión web a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="a7e8c-115">Implementing Scriptable Virtual Channels Using Remote Desktop Web Connection</span></span>](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)
-   [<span data-ttu-id="a7e8c-116">Incrustar el control ActiveX Escritorio remoto en una página web</span><span class="sxs-lookup"><span data-stu-id="a7e8c-116">Embedding the Remote Desktop ActiveX Control in a Webpage</span></span>](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
-   <span data-ttu-id="a7e8c-117">[Descargar y usar el control ActiveX Escritorio remoto](/previous-versions//aa380808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a7e8c-117">[Downloading and Using the Remote Desktop ActiveX Control](/previous-versions//aa380808(v=vs.85))</span></span>
-   [<span data-ttu-id="a7e8c-118">Usar el control ActiveX Escritorio remoto con canales virtuales</span><span class="sxs-lookup"><span data-stu-id="a7e8c-118">Using the Remote Desktop ActiveX Control with Virtual Channels</span></span>](using-the-remote-desktop-activex-control-with-virtual-channels.md)
-   [<span data-ttu-id="a7e8c-119">Proporcionar seguridad de cliente RDP</span><span class="sxs-lookup"><span data-stu-id="a7e8c-119">Providing for RDP Client Security</span></span>](providing-for-rdp-client-security.md)
-   [<span data-ttu-id="a7e8c-120">Deshabilitar características de Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="a7e8c-120">Disabling Remote Desktop Services Features</span></span>](disabling-terminal-services-features.md)

## <a name="installing-remote-desktop-web-connection"></a><span data-ttu-id="a7e8c-121">Instalación de Conexión web a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="a7e8c-121">Installing Remote Desktop Web Connection</span></span>

<span data-ttu-id="a7e8c-122">En los pasos siguientes se instala el control ActiveX de Escritorio remoto y la Página Web de ejemplo en el directorio% SystemRoot% \\ Web \\ TSWeb.</span><span class="sxs-lookup"><span data-stu-id="a7e8c-122">The following steps install the Remote Desktop ActiveX control and sample webpage to the %systemroot%\\Web\\Tsweb directory.</span></span> <span data-ttu-id="a7e8c-123">Comparten la página web en el directorio TSWeb del servidor, por ejemplo,*en https:///TSWeb.*</span><span class="sxs-lookup"><span data-stu-id="a7e8c-123">They share the webpage in the Tsweb directory on your server, for example, at https://*MyServer*/tsweb.</span></span> <span data-ttu-id="a7e8c-124">El control (Msrdp. ocx) y el código Conexión web a Escritorio remoto se encuentran en Msrdp.cab.</span><span class="sxs-lookup"><span data-stu-id="a7e8c-124">The control (Msrdp.ocx) and the Remote Desktop Web Connection code are located in Msrdp.cab.</span></span>

<span data-ttu-id="a7e8c-125">**Para instalar Conexión web a Escritorio remoto**</span><span class="sxs-lookup"><span data-stu-id="a7e8c-125">**To install Remote Desktop Web Connection**</span></span>

1.  <span data-ttu-id="a7e8c-126">En el elemento agregar o quitar programas del panel de control, en Agregar o quitar componentes de Windows, instale Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="a7e8c-126">In the Add/Remove Programs item in Control Panel, under Add/Remove Windows Components, install Microsoft Internet Information Services (IIS).</span></span>
2.  <span data-ttu-id="a7e8c-127">Instale el subcomponente servicio de World Wide Web de IIS.</span><span class="sxs-lookup"><span data-stu-id="a7e8c-127">Install the World Wide Web Service subcomponent of IIS.</span></span>
3.  <span data-ttu-id="a7e8c-128">Instale el subcomponente Conexión web a Escritorio remoto del servicio World Wide Web.</span><span class="sxs-lookup"><span data-stu-id="a7e8c-128">Install the Remote Desktop Web Connection subcomponent of World Wide Web Service.</span></span>

<span data-ttu-id="a7e8c-129">Para obtener una descripción de la página web que se incluye con la instalación de Conexión web a Escritorio remoto, vea [Página Web de ejemplo que se incluye con el control ActiveX escritorio remoto](sample-web-page-included-with-the-remote-desktop-activex-control.md).</span><span class="sxs-lookup"><span data-stu-id="a7e8c-129">For a description of the webpage that is included with the installation of Remote Desktop Web Connection, see [Sample Webpage Included with the Remote Desktop ActiveX Control](sample-web-page-included-with-the-remote-desktop-activex-control.md).</span></span>

 

 
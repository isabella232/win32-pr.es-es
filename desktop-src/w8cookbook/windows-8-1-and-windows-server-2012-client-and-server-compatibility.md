---
title: Compatibilidad de cliente y servidor de Windows 8.1 y Windows Server 2012 R2
description: Compatibilidad de cliente y servidor de Windows 8.1 y Windows Server 2012 R2
ms.assetid: 45C37E2D-3513-4708-A562-1426D2B832F0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c46647dd9ad0f0baeae1ffb98905740a37f9530
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531990"
---
# <a name="windows-81-and-windows-server-2012-r2-client-and-server-compatibility"></a><span data-ttu-id="c6212-103">Compatibilidad de cliente y servidor de Windows 8.1 y Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c6212-103">Windows 8.1 and Windows Server 2012 R2 client and server compatibility</span></span>

<span data-ttu-id="c6212-104">En esta sección se describen los cambios en el sistema operativo a los que debe prestar atención especial debido a los posibles impactos en las aplicaciones existentes y cómo deben diseñarse las nuevas aplicaciones en los clientes, en servidores o en clientes y servidores.</span><span class="sxs-lookup"><span data-stu-id="c6212-104">This section describes changes in the operating system that you should pay special attention to due to the potential impacts on existing apps and how new apps should be designed on clients, on servers, or on both clients and servers.</span></span> <span data-ttu-id="c6212-105">A continuación se muestra la lista de temas que se tratan en esta sección:</span><span class="sxs-lookup"><span data-stu-id="c6212-105">Following is the list of topics covered in this section:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c6212-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="c6212-106">In this section</span></span>



| <span data-ttu-id="c6212-107">Tema</span><span class="sxs-lookup"><span data-stu-id="c6212-107">Topic</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="c6212-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6212-108">Description</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| [<span data-ttu-id="c6212-109">Cambios de versión del sistema operativo en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c6212-109">Operating system version changes in Windows 8.1</span></span>](operating-system-version-changes-in-windows-8-1.md)<br/>                                                                                                             |             |
| [<span data-ttu-id="c6212-110">Componentes de Windows instalados a petición</span><span class="sxs-lookup"><span data-stu-id="c6212-110">Windows components installed on demand</span></span>](windows-components-installed-on-demand.md)<br/>                                                                                                                               |             |
| [<span data-ttu-id="c6212-111">Comportamiento de reserva de fuente HTML</span><span class="sxs-lookup"><span data-stu-id="c6212-111">HTML font fallback behavior</span></span>](html-font-fallback-behavior.md)<br/>                                                                                                                                                     |             |
| [<span data-ttu-id="c6212-112">Windows 8.1 solo permite URI https, no URI http</span><span class="sxs-lookup"><span data-stu-id="c6212-112">Windows 8.1 allows only https URIs, not http URIs</span></span>](windows-8-1-allows-only-https-uris--not-http-uris.md)<br/>                                                                                                         |             |
| [<span data-ttu-id="c6212-113">Entrada MouseWheel para Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c6212-113">Mousewheel input for Windows 8.1</span></span>](mousewheel-input-for-windows-8-1.md)<br/>                                                                                                                                           |             |
| [<span data-ttu-id="c6212-114">Dispositivos Touchpad de Windows Precision</span><span class="sxs-lookup"><span data-stu-id="c6212-114">Windows precision touchpad devices</span></span>](windows-precision-touchpad-devices.md)<br/>                                                                                                                                       |             |
| [<span data-ttu-id="c6212-115">Alta resolución de PPP para aplicaciones de escritorio en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c6212-115">High DPI for desktop apps in Windows 8.1</span></span>](high-dpi-for-desktop-apps-in-windows-8-1.md)<br/>                                                                                                                           |             |
| [<span data-ttu-id="c6212-116">La interfaz de usuario perimetral se suprime en escenarios de inercia y salida</span><span class="sxs-lookup"><span data-stu-id="c6212-116">Edge UI is suppressed in  in-out-in  and  inertia  scenarios</span></span>](edge-ui-is-suppressed-in--in-out-in--and--inertia--scenarios.md)<br/>                                                                                   |             |
| [<span data-ttu-id="c6212-117">No se admite la llamada a ImmSetConversionStatus () o ImmGetConversionStatus () desde aplicaciones de la tienda Windows</span><span class="sxs-lookup"><span data-stu-id="c6212-117">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from Windows Store apps is not supported</span></span>](calling-immsetconversionstatus---or-immgetconversionstatus---from-windows-store-apps-is-not-supported.md)<br/> |             |
| [<span data-ttu-id="c6212-118">Modelo de modo IME cambiado de por usuario a por subproceso</span><span class="sxs-lookup"><span data-stu-id="c6212-118">IME mode model changed from per-user to per-thread</span></span>](ime-mode-model-changed-from-per-user-to-per-thread.md)<br/>                                                                                                       |             |
| [<span data-ttu-id="c6212-119">El IME de chino simplificado no admite las API del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="c6212-119">Input Method manager APIs are not supported by Simplified Chinese IME</span></span>](input-method-manager-apis-are-not-supported-by-simplified-chinese-ime.md)<br/>                                                                 |             |
| [<span data-ttu-id="c6212-120">Algunos paneles de entrada del software IME de Asia Oriental ahora envían vKey</span><span class="sxs-lookup"><span data-stu-id="c6212-120">Some East Asian IME software input panels now send vKey</span></span>](some-east-asian-ime-software-input-panels-now-send-vkey.md)<br/>                                                                                             |             |



 

 

 






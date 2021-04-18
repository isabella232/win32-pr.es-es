---
title: Internet de Windows
description: La interfaz de programación de aplicaciones (API) de Microsoft Windows Internet (WinINet) permite a las aplicaciones tener acceso a los protocolos estándar de Internet, como FTP y HTTP. Para facilitar su uso, WinINet abstrae estos protocolos en una interfaz de alto nivel.
ms.assetid: 9d1856ac-f281-4582-bb70-83a8ec674914
keywords:
- Windows Internet WinINet
- WinINet WinINet, portal
- Windows Internet WinINet, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b5b76fefea900d3f187deb89929d3a09fe3c78
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488087"
---
# <a name="windows-internet"></a><span data-ttu-id="b95a8-107">Internet de Windows</span><span class="sxs-lookup"><span data-stu-id="b95a8-107">Windows Internet</span></span>

## <a name="purpose"></a><span data-ttu-id="b95a8-108">Propósito</span><span class="sxs-lookup"><span data-stu-id="b95a8-108">Purpose</span></span>

<span data-ttu-id="b95a8-109">La interfaz de programación de aplicaciones (API) de Microsoft Windows Internet (WinINet) permite a las aplicaciones tener acceso a los protocolos estándar de Internet, como FTP y HTTP.</span><span class="sxs-lookup"><span data-stu-id="b95a8-109">The Microsoft Windows Internet (WinINet) application programming interface (API) enables applications to access standard Internet protocols, such as FTP and HTTP.</span></span> <span data-ttu-id="b95a8-110">Para facilitar su uso, WinINet abstrae estos protocolos en una interfaz de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="b95a8-110">For ease of use, WinINet abstracts these protocols into a high-level interface.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="b95a8-111">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="b95a8-111">Where applicable</span></span>

<span data-ttu-id="b95a8-112">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="b95a8-112">WinINet does not support server implementations.</span></span> <span data-ttu-id="b95a8-113">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="b95a8-113">In addition, it should not be used from a service.</span></span> <span data-ttu-id="b95a8-114">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="b95a8-114">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="b95a8-115">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="b95a8-115">Developer audience</span></span>

<span data-ttu-id="b95a8-116">WinINet está diseñado para que lo usen los programadores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="b95a8-116">WinINet is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="b95a8-117">Requiere un conocimiento básico de los protocolos FTP y HTTP.</span><span class="sxs-lookup"><span data-stu-id="b95a8-117">It requires a basic understanding of the FTP and HTTP protocols.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="b95a8-118">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="b95a8-118">Run-time requirements</span></span>

<span data-ttu-id="b95a8-119">Las aplicaciones que utilizan la API WinINet requieren Windows NT 4,0 o posterior, o Windows Me/98/95.</span><span class="sxs-lookup"><span data-stu-id="b95a8-119">Applications that use the WinINet API require Windows NT 4.0 or later, or Windows Me/98/95.</span></span> <span data-ttu-id="b95a8-120">Para obtener más información sobre qué sistemas operativos o componentes son necesarios para usar un elemento de programación determinado, consulte la sección de requisitos de la documentación.</span><span class="sxs-lookup"><span data-stu-id="b95a8-120">For more information about which operating systems or components are required to use a particular programming element, see the Requirements section of the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b95a8-121">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b95a8-121">In this section</span></span>



| <span data-ttu-id="b95a8-122">Tema</span><span class="sxs-lookup"><span data-stu-id="b95a8-122">Topic</span></span>                                                          | <span data-ttu-id="b95a8-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="b95a8-123">Description</span></span>                                                      |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="b95a8-124">Acerca de Windows Internet</span><span class="sxs-lookup"><span data-stu-id="b95a8-124">About Windows Internet</span></span>](about-wininet.md)<br/>         | <span data-ttu-id="b95a8-125">Información general sobre la API de Internet de Windows.</span><span class="sxs-lookup"><span data-stu-id="b95a8-125">General information about the Windows Internet API.</span></span><br/>   |
| [<span data-ttu-id="b95a8-126">Usar Internet de Windows</span><span class="sxs-lookup"><span data-stu-id="b95a8-126">Using Windows Internet</span></span>](using-wininet.md)<br/>         | <span data-ttu-id="b95a8-127">Guía de programación de la API de Internet de Windows.</span><span class="sxs-lookup"><span data-stu-id="b95a8-127">Programming guide for the Windows Internet API.</span></span><br/>       |
| [<span data-ttu-id="b95a8-128">Referencia de Internet de Windows</span><span class="sxs-lookup"><span data-stu-id="b95a8-128">Windows Internet Reference</span></span>](wininet-reference.md)<br/> | <span data-ttu-id="b95a8-129">Documentación de referencia de la API de Internet de Windows.</span><span class="sxs-lookup"><span data-stu-id="b95a8-129">Reference documentation for the Windows Internet API.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="b95a8-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b95a8-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b95a8-131">Servicios HTTP de Microsoft Windows (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="b95a8-131">Microsoft Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 


---
title: Herramienta de prueba de Microsoft Platform Ready
description: Herramienta de prueba de Microsoft Platform Ready
ms.assetid: C41FBE70-E392-4FD0-954B-6C24168CB93E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6286e7ed64f013a8ea002ea392ba0d3bcac67296
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "103794194"
---
# <a name="microsoft-platform-ready-test-tool"></a><span data-ttu-id="8fccf-103">Herramienta de prueba de Microsoft Platform Ready</span><span class="sxs-lookup"><span data-stu-id="8fccf-103">Microsoft Platform Ready Test Tool</span></span>

## <a name="platform"></a><span data-ttu-id="8fccf-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="8fccf-104">Platform</span></span>

 <span data-ttu-id="8fccf-105">**Servidores** : windows Server 2012 \| Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8fccf-105">**Servers** – Windows Server 2012 \| Windows Server 2012 R2</span></span>  

## <a name="description"></a><span data-ttu-id="8fccf-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="8fccf-106">Description</span></span>

<span data-ttu-id="8fccf-107">La herramienta de prueba preparación para la plataforma de Microsoft (MPR) se usa para preparar las aplicaciones de la plataforma y para validar el cumplimiento de los requisitos de certificación de las aplicaciones Windows Server 2012 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="8fccf-107">The Microsoft Platform Ready (MPR) Test Tool is used for platform application readiness and to validate compliance with certification requirements for Windows Server 2012 and Windows Server 2012 R2 applications.</span></span>

<span data-ttu-id="8fccf-108">Microsoft recomienda encarecidamente incorporar la herramienta de prueba de MPR en los procesos de compilación y prueba de software, lo que garantiza la disponibilidad de la plataforma antes de que las aplicaciones se publiquen en el mercado.</span><span class="sxs-lookup"><span data-stu-id="8fccf-108">Microsoft strongly encourages incorporating the MPR Test Tool into the software build and test processes, thereby ensuring platform readiness before applications are released to market.</span></span> <span data-ttu-id="8fccf-109">La herramienta de prueba de MPR también es una herramienta recomendada para probar las aplicaciones de línea de negocio y para evaluar los productos de servidor para su compatibilidad con la plataforma antes de tomar decisiones de compra.</span><span class="sxs-lookup"><span data-stu-id="8fccf-109">The MPR Test Tool is also a recommended tool to test line of business applications and for evaluating server products for their platform compatibility before making purchasing decisions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fccf-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fccf-110">Requirements</span></span>

<span data-ttu-id="8fccf-111">La herramienta de prueba de MPR incluye pruebas automatizadas para:</span><span class="sxs-lookup"><span data-stu-id="8fccf-111">The MPR Test Tool includes automated tests for:</span></span>

-   <span data-ttu-id="8fccf-112">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="8fccf-112">Windows Installer</span></span>
-   <span data-ttu-id="8fccf-113">Instalación y funcionalidad principal</span><span class="sxs-lookup"><span data-stu-id="8fccf-113">Setup and Primary Functionality</span></span>
-   <span data-ttu-id="8fccf-114">Controladores y seguridad</span><span class="sxs-lookup"><span data-stu-id="8fccf-114">Drivers and Security</span></span>
-   <span data-ttu-id="8fccf-115">Prácticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="8fccf-115">Best Practices</span></span>

<span data-ttu-id="8fccf-116">La prueba automática y el envío de los resultados de la mayoría de las aplicaciones de servidor deben tardar 2 horas o menos. las aplicaciones más complejas pueden tardar aproximadamente 4 horas.</span><span class="sxs-lookup"><span data-stu-id="8fccf-116">Self-testing and submission of results for most Server apps should take 2 hours or less; more complex apps can take around 4 hours.</span></span>

<span data-ttu-id="8fccf-117">Todos los controladores deben pasar por separado las pruebas de certificación de hardware de Windows y estar firmadas por Microsoft para Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8fccf-117">All drivers must separately pass Windows Hardware Certification testing and be signed by Microsoft for Windows Server 2012.</span></span>

## <a name="usage"></a><span data-ttu-id="8fccf-118">Uso</span><span class="sxs-lookup"><span data-stu-id="8fccf-118">Usage</span></span>

<span data-ttu-id="8fccf-119">Para probar sus aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="8fccf-119">To test your apps:</span></span>

1.  <span data-ttu-id="8fccf-120">Instale la configuración mínima más reciente de Windows Server 2012 (GUI de servidor completa, interfaz de servidor mínima o Server Core) según sea necesario para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8fccf-120">Install the latest Windows Server 2012 minimum configuration (Full Server GUI, Minimal Server Interface, or Server Core) as required for your app.</span></span>
2.  <span data-ttu-id="8fccf-121">Revise los requisitos de certificación.</span><span class="sxs-lookup"><span data-stu-id="8fccf-121">Review the certification requirements.</span></span>
3.  <span data-ttu-id="8fccf-122">En un sistema limpio, ejecute la herramienta de prueba de MPR en modo de interfaz de usuario completa o en modo de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="8fccf-122">On a clean system, run the MPR Test Tool in either full UI mode or command line mode.</span></span>
4.  <span data-ttu-id="8fccf-123">Complete el proceso de prueba autoguiado.</span><span class="sxs-lookup"><span data-stu-id="8fccf-123">Complete the self-guided testing process.</span></span>
5.  <span data-ttu-id="8fccf-124">Revise los resultados y corrija la aplicación según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="8fccf-124">Review results and fix your app as required.</span></span>
6.  <span data-ttu-id="8fccf-125">Iniciar sesión y cargar los resultados correctos en el portal de la plataforma de Microsoft listo para la publicación en el catálogo de Windows Server y el uso del logotipo.</span><span class="sxs-lookup"><span data-stu-id="8fccf-125">Sign-in and upload successful results to Microsoft Platform Ready portal for listing in Windows Server Catalog and usage of the logo.</span></span>

## <a name="resources"></a><span data-ttu-id="8fccf-126">Recursos</span><span class="sxs-lookup"><span data-stu-id="8fccf-126">Resources</span></span>

-   [<span data-ttu-id="8fccf-127">Requisitos para el programa de certificación de aplicaciones de Windows Server</span><span class="sxs-lookup"><span data-stu-id="8fccf-127">Requirements for Windows Server App Certification Program</span></span>](../win_cert/certification-requirements-for-windows-desktop-apps.md)
-   [<span data-ttu-id="8fccf-128">Herramienta de comprobación Microsoft Platform Ready (MPR)</span><span class="sxs-lookup"><span data-stu-id="8fccf-128">Microsoft Platform Ready (MPR) Test Tool</span></span>](https://www.microsoft.com/download/details.aspx?id=37143)
-   [<span data-ttu-id="8fccf-129">Programa de certificación de aplicaciones de Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8fccf-129">Windows Server 2012 Application Certification Program</span></span>](https://azure.microsoft.com/overview/commercial-marketplace/)
-   [<span data-ttu-id="8fccf-130">Comentarios del logotipo de Windows Server</span><span class="sxs-lookup"><span data-stu-id="8fccf-130">Windows Server Logo Feedback</span></span>](mailto:WSLogoFB@microsoft.com)

 

 
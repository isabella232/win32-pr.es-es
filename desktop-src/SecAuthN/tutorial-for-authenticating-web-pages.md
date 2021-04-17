---
description: En este tutorial se resaltan los distintos aspectos que los desarrolladores web deben tener en cuenta al diseñar páginas para el flujo de autorización Web de Windows 8. En esta sección se muestra un flujo de autorización de dos páginas.
ms.assetid: A26E09EF-6C7A-4F75-89A7-76086F63F3B1
title: Tutorial para autenticar páginas web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c6fc6482c5e6dfaf89a9fc9732783f5f088b4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652906"
---
# <a name="tutorial-for-authenticating-web-pages"></a><span data-ttu-id="4da1d-104">Tutorial para autenticar páginas web</span><span class="sxs-lookup"><span data-stu-id="4da1d-104">Tutorial for authenticating web pages</span></span>

<span data-ttu-id="4da1d-105">En este tutorial se resaltan los distintos aspectos que los desarrolladores web deben tener en cuenta al diseñar páginas para el flujo de autorización Web de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4da1d-105">This tutorial highlights the different aspects that web developers should care about when designing pages for the web authorization flow for Windows 8.</span></span> <span data-ttu-id="4da1d-106">En esta sección se muestra un flujo de autorización de dos páginas.</span><span class="sxs-lookup"><span data-stu-id="4da1d-106">This section This sample demonstrates a two-page authorization flow.</span></span>

<span data-ttu-id="4da1d-107">**Objetivo:** El objetivo del ejemplo no es ser preceptivo en cuanto al diseño o diseño visual en el que cada proveedor tendrá un punto de vista único en, pero para llamar a algunas áreas que merece la pena invertir en para tener una experiencia de estilo de diseño de Microsoft de primera clase para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4da1d-107">**Objective:** The goal of the sample is not to be prescriptive about the layout or visual design that each provider will certainly have a unique point of view on, but to call out a few areas worth investing in to have a first-class Microsoft design style experience for Windows 8.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4da1d-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4da1d-108">Prerequisites</span></span>

<span data-ttu-id="4da1d-109">Para poder usar las API de agente de autenticación Web, necesita:</span><span class="sxs-lookup"><span data-stu-id="4da1d-109">In order to use web authentication broker APIs, you need:</span></span>

-   <span data-ttu-id="4da1d-110">Windows 8 (solo x86 o AMD64)</span><span class="sxs-lookup"><span data-stu-id="4da1d-110">Windows 8 (x86 or amd64 only)</span></span>
-   <span data-ttu-id="4da1d-111">Microsoft Internet Information Services (IIS) debe instalarse desde el panel de control en "programas y características" y con la opción "activar o desactivar las características de Windows".</span><span class="sxs-lookup"><span data-stu-id="4da1d-111">Microsoft Internet Information Services (IIS) should be installed from the Control Panel under "Programs and Features" and using the "Turn Windows features on or off" option.</span></span>

<span data-ttu-id="4da1d-112">**Tiempo total de finalización:** 2 minutos.</span><span class="sxs-lookup"><span data-stu-id="4da1d-112">**Total time to complete:** 2 minutes.</span></span>

## <a name="where-to-go-from-here"></a><span data-ttu-id="4da1d-113">Cómo continuar a partir de aquí</span><span class="sxs-lookup"><span data-stu-id="4da1d-113">Where to go from here</span></span>

<span data-ttu-id="4da1d-114">Siguiente [autenticación para páginas web](authentication-for-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="4da1d-114">Next [Authentication for web pages](authentication-for-web-pages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="4da1d-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4da1d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4da1d-116">Consideraciones para el desarrollo de páginas web</span><span class="sxs-lookup"><span data-stu-id="4da1d-116">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="4da1d-117">Aplicación de ejemplo del SDK del agente de autenticación Web</span><span class="sxs-lookup"><span data-stu-id="4da1d-117">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="4da1d-118">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="4da1d-118">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041)
</dt> </dl>

 

 

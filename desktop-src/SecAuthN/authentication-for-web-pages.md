---
description: La autenticación está probando quién es.
ms.assetid: 5B058197-67B3-40DD-80D8-7BD8EE084CC9
title: Autenticación para páginas web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7c7bd37334f345ae16074c050b6b06c5fd644f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002604"
---
# <a name="authentication-for-web-pages"></a><span data-ttu-id="0afd9-103">Autenticación para páginas web</span><span class="sxs-lookup"><span data-stu-id="0afd9-103">Authentication for web pages</span></span>

<span data-ttu-id="0afd9-104">La autenticación está probando quién es.</span><span class="sxs-lookup"><span data-stu-id="0afd9-104">Authentication is proving who you are.</span></span>

<span data-ttu-id="0afd9-105">**Objetivo:** Para que el agente de autenticación web aparezca como parte de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0afd9-105">**Objective:** To have the web authentication broker appear as part of your app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0afd9-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0afd9-106">Prerequisites</span></span>

<span data-ttu-id="0afd9-107">None</span><span class="sxs-lookup"><span data-stu-id="0afd9-107">None</span></span>

<span data-ttu-id="0afd9-108">**Tiempo de finalización:** 15 minutos.</span><span class="sxs-lookup"><span data-stu-id="0afd9-108">**Time to complete:** 15 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="0afd9-109">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="0afd9-109">Instructions</span></span>

### <a name="1-getting-started"></a><span data-ttu-id="0afd9-110">1. Introducción</span><span class="sxs-lookup"><span data-stu-id="0afd9-110">1. Getting started</span></span>

<span data-ttu-id="0afd9-111">Inicie el archivo de instalación para instalar un sitio web de Contoso en Internet Information Services 8 en el equipo local para hospedar los archivos HTML y CSS de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0afd9-111">Launch the setup file to install a Contoso website in Internet Information Services 8 on the local machine to host the sample HTML and CSS files.</span></span>

1.  <span data-ttu-id="0afd9-112">Los archivos HTML y CSS de ejemplo se instalarán en el directorio archivos de programa en Microsoft \\ contoso.</span><span class="sxs-lookup"><span data-stu-id="0afd9-112">Sample HTML and CSS files will be installed to the program files directory under Microsoft\\Contoso.</span></span>
2.  <span data-ttu-id="0afd9-113">Además, una aplicación de la tienda Windows "fabrikam social" se desempaquetará en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="0afd9-113">In addition a "Fabrikam Social"Windows Store app will be unpackaged to the desktop.</span></span>

### <a name="2-getting-familiar"></a><span data-ttu-id="0afd9-114">2. familiarizarse</span><span class="sxs-lookup"><span data-stu-id="0afd9-114">2. Getting familiar</span></span>

<span data-ttu-id="0afd9-115">Para hacerse una idea del aspecto de las páginas de ejemplo en el agente de autenticación Web, abra el archivo de solución Fabrikam social de Visual Studio 11 en la carpeta "fabrikam social" en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="0afd9-115">To get a feel for what the sample pages look like in the Web Authentication Broker, open the Fabrikam Social Visual Studio 11 solution file in the "Fabrikam Social" folder on the desktop.</span></span>

1.  <span data-ttu-id="0afd9-116">Ejecute la aplicación y presione "iniciar" para que aparezcan las páginas de ejemplo en el agente de autenticación Web.</span><span class="sxs-lookup"><span data-stu-id="0afd9-116">Run the application and hit "Launch" to bring up the sample pages in the Web Authentication Broker.</span></span>
2.  <span data-ttu-id="0afd9-117">Se puede cambiar el tamaño de la aplicación a un lado o se puede activar compartiendo algunos datos en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0afd9-117">The app can be resized to one side or activated by sharing some data to the application.</span></span>

### <a name="3-authentication"></a><span data-ttu-id="0afd9-118">3. Authentication</span><span class="sxs-lookup"><span data-stu-id="0afd9-118">3. Authentication</span></span>

<span data-ttu-id="0afd9-119">Cuando la aplicación subyacente invoca la API de autenticación Web para conectarse al proveedor, "Contoso social", se muestra la página de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="0afd9-119">When the Web Auth API is invoked by the underlying app to connect to the provider, "Contoso Social", the login page is shown.</span></span> <span data-ttu-id="0afd9-120">Esta página está diseñada para ser mejor en una experiencia de inicio de sesión rápida y fluida.</span><span class="sxs-lookup"><span data-stu-id="0afd9-120">This page is designed to be best at a fast and fluid login experience.</span></span> <span data-ttu-id="0afd9-121">También proporciona puntos de entrada a algunas otras acciones de usuario comunes, como recuperar detalles de contraseña, registrarse para obtener una cuenta y leer instrucciones sobre la privacidad y los términos y condiciones que se completan en el explorador.</span><span class="sxs-lookup"><span data-stu-id="0afd9-121">It also provides entry points to some other common user actions such as retrieving password details, signing up for an account, and reading statements on privacy and terms and conditions that are completed in the browser.</span></span> ![Página de inicio de sesión de Contoso](images/wab-figure8.png)

## <a name="summary-and-next-steps"></a><span data-ttu-id="0afd9-123">Resumen y pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="0afd9-123">Summary and next steps</span></span>

<span data-ttu-id="0afd9-124">[Tutorial de resumen para autenticar páginas web](tutorial-for-authenticating-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="0afd9-124">Summary [Tutorial for authenticating web pages](tutorial-for-authenticating-web-pages.md)</span></span>

<span data-ttu-id="0afd9-125">Siguiente [autorización para páginas web](authorization-for-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="0afd9-125">Next [Authorization for web pages](authorization-for-web-pages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="0afd9-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0afd9-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0afd9-127">Consideraciones para el desarrollo de páginas web</span><span class="sxs-lookup"><span data-stu-id="0afd9-127">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="0afd9-128">Aplicación de ejemplo del SDK del agente de autenticación Web</span><span class="sxs-lookup"><span data-stu-id="0afd9-128">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="0afd9-129">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="0afd9-129">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 

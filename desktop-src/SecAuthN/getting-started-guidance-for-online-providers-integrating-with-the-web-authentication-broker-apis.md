---
description: Directrices para que los desarrolladores web y los proveedores en línea creen páginas web adaptadas a las API de Windows 8 Web Authentication Broker para las funcionalidades de inicio de sesión único (SSO).
ms.assetid: E2AECE26-9649-41CB-9808-4F8171C707C3
title: Guía de introducción para proveedores en línea que se integran con las API del Agente de autenticación web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bf0ce59cd92e32264823861aaef44e90b4f2c0
ms.sourcegitcommit: 6377cd944d1f09f2dfe5727170ca8b330c8235bf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "113353638"
---
# <a name="getting-started-guidance-for-online-providers-integrating-with-the-web-authentication-broker-apis"></a><span data-ttu-id="79dc9-103">Guía de introducción para proveedores en línea que se integran con las API del Agente de autenticación web</span><span class="sxs-lookup"><span data-stu-id="79dc9-103">Getting started guidance for online providers integrating with the Web Authentication Broker APIs</span></span>

<span data-ttu-id="79dc9-104">Esta sección guía a los desarrolladores web y proveedores en línea para crear páginas web adaptadas a Windows 8 API del Agente de autenticación web.</span><span class="sxs-lookup"><span data-stu-id="79dc9-104">This section guides web developers and online providers for creating web pages tailored for the Windows 8 Web Authentication Broker APIs.</span></span> <span data-ttu-id="79dc9-105">Proporciona recomendaciones visuales e interactivas para una experiencia de usuario de un extremo a otro de la página web, así como cómo habilitar las funcionalidades de inicio de sesión único (SSO).</span><span class="sxs-lookup"><span data-stu-id="79dc9-105">It provides the visual and interactive recommendations for an end-to-end user experience of the web page as well as how to enable single sign-on (SSO) capabilities.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="79dc9-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="79dc9-106">In this section</span></span>



| <span data-ttu-id="79dc9-107">Tema</span><span class="sxs-lookup"><span data-stu-id="79dc9-107">Topic</span></span>                                                                                                     | <span data-ttu-id="79dc9-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="79dc9-108">Description</span></span>                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79dc9-109">Consideraciones para el desarrollo de páginas web</span><span class="sxs-lookup"><span data-stu-id="79dc9-109">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)<br/> | <span data-ttu-id="79dc9-110">El Agente de autenticación web se basa en las mismas tecnologías que Internet Explorer en Windows.</span><span class="sxs-lookup"><span data-stu-id="79dc9-110">Web Authentication Broker is built on the top of the same technologies that power Internet Explorer in Windows.</span></span> <span data-ttu-id="79dc9-111">Sin embargo, debido a un propósito muy especial de este componente, algunas características del Internet Explorer se deshabilitaron o se bloquearon para una configuración específica.</span><span class="sxs-lookup"><span data-stu-id="79dc9-111">However, due to a very special purpose of this component some features of the Internet Explorer were disabled or locked to specific configuration.</span></span> <br/> |
| [<span data-ttu-id="79dc9-112">Cómo personalizar los elementos de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="79dc9-112">How to customize the UI elements</span></span>](how-to-customize-the-ui-elements.md)<br/>                       | <span data-ttu-id="79dc9-113">Una página web personaliza la interfaz de usuario (UI) con el título, el icono y el color del encabezado mediante etiquetas de metadatos definidas en la página web.</span><span class="sxs-lookup"><span data-stu-id="79dc9-113">A web page customizes the user interface (UI) with the title, icon, and header color by using metadata tags defined on the web page.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="79dc9-114">Tutorial para autenticar páginas web</span><span class="sxs-lookup"><span data-stu-id="79dc9-114">Tutorial for authenticating web pages</span></span>](tutorial-for-authenticating-web-pages.md)<br/>             |                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="79dc9-115">Problemas de autenticación web</span><span class="sxs-lookup"><span data-stu-id="79dc9-115">Web authentication problems</span></span>](web-authentication-problems.md)<br/>                                 | <span data-ttu-id="79dc9-116">En este tema se describen las sugerencias de solución de problemas para usar las API del Agente de autenticación web para las páginas web.</span><span class="sxs-lookup"><span data-stu-id="79dc9-116">This topic describes troubleshooting tips for using the Web Authentication Broker APIs for your web pages.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="79dc9-117">Preguntas más frecuentes sobre el Agente de autenticación web</span><span class="sxs-lookup"><span data-stu-id="79dc9-117">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.yml)<br/>                     | <span data-ttu-id="79dc9-118">Preguntas más frecuentes sobre el Agente de autenticación web.</span><span class="sxs-lookup"><span data-stu-id="79dc9-118">Frequently asked questions for Web Authentication Broker.</span></span><br/>                                                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="79dc9-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="79dc9-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="79dc9-120">[Introducción al agente de autenticación web](/previous-versions/windows/apps/hh750287(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="79dc9-120">[Web authentication broker overview](/previous-versions/windows/apps/hh750287(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="79dc9-121">Aplicación de ejemplo del SDK del Agente de autenticación web</span><span class="sxs-lookup"><span data-stu-id="79dc9-121">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="79dc9-122">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="79dc9-122">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 


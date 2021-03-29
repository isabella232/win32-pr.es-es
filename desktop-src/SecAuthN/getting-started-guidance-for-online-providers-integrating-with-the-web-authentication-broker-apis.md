---
description: Instrucciones para desarrolladores web y proveedores en línea para crear páginas web adaptadas a las API de agente de autenticación Web de Windows 8 para las funcionalidades de inicio de sesión único (SSO).
ms.assetid: E2AECE26-9649-41CB-9808-4F8171C707C3
title: Guía de introducción para los proveedores en línea que se integran con las API de agente de autenticación Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 842f3c562d2ad288efaecec82f8da8ca771886a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911882"
---
# <a name="getting-started-guidance-for-online-providers-integrating-with-the-web-authentication-broker-apis"></a><span data-ttu-id="d2b3e-103">Guía de introducción para los proveedores en línea que se integran con las API de agente de autenticación Web</span><span class="sxs-lookup"><span data-stu-id="d2b3e-103">Getting started guidance for online providers integrating with the Web Authentication Broker APIs</span></span>

<span data-ttu-id="d2b3e-104">En esta sección se describen los desarrolladores web y los proveedores en línea para crear páginas web adaptadas a las API del agente de autenticación Web de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d2b3e-104">This section guides web developers and online providers for creating web pages tailored for the Windows 8 Web Authentication Broker APIs.</span></span> <span data-ttu-id="d2b3e-105">Proporciona las recomendaciones visuales e interactivas para una experiencia del usuario de un extremo a otro de la página web, así como la forma de habilitar las funcionalidades de inicio de sesión único (SSO).</span><span class="sxs-lookup"><span data-stu-id="d2b3e-105">It provides the visual and interactive recommendations for an end-to-end user experience of the web page as well as how to enable single sign-on (SSO) capabilities.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d2b3e-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="d2b3e-106">In this section</span></span>



| <span data-ttu-id="d2b3e-107">Tema</span><span class="sxs-lookup"><span data-stu-id="d2b3e-107">Topic</span></span>                                                                                                     | <span data-ttu-id="d2b3e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2b3e-108">Description</span></span>                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2b3e-109">Consideraciones para el desarrollo de páginas web</span><span class="sxs-lookup"><span data-stu-id="d2b3e-109">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)<br/> | <span data-ttu-id="d2b3e-110">El agente de autenticación Web se basa en la parte superior de las mismas tecnologías que Power Internet Explorer en Windows.</span><span class="sxs-lookup"><span data-stu-id="d2b3e-110">Web Authentication Broker is built on the top of the same technologies that power Internet Explorer in Windows.</span></span> <span data-ttu-id="d2b3e-111">Sin embargo, debido a una finalidad muy especial de este componente, algunas características de Internet Explorer se deshabilitaron o se bloqueaban para una configuración específica.</span><span class="sxs-lookup"><span data-stu-id="d2b3e-111">However, due to a very special purpose of this component some features of the Internet Explorer were disabled or locked to specific configuration.</span></span> <br/> |
| [<span data-ttu-id="d2b3e-112">Cómo personalizar los elementos de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="d2b3e-112">How to customize the UI elements</span></span>](how-to-customize-the-ui-elements.md)<br/>                       | <span data-ttu-id="d2b3e-113">Una página web Personaliza la interfaz de usuario (UI) con el título, el icono y el color del encabezado mediante etiquetas de metadatos definidas en la Página Web.</span><span class="sxs-lookup"><span data-stu-id="d2b3e-113">A web page customizes the user interface (UI) with the title, icon, and header color by using metadata tags defined on the web page.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="d2b3e-114">Tutorial para autenticar páginas web</span><span class="sxs-lookup"><span data-stu-id="d2b3e-114">Tutorial for authenticating web pages</span></span>](tutorial-for-authenticating-web-pages.md)<br/>             |                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="d2b3e-115">Problemas de autenticación web</span><span class="sxs-lookup"><span data-stu-id="d2b3e-115">Web authentication problems</span></span>](web-authentication-problems.md)<br/>                                 | <span data-ttu-id="d2b3e-116">En este tema se describen las sugerencias de solución de problemas para usar las API de agente de autenticación Web para las páginas Web.</span><span class="sxs-lookup"><span data-stu-id="d2b3e-116">This topic describes troubleshooting tips for using the Web Authentication Broker APIs for your web pages.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="d2b3e-117">Preguntas más frecuentes sobre el agente de autenticación Web</span><span class="sxs-lookup"><span data-stu-id="d2b3e-117">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.md)<br/>                     | <span data-ttu-id="d2b3e-118">Preguntas más frecuentes sobre el agente de autenticación Web.</span><span class="sxs-lookup"><span data-stu-id="d2b3e-118">Frequently asked questions for Web Authentication Broker.</span></span><br/>                                                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="d2b3e-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d2b3e-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d2b3e-120">[Introducción al agente de autenticación Web](/previous-versions/windows/apps/hh750287(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="d2b3e-120">[Web authentication broker overview](/previous-versions/windows/apps/hh750287(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="d2b3e-121">Aplicación de ejemplo del SDK del agente de autenticación Web</span><span class="sxs-lookup"><span data-stu-id="d2b3e-121">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="d2b3e-122">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="d2b3e-122">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 


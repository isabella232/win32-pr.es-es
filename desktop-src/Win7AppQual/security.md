---
description: Seguridad (Guía de calidad de aplicaciones de Windows 7 y Windows Server 2008 R2)
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: Seguridad (Guía de calidad de aplicaciones de Windows 7 y Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f320f4cb561079380e19a969eba95f3f6b321fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116233"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="d1e18-103">Seguridad (Guía de calidad de aplicaciones de Windows 7 y Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="d1e18-103">Security (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="d1e18-104">A partir de Windows Internet Explorer 7, Windows Internet Explorer se ejecuta  en un contexto de seguridad denominado Modo protegido cuando los usuarios lo ejecutan en el sistema operativo Windows Vista o en una versión posterior.</span><span class="sxs-lookup"><span data-stu-id="d1e18-104">Starting with Windows Internet Explorer 7, Windows Internet Explorer runs in a security context called *Protected Mode* when users run it on the Windows Vista operating system or a later version.</span></span> <span data-ttu-id="d1e18-105">Este modo se Internet Explorer en una configuración con menos privilegios que una aplicación de usuario estándar, por lo que cierta funcionalidad es limitada, especialmente los controles ActiveX y determinados tipos de complementos. Para obtener más información sobre el modo protegido en Internet Explorer y su impacto en la compatibilidad, vea Descripción y trabajo en modo [protegido Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) en MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="d1e18-105">This mode runs Internet Explorer in a lower-privilege setting than a standard user application so certain functionality is limited, especially ActiveX controls and certain types of plug-ins. For more information about Protected Mode in Internet Explorer and its impact on compatibility, see [Understanding and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) in the MSDN Library.</span></span>

<span data-ttu-id="d1e18-106">De forma predeterminada, Windows Internet Explorer 8 también habilita la prevención de ejecución de datos (DEP), que ayuda a las aplicaciones a evitar la ejecución de código arbitrario en ataques en línea.</span><span class="sxs-lookup"><span data-stu-id="d1e18-106">By default, Windows Internet Explorer 8 also enables Data Execution Prevention (DEP), which helps applications avoid running arbitrary code in online attacks.</span></span> <span data-ttu-id="d1e18-107">Sin embargo, es posible que algunos complementos no usen esta característica de seguridad (por ejemplo, los complementos que no están diseñados para ejecutar solo código que se encuentra en la memoria que se ha marcado específicamente como ejecutable, como las aplicaciones que se han creado mediante una versión anterior del marco de la biblioteca de plantillas ActiveX (ATL).</span><span class="sxs-lookup"><span data-stu-id="d1e18-107">However, some add-ons might not use this security feature (for example, any add-ons that are not designed to run only code that is located in memory that has been specifically marked as executable, such as applications that are built by using an older version of the ActiveX Template Library (ATL) framework).</span></span>

<span data-ttu-id="d1e18-108">Internet Explorer 8 también protege a los usuarios frente a posibles vulnerabilidades de seguridad que usan scripts.</span><span class="sxs-lookup"><span data-stu-id="d1e18-108">Internet Explorer 8 also protects users against potential security vulnerabilities that use scripts.</span></span> <span data-ttu-id="d1e18-109">Por ejemplo, no puede navegar desde una dirección URL de una zona de menos confianza a una dirección URL de una zona de mayor confianza, excepto a través de la interacción explícita del usuario.</span><span class="sxs-lookup"><span data-stu-id="d1e18-109">For example, you cannot navigate from a URL in a less trusted zone to a URL in a more trusted zone except through explicit user interaction.</span></span> <span data-ttu-id="d1e18-110">Tampoco puede ocultar determinados elementos de la interfaz de usuario del explorador (como la barra de direcciones) en una zona de no confianza (Internet).</span><span class="sxs-lookup"><span data-stu-id="d1e18-110">You also cannot hide certain elements of the browser’s user interface (such as the address bar) in an un-trusted (Internet) zone.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1e18-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d1e18-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1e18-112">Diseñar actualizaciones que afectan a la compatibilidad entre exploradores</span><span class="sxs-lookup"><span data-stu-id="d1e18-112">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 

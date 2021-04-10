---
description: .
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: Seguridad (Guía de calidad de la aplicación Windows 7 y Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bbaaa6b34463e04f5870082e5c693462f4e19fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279632"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="ed30a-103">Seguridad (Guía de calidad de la aplicación Windows 7 y Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="ed30a-103">Security (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="ed30a-104">A partir de Windows Internet Explorer 7, Windows Internet Explorer se ejecuta en un contexto de seguridad denominado *modo protegido* cuando los usuarios lo ejecutan en el sistema operativo Windows Vista o en una versión posterior.</span><span class="sxs-lookup"><span data-stu-id="ed30a-104">Starting with Windows Internet Explorer 7, Windows Internet Explorer runs in a security context called *Protected Mode* when users run it on the Windows Vista operating system or a later version.</span></span> <span data-ttu-id="ed30a-105">Este modo ejecuta Internet Explorer en una configuración con menos privilegios que una aplicación de usuario estándar, por lo que determinada funcionalidad es limitada, en especial los controles ActiveX y determinados tipos de complementos. Para obtener más información acerca del modo protegido en Internet Explorer y su impacto en la compatibilidad, vea [Descripción y funcionamiento en modo protegido de Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) en MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="ed30a-105">This mode runs Internet Explorer in a lower-privilege setting than a standard user application so certain functionality is limited, especially ActiveX controls and certain types of plug-ins. For more information about Protected Mode in Internet Explorer and its impact on compatibility, see [Understanding and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) in the MSDN Library.</span></span>

<span data-ttu-id="ed30a-106">De forma predeterminada, Windows Internet Explorer 8 también habilita la prevención de ejecución de datos (DEP), que ayuda a las aplicaciones a evitar la ejecución de código arbitrario en ataques en línea.</span><span class="sxs-lookup"><span data-stu-id="ed30a-106">By default, Windows Internet Explorer 8 also enables Data Execution Prevention (DEP), which helps applications avoid running arbitrary code in online attacks.</span></span> <span data-ttu-id="ed30a-107">Sin embargo, es posible que algunos complementos no utilicen esta característica de seguridad (por ejemplo, los complementos que no están diseñados para ejecutar solo el código que se encuentra en memoria que se ha marcado específicamente como ejecutable, como las aplicaciones compiladas con una versión anterior del marco de trabajo de la biblioteca de plantillas ActiveX (ATL)).</span><span class="sxs-lookup"><span data-stu-id="ed30a-107">However, some add-ons might not use this security feature (for example, any add-ons that are not designed to run only code that is located in memory that has been specifically marked as executable, such as applications that are built by using an older version of the ActiveX Template Library (ATL) framework).</span></span>

<span data-ttu-id="ed30a-108">Internet Explorer 8 también protege a los usuarios frente a posibles vulnerabilidades de seguridad que usan scripts.</span><span class="sxs-lookup"><span data-stu-id="ed30a-108">Internet Explorer 8 also protects users against potential security vulnerabilities that use scripts.</span></span> <span data-ttu-id="ed30a-109">Por ejemplo, no se puede navegar desde una dirección URL de una zona de menos confianza a una dirección URL en una zona más confiable excepto a través de la interacción explícita del usuario.</span><span class="sxs-lookup"><span data-stu-id="ed30a-109">For example, you cannot navigate from a URL in a less trusted zone to a URL in a more trusted zone except through explicit user interaction.</span></span> <span data-ttu-id="ed30a-110">Tampoco puede ocultar ciertos elementos de la interfaz de usuario del explorador (como la barra de direcciones) en una zona que no es de confianza (Internet).</span><span class="sxs-lookup"><span data-stu-id="ed30a-110">You also cannot hide certain elements of the browser’s user interface (such as the address bar) in an un-trusted (Internet) zone.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed30a-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ed30a-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed30a-112">Actualizaciones de diseño que afectan a la compatibilidad entre exploradores</span><span class="sxs-lookup"><span data-stu-id="ed30a-112">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 

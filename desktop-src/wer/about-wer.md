---
title: Acerca de WER
description: Informe de errores de Windows (WER) es una infraestructura de comentarios basada en eventos flexible diseñada para recopilar información sobre los problemas de hardware y software que Windows puede detectar, notificar la información a Microsoft y proporcionar a los usuarios las soluciones disponibles. Para obtener información acerca de las mejoras de WER, consulte Novedades de WER.
ms.assetid: d26b3d2a-51cf-41d9-936b-f1b45778ea61
keywords:
- Informe de errores de Windows Informe de errores de Windows, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37ab7622c3e0b3a7bebff64e6c8373f2d163ba23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357329"
---
# <a name="about-wer"></a><span data-ttu-id="ce42b-105">Acerca de WER</span><span class="sxs-lookup"><span data-stu-id="ce42b-105">About WER</span></span>

<span data-ttu-id="ce42b-106">Informe de errores de Windows (WER) es una infraestructura de comentarios basada en eventos flexible diseñada para recopilar información sobre los problemas de hardware y software que Windows puede detectar, notificar la información a Microsoft y proporcionar a los usuarios las soluciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="ce42b-106">Windows Error Reporting (WER) is a flexible event-based feedback infrastructure designed to gather information about the hardware and software problems that Windows can detect, report the information to Microsoft, and provide users with any available solutions.</span></span> <span data-ttu-id="ce42b-107">Para obtener información acerca de las mejoras de WER, consulte [novedades de Wer](what-s-new-in-wer.md).</span><span class="sxs-lookup"><span data-stu-id="ce42b-107">For information about the improvements to WER, see [What's New in WER](what-s-new-in-wer.md).</span></span>

<span data-ttu-id="ce42b-108">A partir de Windows Vista, Windows proporciona bloqueo, no respuesta y generación de informes de errores de kernel de forma predeterminada sin necesidad de realizar cambios en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ce42b-108">Beginning with Windows Vista, Windows provides crash, no response, and kernel fault error reporting by default without requiring changes to your application.</span></span> <span data-ttu-id="ce42b-109">En su lugar, las aplicaciones usan la API de WER para generar informes de errores para problemas específicos de la aplicación que no están relacionados con bloqueos, no respuestas o errores de kernel.</span><span class="sxs-lookup"><span data-stu-id="ce42b-109">Applications instead use the WER API to generate error reports for application-specific issues that are not related to crashes, non-responses, or kernel faults.</span></span>

<span data-ttu-id="ce42b-110">Para generar informes de errores para problemas específicos de la aplicación, la aplicación debe crear una breve descripción del problema con algunos datos básicos denominados *parámetros de informe*.</span><span class="sxs-lookup"><span data-stu-id="ce42b-110">To generate error reports for application-specific issues, the application must create a short description of the problem using a few basic pieces of information called *report parameters*.</span></span> <span data-ttu-id="ce42b-111">Los parámetros de informe incluyen información como el nombre de la aplicación, la versión de la aplicación, el nombre del módulo, la versión del módulo y el código de error.</span><span class="sxs-lookup"><span data-stu-id="ce42b-111">Report parameters include information such as the application name, application version, module name, module version, and error code.</span></span> <span data-ttu-id="ce42b-112">La combinación de estos parámetros de informe describe un problema único.</span><span class="sxs-lookup"><span data-stu-id="ce42b-112">The combination of these report parameters describes a unique problem.</span></span>

<span data-ttu-id="ce42b-113">Cuando WER comprueba una solución, se comunica con el servidor WER en Microsoft preguntando primero si el problema ya está conocido.</span><span class="sxs-lookup"><span data-stu-id="ce42b-113">When WER checks for a solution, it communicates with the WER server at Microsoft by first asking if the problem is already known.</span></span> <span data-ttu-id="ce42b-114">El servidor responde de una de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="ce42b-114">The server responds in one of the following ways:</span></span>

-   <span data-ttu-id="ce42b-115">Si se conoce el problema y hay una solución, el servidor envía la solución al equipo cliente y WER muestra esta información al usuario.</span><span class="sxs-lookup"><span data-stu-id="ce42b-115">If the problem is known and there is a solution, the server sends the solution to the client computer and WER displays this information to the user.</span></span>
-   <span data-ttu-id="ce42b-116">Si se está investigando el problema, el servidor puede enviar una respuesta que indica el estado.</span><span class="sxs-lookup"><span data-stu-id="ce42b-116">If the problem is being investigated, the server may send a response that indicates the status.</span></span> <span data-ttu-id="ce42b-117">Si el desarrollador necesita más información para resolver el problema, el servidor solicita información adicional de WER y WER solicita al usuario permiso para enviar esta información.</span><span class="sxs-lookup"><span data-stu-id="ce42b-117">If the developer needs more information to solve the problem, the server requests additional information from WER and WER asks the user for permission to send this information.</span></span>
-   <span data-ttu-id="ce42b-118">Si no se conoce el problema, el servidor crea un problema para que un desarrollador investigue y envíe a WER una respuesta que indica el estado.</span><span class="sxs-lookup"><span data-stu-id="ce42b-118">If the problem is not known, the server creates an issue for a developer to investigate and sends WER a response that indicates the status.</span></span>

<span data-ttu-id="ce42b-119">Con este proceso, WER recopila más información si es necesario o envía una solución al usuario cuando está disponible.</span><span class="sxs-lookup"><span data-stu-id="ce42b-119">Using this process, WER gathers more information if needed or sends a solution to the user when available.</span></span> <span data-ttu-id="ce42b-120">En Windows Vista, el usuario puede ir a **informes de problemas y soluciones** en cualquier momento para ver las soluciones disponibles, comprobar si hay nuevas soluciones disponibles o administrar los demás informes y valores de wer.</span><span class="sxs-lookup"><span data-stu-id="ce42b-120">On Windows Vista, the user can go to **Problem Reports and Solutions** at any time to view available solutions, check whether new solutions are available, or manage their other WER reports and settings.</span></span> <span data-ttu-id="ce42b-121">En Windows 7, los **informes de problemas y las soluciones** ahora se denominan **centro de actividades**.</span><span class="sxs-lookup"><span data-stu-id="ce42b-121">On Windows 7, the **Problem Reports and Solutions** is now called the **Action Center**.</span></span> <span data-ttu-id="ce42b-122">Haga clic en **Inicio** y escriba "ver" en **Buscar programas y archivos** y, a continuación, seleccione **Ver todos los informes de problemas**, **ver el historial de confiabilidad** o **ver soluciones a problemas**.</span><span class="sxs-lookup"><span data-stu-id="ce42b-122">Click **Start** and enter "view" in **Search programs and files** and then select **View all problem reports**, **View reliability history**, or **View solutions to problems**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce42b-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ce42b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce42b-124">Informe de errores de Windows</span><span class="sxs-lookup"><span data-stu-id="ce42b-124">Windows Error Reporting</span></span>](windows-error-reporting.md)
</dt> </dl>

 

 





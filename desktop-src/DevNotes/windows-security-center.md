---
description: Centro de seguridad de Windows
ms.assetid: FF0D7B81-AFDC-4DB2-B2B0-0D2536B2757B
title: Centro de seguridad de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 694185b0a0fed7af9c2ab3d7965674c02354c079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152782"
---
# <a name="windows-security-center"></a><span data-ttu-id="c7597-103">Centro de seguridad de Windows</span><span class="sxs-lookup"><span data-stu-id="c7597-103">Windows Security Center</span></span>

<span data-ttu-id="c7597-104">Windows Security Center (WSC) es una completa herramienta de informes que ayuda a los usuarios a establecer y mantener un nivel de seguridad de protección alrededor de sus sistemas informáticos.</span><span class="sxs-lookup"><span data-stu-id="c7597-104">Windows Security Center (WSC) is a comprehensive reporting tool that helps users establish and maintain a protective security layer around their computer systems.</span></span> <span data-ttu-id="c7597-105">Una vez establecida una capa de seguridad, Windows Security Center es invisible a medida que supervisa el estado de mantenimiento del equipo.</span><span class="sxs-lookup"><span data-stu-id="c7597-105">Once a security layer is established, Windows Security Center is inconspicuous as it monitors the computer’s health state.</span></span> <span data-ttu-id="c7597-106">Sin embargo, si existen vulnerabilidades, WSC proporciona alertas e instrucciones prescriptivas para ayudar al usuario a lograr un estado seguro que se muestra al usuario final a través del centro de actividades.</span><span class="sxs-lookup"><span data-stu-id="c7597-106">However, if vulnerabilities exist, WSC provides alerts and prescriptive guidance to assist the user in achieving a secure state which is surfaced to the end user through the Action Center.</span></span>

<span data-ttu-id="c7597-107">Para que las soluciones de seguridad de terceros (antivirus, antimalware o anti spyware) sean compatibles con Windows y notifiquen correctamente el estado en el centro de actividades, es necesario registrarse con Security Center e informar de los cambios de estado posteriores mediante las API privadas para la comunicación con el objeto WSC.</span><span class="sxs-lookup"><span data-stu-id="c7597-107">In order for third party security solutions (antivirus, antimalware, or antispyware) to be compliant with Windows and successfully report status to Action Center, they are required to register themselves with Security Center and report any subsequent status changes using private APIs for communicating with WSC.</span></span> <span data-ttu-id="c7597-108">WSC, a su vez, comunica estas actualizaciones al centro de actividades, donde finalmente se muestran al usuario final.</span><span class="sxs-lookup"><span data-stu-id="c7597-108">WSC, in turn, communicates these updates to Action Center, where they are finally displayed to the end user.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c7597-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="c7597-109">In this section</span></span>

-   [<span data-ttu-id="c7597-110">Enumeraciones de Security Center de Windows</span><span class="sxs-lookup"><span data-stu-id="c7597-110">Windows Security Center Enumerations</span></span>](windows-security-center-enumerations.md)
-   [<span data-ttu-id="c7597-111">Interfaces de Security Center de Windows</span><span class="sxs-lookup"><span data-stu-id="c7597-111">Windows Security Center Interfaces</span></span>](windows-security-center-interfaces.md)
-   [<span data-ttu-id="c7597-112">Funciones de Security Center de Windows</span><span class="sxs-lookup"><span data-stu-id="c7597-112">Windows Security Center Functions</span></span>](windows-security-center-functions.md)

 

 




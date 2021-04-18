---
description: En este documento se proporciona información sobre las consideraciones de seguridad relacionadas con la adquisición de imágenes de Windows (WIA).
ms.assetid: 35455320-7d08-49de-938d-40dc0873917b
title: 'Consideraciones de seguridad: adquisición de imágenes de Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ab080582492a0c03eab7879624bfb49a370e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715183"
---
# <a name="security-considerations-windows-image-acquisition"></a><span data-ttu-id="7aa7b-103">Consideraciones de seguridad: adquisición de imágenes de Windows</span><span class="sxs-lookup"><span data-stu-id="7aa7b-103">Security Considerations: Windows Image Acquisition</span></span>

<span data-ttu-id="7aa7b-104">En este documento se proporciona información sobre las consideraciones de seguridad relacionadas con la adquisición de imágenes de Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="7aa7b-104">This document provides information about security considerations related to Windows Image Acquisition (WIA).</span></span> <span data-ttu-id="7aa7b-105">En este documento no se proporciona todo lo que necesita saber acerca de los problemas de seguridad; en su lugar, úselo como punto de partida y referencia para esta área tecnológica.</span><span class="sxs-lookup"><span data-stu-id="7aa7b-105">This document doesn't provide all you need to know about security issues - instead, use it as a starting point and reference for this technology area.</span></span>

-   [<span data-ttu-id="7aa7b-106">Usar comillas alrededor de los nombres de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="7aa7b-106">Use quotation marks around path names</span></span>](#use-quotation-marks-around-path-names)
-   [<span data-ttu-id="7aa7b-107">Colocar aplicaciones registradas en ubicaciones seguras</span><span class="sxs-lookup"><span data-stu-id="7aa7b-107">Place registered applications in secure locations</span></span>](#place-registered-applications-in-secure-locations)
-   [<span data-ttu-id="7aa7b-108">No usar directorios subyacentes ni claves del registro</span><span class="sxs-lookup"><span data-stu-id="7aa7b-108">Do not use underlying directories or registry keys</span></span>](#do-not-use-underlying-directories-or-registry-keys)
-   [<span data-ttu-id="7aa7b-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7aa7b-109">Related Topics</span></span>](#related-topics)

## <a name="use-quotation-marks-around-path-names"></a><span data-ttu-id="7aa7b-110">Usar comillas alrededor de los nombres de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="7aa7b-110">Use quotation marks around path names</span></span>

<span data-ttu-id="7aa7b-111">Al usar [**IWiaDevMgr:: RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) para registrar una aplicación para recibir eventos de dispositivo, asegúrese de encerrar la ruta de acceso y el nombre de archivo de la aplicación entre comillas.</span><span class="sxs-lookup"><span data-stu-id="7aa7b-111">When using [**IWiaDevMgr::RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) to register an application to receive device events, be sure to surround the path and filename of the application with quotation marks.</span></span> <span data-ttu-id="7aa7b-112">Esto evita la posibilidad de que la ruta de acceso se interprete erróneamente y se ejecute una aplicación no autorizada.</span><span class="sxs-lookup"><span data-stu-id="7aa7b-112">This avoids the possibility that the path is misinterpreted and an unauthorized application is run.</span></span>

## <a name="place-registered-applications-in-secure-locations"></a><span data-ttu-id="7aa7b-113">Colocar aplicaciones registradas en ubicaciones seguras</span><span class="sxs-lookup"><span data-stu-id="7aa7b-113">Place registered applications in secure locations</span></span>

<span data-ttu-id="7aa7b-114">Cuando una aplicación se registra para recibir un evento de dispositivo, la aplicación puede ejecutarla cualquier usuario que tenga acceso a dicho dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7aa7b-114">When an application is registered to receive a device event, that application can be run by any user that has access to that device.</span></span> <span data-ttu-id="7aa7b-115">Por ejemplo, si una aplicación se registra para un evento de análisis, al presionar el botón "examinar" en un escáner se ejecutará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7aa7b-115">For example, if an application is registered for a scan event, pressing the "scan" button on a scanner will cause that application to run.</span></span> <span data-ttu-id="7aa7b-116">Si la aplicación se ejecuta con un privilegio más alto del que tiene el usuario, se produce un posible problema de seguridad.</span><span class="sxs-lookup"><span data-stu-id="7aa7b-116">If the application runs with a higher privilege than the user has, this causes a potential security issue.</span></span>

## <a name="do-not-use-underlying-directories-or-registry-keys"></a><span data-ttu-id="7aa7b-117">No usar directorios subyacentes ni claves del registro</span><span class="sxs-lookup"><span data-stu-id="7aa7b-117">Do not use underlying directories or registry keys</span></span>

<span data-ttu-id="7aa7b-118">WIA usa varios directorios y claves del registro internamente para almacenar datos o información.</span><span class="sxs-lookup"><span data-stu-id="7aa7b-118">WIA uses several directories and registry keys internally to store data or information.</span></span> <span data-ttu-id="7aa7b-119">No tener acceso directamente a estos directorios o claves del registro.</span><span class="sxs-lookup"><span data-stu-id="7aa7b-119">Do not access these directories or registry keys directly.</span></span> <span data-ttu-id="7aa7b-120">En su lugar, use los métodos de interfaz expuestos para especificar los directorios de las imágenes adquiridas.</span><span class="sxs-lookup"><span data-stu-id="7aa7b-120">Instead, use the exposed interface methods to specify directories for acquired images.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7aa7b-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7aa7b-121">Related Topics</span></span>

-   [<span data-ttu-id="7aa7b-122">Seguridad de Microsoft</span><span class="sxs-lookup"><span data-stu-id="7aa7b-122">Microsoft Security</span></span>](https://www.microsoft.com/security/)
-   [<span data-ttu-id="7aa7b-123">Página principal de seguridad de MSDN Library</span><span class="sxs-lookup"><span data-stu-id="7aa7b-123">MSDN Library Security Home Page</span></span>](https://msdn.microsoft.com/security/default.aspx)
-   [<span data-ttu-id="7aa7b-124">Recursos de procedimientos de seguridad</span><span class="sxs-lookup"><span data-stu-id="7aa7b-124">Security How-to Resources</span></span>](https://www.microsoft.com/technet/solutionaccelerators/howto/sechow.mspx)
-   [<span data-ttu-id="7aa7b-125">Recursos de seguridad de TechNet</span><span class="sxs-lookup"><span data-stu-id="7aa7b-125">TechNet Security Resources</span></span>](https://technet.microsoft.com/security/default.aspx)
-   <span data-ttu-id="7aa7b-126">[Consideraciones de seguridad para desarrolladores de Windows XP Embedded](/previous-versions/ms838345(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7aa7b-126">[Security Considerations for Windows XP Embedded Developers](/previous-versions/ms838345(v=msdn.10))</span></span>
-   [<span data-ttu-id="7aa7b-127">Prácticas recomendadas de seguridad</span><span class="sxs-lookup"><span data-stu-id="7aa7b-127">Security Best Practices</span></span>](../secbp/best-practices-for-the-security-apis.md)

 

 

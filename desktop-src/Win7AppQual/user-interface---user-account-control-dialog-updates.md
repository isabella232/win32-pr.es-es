---
description: 'Interfaz de usuario: actualizaciones del cuadro de diálogo Control de cuentas de usuario'
ms.assetid: f2d4b82d-a84a-4fc1-b7ad-cdc92a24f889
title: 'Interfaz de usuario: actualizaciones del cuadro de diálogo Control de cuentas de usuario'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5cd6cc6709283c7bd9cba3e26bd2df29bb02ec2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094423"
---
# <a name="user-interface---user-account-control-dialog-updates"></a><span data-ttu-id="99886-103">Interfaz de usuario: actualizaciones del cuadro de diálogo Control de cuentas de usuario</span><span class="sxs-lookup"><span data-stu-id="99886-103">User Interface - User Account Control Dialog Updates</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="99886-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="99886-104">Affected Platforms</span></span>

<span data-ttu-id="99886-105">**Clientes:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="99886-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="99886-106">**Servidores:** Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="99886-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="99886-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="99886-107">Feature Impact</span></span>

<span data-ttu-id="99886-108">**Gravedad:** baja</span><span class="sxs-lookup"><span data-stu-id="99886-108">**Severity** - Low</span></span>  
<span data-ttu-id="99886-109">**Frecuencia:** media</span><span class="sxs-lookup"><span data-stu-id="99886-109">**Frequency** - Medium</span></span>  











## <a name="description"></a><span data-ttu-id="99886-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="99886-110">Description</span></span>

<span data-ttu-id="99886-111">En Windows 7, hemos estandarizado las opciones del cuadro de diálogo UAC.</span><span class="sxs-lookup"><span data-stu-id="99886-111">In Windows 7, we have standardized the UAC dialog box choices.</span></span> <span data-ttu-id="99886-112">Anteriormente, los usuarios tenían que seleccionar entre varias opciones, por ejemplo, "Continuar", "Cancelar", y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="99886-112">Previously, users had to select from multiple options, for example, "Continue," "Cancel," and so on.</span></span> <span data-ttu-id="99886-113">Ahora todos los cuadros de diálogo dan a los usuarios un simple "Sí" o "No".</span><span class="sxs-lookup"><span data-stu-id="99886-113">Now all dialog boxes give users a simple "Yes" or "No."</span></span> <span data-ttu-id="99886-114">El diseño del cuadro de diálogo ahora también muestra claramente el nombre del programa, el publicador y el origen.</span><span class="sxs-lookup"><span data-stu-id="99886-114">The dialog layout now also clearly shows the program name, publisher, and origin.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="99886-115">Aprovechamiento de las funcionalidades de características</span><span class="sxs-lookup"><span data-stu-id="99886-115">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="99886-116">Los requisitos de desarrollo de aplicaciones en Windows 7 para la compatibilidad con UAC son los mismos que en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="99886-116">The application development requirements in Windows 7 for UAC compatibility are the same as in Windows Vista.</span></span> <span data-ttu-id="99886-117">Las aplicaciones compatibles con Windows Vista interactuarán con UAC en Windows 7 sin modificaciones.</span><span class="sxs-lookup"><span data-stu-id="99886-117">Windows Vista-compatible applications will interact with UAC in Windows 7 without any modifications.</span></span> <span data-ttu-id="99886-118">Consulte los temas de Control de cuentas de usuario en la Guía de compatibilidad de aplicaciones de *Windows Vista* para obtener información sobre cómo hacer que las aplicaciones de Windows XP funcionen correctamente en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="99886-118">See the User Account Control topics in the *Windows Vista Application Compatibility Cookbook* for information about how to make Windows XP applications work correctly on Windows 7.</span></span> <span data-ttu-id="99886-119">Aunque las mejoras de UAC para Windows 7 afectarán a la experiencia del usuario, no afectarán a la interfaz de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="99886-119">While the UAC improvements for Windows 7 will impact the user's experience, they will not impact the application interface.</span></span> <span data-ttu-id="99886-120">Sin embargo, si hay contenido de ayuda vinculado a los diálogos de UAC, es posible que tenga que actualizar las capturas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="99886-120">However, if there is any help content linked to the UAC dialogs, you may need to update the screenshots.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="99886-121">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="99886-121">Links to Other Resources</span></span>

-   <span data-ttu-id="99886-122">[Guía de compatibilidad de aplicaciones de Windows Vista](/previous-versions/bb757005(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="99886-122">[Windows Vista Application Compatibility Cookbook](/previous-versions/bb757005(v=msdn.10))</span></span>
-   [<span data-ttu-id="99886-123">Descarga del kit de herramientas de compatibilidad de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="99886-123">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="99886-124">[Analizador de usuario estándar](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="99886-124">[Standard User Analyzer](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))</span></span>

> [!Note]  
> <span data-ttu-id="99886-125">Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones.</span><span class="sxs-lookup"><span data-stu-id="99886-125">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 

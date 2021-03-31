---
description: .
ms.assetid: ce5db84a-53b6-4a7f-bee4-d198d8a6781e
title: Informe de errores de Windows la grabadora de pasos del problema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25fb70acef867b878063bd6011fde6867f7f0e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818070"
---
# <a name="windows-error-reporting-problem-steps-recorder"></a><span data-ttu-id="2b1db-103">Informe de errores de Windows la grabadora de pasos del problema</span><span class="sxs-lookup"><span data-stu-id="2b1db-103">Windows Error Reporting Problem Steps Recorder</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="2b1db-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="2b1db-104">Affected Platforms</span></span>

<span data-ttu-id="2b1db-105">**Clientes** : Windows 7</span><span class="sxs-lookup"><span data-stu-id="2b1db-105">**Clients** – Windows 7</span></span>  
<span data-ttu-id="2b1db-106">**Servidores** : Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2b1db-106">**Servers** – Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="2b1db-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b1db-107">Description</span></span>

<span data-ttu-id="2b1db-108">Antes de Windows 7, Informe de errores de Windows (WER) recopilaba informes de errores que indicaban problemas en la necesidad de reparación.</span><span class="sxs-lookup"><span data-stu-id="2b1db-108">Prior to Windows 7, Windows Error Reporting (WER) collected error reports that indicated problems in need of repair.</span></span> <span data-ttu-id="2b1db-109">Estos informes de errores contienen información útil que describe la naturaleza general de un problema, pero no hay información suficiente para determinar su causa principal.</span><span class="sxs-lookup"><span data-stu-id="2b1db-109">These error reports contain helpful information that describes the general nature of a problem, but not enough information to determine its root cause.</span></span> <span data-ttu-id="2b1db-110">Para ello, los desarrolladores necesitan una herramienta para reproducir el escenario de bloqueo y bloqueo para la depuración.</span><span class="sxs-lookup"><span data-stu-id="2b1db-110">For that, developers need a tool to reproduce the crash/hang scenario for debugging.</span></span>

<span data-ttu-id="2b1db-111">Una nueva aplicación, la grabadora de pasos de problemas (PSR.exe), se envía a todas las compilaciones de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2b1db-111">A new application, Problem Steps Recorder (PSR.exe), is shipping on all builds of Windows 7.</span></span> <span data-ttu-id="2b1db-112">Esta característica habilita la recopilación de las acciones realizadas por un usuario a la vez que encuentra un bloqueo para que los evaluadores y los desarrolladores puedan reproducir la situación de análisis y depuración.</span><span class="sxs-lookup"><span data-stu-id="2b1db-112">This feature enables the collection of the actions performed by a user while encountering a crash so that testers and developers can reproduce the situation for analysis and debugging.</span></span>

## <a name="usage"></a><span data-ttu-id="2b1db-113">Uso</span><span class="sxs-lookup"><span data-stu-id="2b1db-113">Usage</span></span>

<span data-ttu-id="2b1db-114">Actualmente, un desarrollador de servicios de Informe de errores de Windows debe solicitar la habilitación de los PSR para una aplicación; Las organizaciones de soporte técnico de Microsoft también usan esta herramienta mientras solucionan problemas con los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="2b1db-114">Currently, a Windows Error Reporting service developer must request PSR enablement for an application; Microsoft support organizations also use this tool while troubleshooting with end users.</span></span> <span data-ttu-id="2b1db-115">Los planes están en vigor para que PSR esté disponible en Windows Quality Online Services (WinQual) después del lanzamiento de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2b1db-115">Plans are in place to make PSR available at Windows Quality Online Services (Winqual) after the release of Windows 7.</span></span>

<span data-ttu-id="2b1db-116">**Nota:** Con PSR habilitado para una aplicación, la aplicación puede ver una degradación del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="2b1db-116">**Note:** With PSR enabled for an application, the application may see some performance degradation.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="2b1db-117">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="2b1db-117">Links to Other Resources</span></span>

-   [<span data-ttu-id="2b1db-118">Informe de errores de Windows entrada de blog</span><span class="sxs-lookup"><span data-stu-id="2b1db-118">Windows Error Reporting blog entry</span></span>](/archive/blogs/wer/)
-   [<span data-ttu-id="2b1db-119">Servicios en línea de calidad de Windows (WinQual)</span><span class="sxs-lookup"><span data-stu-id="2b1db-119">Windows Quality Online Services (Winqual)</span></span>](https://winqual.microsoft.com)

 

 

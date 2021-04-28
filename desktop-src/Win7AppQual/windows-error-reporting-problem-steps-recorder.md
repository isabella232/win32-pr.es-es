---
description: Informe de errores de Windows Grabación de acciones de usuario
ms.assetid: ce5db84a-53b6-4a7f-bee4-d198d8a6781e
title: Informe de errores de Windows Grabación de acciones de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46abb8adf545152e34c2b2100022068291e3571f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084163"
---
# <a name="windows-error-reporting-problem-steps-recorder"></a><span data-ttu-id="6b9d5-103">Informe de errores de Windows Grabación de acciones de usuario</span><span class="sxs-lookup"><span data-stu-id="6b9d5-103">Windows Error Reporting Problem Steps Recorder</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="6b9d5-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="6b9d5-104">Affected Platforms</span></span>

<span data-ttu-id="6b9d5-105">**Clientes:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="6b9d5-105">**Clients** – Windows 7</span></span>  
<span data-ttu-id="6b9d5-106">**Servidores:** Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6b9d5-106">**Servers** – Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="6b9d5-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b9d5-107">Description</span></span>

<span data-ttu-id="6b9d5-108">Antes de Windows 7, Informe de errores de Windows (WER) recopilaba informes de errores que indicaban problemas que necesitaban reparación.</span><span class="sxs-lookup"><span data-stu-id="6b9d5-108">Prior to Windows 7, Windows Error Reporting (WER) collected error reports that indicated problems in need of repair.</span></span> <span data-ttu-id="6b9d5-109">Estos informes de error contienen información útil que describe la naturaleza general de un problema, pero no suficiente información para determinar su causa principal.</span><span class="sxs-lookup"><span data-stu-id="6b9d5-109">These error reports contain helpful information that describes the general nature of a problem, but not enough information to determine its root cause.</span></span> <span data-ttu-id="6b9d5-110">Para ello, los desarrolladores necesitan una herramienta para reproducir el escenario de bloqueo o bloqueo para la depuración.</span><span class="sxs-lookup"><span data-stu-id="6b9d5-110">For that, developers need a tool to reproduce the crash/hang scenario for debugging.</span></span>

<span data-ttu-id="6b9d5-111">Una nueva aplicación, Grabación de acciones de usuario (PSR.exe), se está enviando en todas las compilaciones de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6b9d5-111">A new application, Problem Steps Recorder (PSR.exe), is shipping on all builds of Windows 7.</span></span> <span data-ttu-id="6b9d5-112">Esta característica permite la recopilación de las acciones realizadas por un usuario al encontrar un bloqueo para que los evaluadores y desarrolladores puedan reproducir la situación para su análisis y depuración.</span><span class="sxs-lookup"><span data-stu-id="6b9d5-112">This feature enables the collection of the actions performed by a user while encountering a crash so that testers and developers can reproduce the situation for analysis and debugging.</span></span>

## <a name="usage"></a><span data-ttu-id="6b9d5-113">Uso</span><span class="sxs-lookup"><span data-stu-id="6b9d5-113">Usage</span></span>

<span data-ttu-id="6b9d5-114">Actualmente, un desarrollador Informe de errores de Windows servicio debe solicitar la habilitación de PSR para una aplicación; Las organizaciones de soporte técnico de Microsoft también usan esta herramienta al solucionar problemas con los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="6b9d5-114">Currently, a Windows Error Reporting service developer must request PSR enablement for an application; Microsoft support organizations also use this tool while troubleshooting with end users.</span></span> <span data-ttu-id="6b9d5-115">Hay planes para que PSR esté disponible en Windows Quality Online Services (Winqual) después del lanzamiento de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6b9d5-115">Plans are in place to make PSR available at Windows Quality Online Services (Winqual) after the release of Windows 7.</span></span>

<span data-ttu-id="6b9d5-116">**Nota:** Con PSR habilitado para una aplicación, es posible que la aplicación vea alguna degradación del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="6b9d5-116">**Note:** With PSR enabled for an application, the application may see some performance degradation.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="6b9d5-117">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="6b9d5-117">Links to Other Resources</span></span>

-   [<span data-ttu-id="6b9d5-118">Informe de errores de Windows entrada de blog</span><span class="sxs-lookup"><span data-stu-id="6b9d5-118">Windows Error Reporting blog entry</span></span>](/archive/blogs/wer/)
-   [<span data-ttu-id="6b9d5-119">Windows Quality Online Services (Winqual)</span><span class="sxs-lookup"><span data-stu-id="6b9d5-119">Windows Quality Online Services (Winqual)</span></span>](https://winqual.microsoft.com)

 

 

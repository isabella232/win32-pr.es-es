---
description: El Windows Installer proporciona muchas acciones integradas para realizar el proceso de instalación. Para obtener una lista de estas acciones, consulte la referencia de acciones estándar.
ms.assetid: 4a1f3ccc-4904-47d0-bfc6-013e404de47e
title: Acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9623351bdcd4cd109d2112724d13e0f9ccaa6b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082786"
---
# <a name="custom-actions"></a><span data-ttu-id="bb129-104">Acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="bb129-104">Custom Actions</span></span>

<span data-ttu-id="bb129-105">El Windows Installer proporciona muchas acciones integradas para realizar el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="bb129-105">The Windows Installer provides many built-in actions for performing the installation process.</span></span> <span data-ttu-id="bb129-106">Para obtener una lista de estas acciones, consulte la [referencia de acciones estándar](standard-actions-reference.md).</span><span class="sxs-lookup"><span data-stu-id="bb129-106">For a list of these actions, see the [Standard Actions Reference](standard-actions-reference.md).</span></span>

<span data-ttu-id="bb129-107">Las acciones estándar son suficientes para ejecutar una instalación en la mayoría de los casos.</span><span class="sxs-lookup"><span data-stu-id="bb129-107">Standard actions are sufficient to execute an installation in most cases.</span></span> <span data-ttu-id="bb129-108">Sin embargo, hay situaciones en las que el desarrollador de un paquete de instalación encuentra que es necesario escribir una acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="bb129-108">However, there are situations where the developer of an installation package finds it necessary to write a custom action.</span></span> <span data-ttu-id="bb129-109">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="bb129-109">For example:</span></span>

-   <span data-ttu-id="bb129-110">Quiere iniciar un archivo ejecutable durante la instalación que está instalado en el equipo del usuario o que se está instalando con la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bb129-110">You want to launch an executable during installation that is installed on the user's machine or that is being installed with the application.</span></span>
-   <span data-ttu-id="bb129-111">Desea llamar a funciones especiales durante una instalación definida en una biblioteca de vínculos dinámicos (DLL).</span><span class="sxs-lookup"><span data-stu-id="bb129-111">You want to call special functions during an installation that are defined in a dynamic-link library (DLL).</span></span>
-   <span data-ttu-id="bb129-112">Quiere usar funciones escritas en los lenguajes de desarrollo Microsoft Visual Basic Scripting Edition o el texto de script literal de Microsoft JScript durante una instalación.</span><span class="sxs-lookup"><span data-stu-id="bb129-112">You want to use functions written in the development languages Microsoft Visual Basic Scripting Edition or Microsoft JScript literal script text during an installation.</span></span>
-   <span data-ttu-id="bb129-113">Desea aplazar la ejecución de algunas acciones hasta el momento en que se ejecuta el script de instalación.</span><span class="sxs-lookup"><span data-stu-id="bb129-113">You want to defer the execution of some actions until the time when the installation script is being executed.</span></span>
-   <span data-ttu-id="bb129-114">Desea agregar información de tiempo y progreso a un control ProgressBar y a un control de texto TimeRemaining.</span><span class="sxs-lookup"><span data-stu-id="bb129-114">You want to add time and progress information to a ProgressBar control and a TimeRemaining Text control.</span></span>

<span data-ttu-id="bb129-115">En las secciones siguientes se describen las acciones personalizadas y cómo incorporarlas en un paquete de instalación:</span><span class="sxs-lookup"><span data-stu-id="bb129-115">The following sections describe custom actions and how to incorporate them into an installation package:</span></span>

-   [<span data-ttu-id="bb129-116">Acerca de las acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="bb129-116">About Custom Actions</span></span>](about-custom-actions.md)
-   [<span data-ttu-id="bb129-117">Uso de acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="bb129-117">Using Custom Actions</span></span>](using-custom-actions.md)
-   [<span data-ttu-id="bb129-118">Referencia de acción personalizada</span><span class="sxs-lookup"><span data-stu-id="bb129-118">Custom Action Reference</span></span>](custom-action-reference.md)
-   [<span data-ttu-id="bb129-119">Lista de Resumen de todos los tipos de acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="bb129-119">Summary List of All Custom Action Types</span></span>](summary-list-of-all-custom-action-types.md)

 

 




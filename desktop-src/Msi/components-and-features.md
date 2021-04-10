---
description: El Windows Installer organiza una instalación en torno a los conceptos de componentes y características.
ms.assetid: c560441e-89c5-4f82-837b-988c3f404d37
title: Componentes y características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b21241c98fbb701bd6a3ef5869045ef8c46da1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155140"
---
# <a name="components-and-features"></a><span data-ttu-id="fe4e2-103">Componentes y características</span><span class="sxs-lookup"><span data-stu-id="fe4e2-103">Components and Features</span></span>

<span data-ttu-id="fe4e2-104">El Windows Installer organiza una instalación en torno a los conceptos de componentes y características.</span><span class="sxs-lookup"><span data-stu-id="fe4e2-104">The Windows Installer organizes an installation around the concepts of components and features.</span></span>

<span data-ttu-id="fe4e2-105">Una característica forma parte de la funcionalidad total de la aplicación que un usuario puede decidir instalar de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="fe4e2-105">A feature is a part of the application's total functionality that a user may decide to install independently.</span></span> <span data-ttu-id="fe4e2-106">Para obtener más información, vea [características de Windows Installer](windows-installer-features.md).</span><span class="sxs-lookup"><span data-stu-id="fe4e2-106">For more information, see [Windows Installer Features](windows-installer-features.md).</span></span>

<span data-ttu-id="fe4e2-107">Un componente es una parte de la aplicación o del producto que se va a instalar.</span><span class="sxs-lookup"><span data-stu-id="fe4e2-107">A component is a piece of the application or product to be installed.</span></span> <span data-ttu-id="fe4e2-108">El instalador siempre instala o quita un componente del equipo de un usuario como una pieza coherente.</span><span class="sxs-lookup"><span data-stu-id="fe4e2-108">The installer always installs or removes a component from a user's computer as a coherent piece.</span></span> <span data-ttu-id="fe4e2-109">Los componentes suelen estar ocultos para el usuario.</span><span class="sxs-lookup"><span data-stu-id="fe4e2-109">Components are usually hidden from the user.</span></span> <span data-ttu-id="fe4e2-110">Cuando un usuario selecciona una característica para la instalación, el instalador determina qué componentes deben instalarse para proporcionar esa característica.</span><span class="sxs-lookup"><span data-stu-id="fe4e2-110">When a user selects a feature for installation, the installer determines which components must be installed to provide that feature.</span></span> <span data-ttu-id="fe4e2-111">Para obtener más información, vea [componentes de Windows Installer](windows-installer-components.md).</span><span class="sxs-lookup"><span data-stu-id="fe4e2-111">For more information, see [Windows Installer Components](windows-installer-components.md).</span></span>

<span data-ttu-id="fe4e2-112">Los autores de los paquetes de instalación deben decidir cómo dividir la aplicación en características y componentes.</span><span class="sxs-lookup"><span data-stu-id="fe4e2-112">Authors of installation packages need to decide how to divide their application into features and components.</span></span> <span data-ttu-id="fe4e2-113">La selección de características viene determinada principalmente por la funcionalidad de la aplicación desde la perspectiva del usuario.</span><span class="sxs-lookup"><span data-stu-id="fe4e2-113">The selection of features is primarily determined by the application's functionality from the user's perspective.</span></span> <span data-ttu-id="fe4e2-114">Dado que los componentes normalmente se deben compartir entre las aplicaciones, o incluso entre productos, se recomienda que los autores sigan un método estándar para seleccionar los componentes.</span><span class="sxs-lookup"><span data-stu-id="fe4e2-114">Because components commonly must be shared across applications, or even across products, it is recommended that authors follow a standard method for selecting components.</span></span> <span data-ttu-id="fe4e2-115">Para obtener más información, vea [organizar aplicaciones en componentes](organizing-applications-into-components.md).</span><span class="sxs-lookup"><span data-stu-id="fe4e2-115">For more information, see [Organizing Applications into Components](organizing-applications-into-components.md).</span></span>

 

 




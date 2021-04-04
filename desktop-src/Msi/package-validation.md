---
description: Se recomienda encarecidamente ejecutar la validación en cada paquete de instalación nuevo o recién modificado antes de intentar instalar el paquete por primera vez.
ms.assetid: 47168c0b-82ab-4f1b-84d7-98c8f64d6da0
title: Validación de paquetes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058fbd5bff08701f9603938a631de4e8a59857d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908706"
---
# <a name="package-validation"></a><span data-ttu-id="7e8f6-103">Validación de paquetes</span><span class="sxs-lookup"><span data-stu-id="7e8f6-103">Package Validation</span></span>

<span data-ttu-id="7e8f6-104">Se recomienda encarecidamente ejecutar la validación en cada paquete de instalación nuevo o recién modificado antes de intentar instalar el paquete por primera vez.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-104">It is strongly recommended that you run validation on every new or newly modified installation package before attempting to install the package for the first time.</span></span>

<span data-ttu-id="7e8f6-105">La validación de paquetes incluye los tres procesos siguientes:</span><span class="sxs-lookup"><span data-stu-id="7e8f6-105">Package validation includes the following three processes:</span></span>

-   [<span data-ttu-id="7e8f6-106">Validación interna</span><span class="sxs-lookup"><span data-stu-id="7e8f6-106">Internal Validation</span></span>](internal-validation.md)
-   [<span data-ttu-id="7e8f6-107">Validación de grupo de cadenas</span><span class="sxs-lookup"><span data-stu-id="7e8f6-107">String-Pool Validation</span></span>](string-pool-validation.md)
-   [<span data-ttu-id="7e8f6-108">Evaluadores de coherencia interna-CIEM</span><span class="sxs-lookup"><span data-stu-id="7e8f6-108">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)

<span data-ttu-id="7e8f6-109">Los módulos de combinación deben validarse mediante el método descrito en [validación de módulos de combinación](validating-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="7e8f6-109">Merge modules should be validated by using the method described in [Validating Merge Modules](validating-merge-modules.md).</span></span>

<span data-ttu-id="7e8f6-110">Evalcom2.dll proporciona un objeto COM que implementa las operaciones de validación para los paquetes de instalación y los módulos de combinación.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-110">Evalcom2.dll provides a COM object that implements validation operations for installation packages and merge modules.</span></span> <span data-ttu-id="7e8f6-111">El objeto principal implementa interfaces para programas de C/C++.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-111">The main object implements interfaces for C/C++ programs.</span></span> <span data-ttu-id="7e8f6-112">Para obtener más información, vea automatización de la [validación](validation-automation.md).</span><span class="sxs-lookup"><span data-stu-id="7e8f6-112">For more information, see [Validation Automation](validation-automation.md).</span></span>

 

 




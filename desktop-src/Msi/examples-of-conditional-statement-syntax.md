---
description: A continuación se proporcionan algunas instancias comunes de instrucciones condicionales. Para obtener más información, vea sintaxis de la instrucción condicional.
ms.assetid: 8b6bae7a-20ae-494c-bd96-66bd537c8630
title: Ejemplos de sintaxis de instrucciones condicionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca91a2b3e89160fad19ad5d9b1c6a3d33929e5d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001652"
---
# <a name="examples-of-conditional-statement-syntax"></a><span data-ttu-id="4b709-104">Ejemplos de sintaxis de instrucciones condicionales</span><span class="sxs-lookup"><span data-stu-id="4b709-104">Examples of Conditional Statement Syntax</span></span>

<span data-ttu-id="4b709-105">A continuación se proporcionan algunas instancias comunes de instrucciones condicionales.</span><span class="sxs-lookup"><span data-stu-id="4b709-105">The following provides some common instances of conditional statements.</span></span> <span data-ttu-id="4b709-106">Para obtener más información, vea sintaxis de la [instrucción condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="4b709-106">For more information, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

## <a name="run-action-on-removal"></a><span data-ttu-id="4b709-107">Ejecutar acción al quitar.</span><span class="sxs-lookup"><span data-stu-id="4b709-107">Run action on removal.</span></span>

<span data-ttu-id="4b709-108">Para obtener más información, consulte [acondicionamiento de acciones para ejecutar durante la eliminación](conditioning-actions-to-run-during-removal.md).</span><span class="sxs-lookup"><span data-stu-id="4b709-108">For information, see [Conditioning Actions to Run During Removal](conditioning-actions-to-run-during-removal.md).</span></span>

## <a name="run-action-only-if-the-product-has-not-been-installed"></a><span data-ttu-id="4b709-109">Ejecutar acción solo si el producto no se ha instalado.</span><span class="sxs-lookup"><span data-stu-id="4b709-109">Run action only if the product has not been installed.</span></span>

``` syntax
NOT Installed
```

## <a name="run-action-only-if-the-product-will-be-installed-local-do-not-run-action-on-a-reinstallation"></a><span data-ttu-id="4b709-110">Ejecute la acción solo si el producto se va a instalar local.</span><span class="sxs-lookup"><span data-stu-id="4b709-110">Run action only if the product will be installed local.</span></span> <span data-ttu-id="4b709-111">No ejecute la acción en una reinstalación.</span><span class="sxs-lookup"><span data-stu-id="4b709-111">Do not run action on a reinstallation.</span></span>

``` syntax
(&FeatureName=3) AND NOT(!FeatureName=3)
```

<span data-ttu-id="4b709-112">El término "&FeatureName = 3" significa que la acción es instalar la característica local.</span><span class="sxs-lookup"><span data-stu-id="4b709-112">The term "&FeatureName=3" means the action is to install the feature local.</span></span> <span data-ttu-id="4b709-113">El término "no (! FeatureName = 3) "significa que la característica no está instalada localmente.</span><span class="sxs-lookup"><span data-stu-id="4b709-113">The term "NOT(!FeatureName=3)" means the feature is not installed local.</span></span>

## <a name="run-action-only-if-the-feature-will-be-uninstalled"></a><span data-ttu-id="4b709-114">Ejecute la acción solo si se va a desinstalar la característica.</span><span class="sxs-lookup"><span data-stu-id="4b709-114">Run action only if the feature will be uninstalled.</span></span>

``` syntax
(&FeatureName=2) AND (!FeatureName=3)
```

<span data-ttu-id="4b709-115">Esta condición solo comprueba si hay una transición de la característica de un estado instalado local al estado ausente.</span><span class="sxs-lookup"><span data-stu-id="4b709-115">This condition only checks for a transition of the feature from an installed state of local to the absent state.</span></span>

## <a name="run-action-only-if-the-component-was-installed-local-but-is-transitioning-out-of-state"></a><span data-ttu-id="4b709-116">Ejecute la acción solo si el componente se instaló localmente, pero está pasando del estado.</span><span class="sxs-lookup"><span data-stu-id="4b709-116">Run action only if the component was installed local, but is transitioning out of state.</span></span>

``` syntax
(?ComponentName=3) AND ($ComponentName=2 OR $ComponentName=4)
```

<span data-ttu-id="4b709-117">El término "? ComponetName = 3 "significa que el componente está instalado localmente.</span><span class="sxs-lookup"><span data-stu-id="4b709-117">The term "?ComponetName=3" means the component is installed local.</span></span> <span data-ttu-id="4b709-118">El término "$ComponentName = 2" significa que falta el estado de la acción en el componente.</span><span class="sxs-lookup"><span data-stu-id="4b709-118">The term "$ComponentName=2" means that the action state on the component is Absent.</span></span> <span data-ttu-id="4b709-119">El término "$ComponentName = 4" significa que el estado de la acción en el componente se ejecuta desde el origen.</span><span class="sxs-lookup"><span data-stu-id="4b709-119">The term "$ComponentName=4" means that the action state on the component is run from source.</span></span> <span data-ttu-id="4b709-120">Tenga en cuenta que un estado de acción de anunciad no es válido para un componente.</span><span class="sxs-lookup"><span data-stu-id="4b709-120">Note that an action state of advertise is not valid for a component.</span></span>

## <a name="run-action-only-on-the-reinstallation-of-a-component"></a><span data-ttu-id="4b709-121">Ejecutar acción solo en la reinstalación de un componente.</span><span class="sxs-lookup"><span data-stu-id="4b709-121">Run action only on the reinstallation of a component.</span></span>

``` syntax
?ComponentName=$ComponentName
```

## <a name="run-action-only-when-a-particular-patch-is-applied"></a><span data-ttu-id="4b709-122">Ejecutar acción solo cuando se aplica una revisión determinada.</span><span class="sxs-lookup"><span data-stu-id="4b709-122">Run action only when a particular patch is applied.</span></span>

``` syntax
PATCH AND PATCH >< MEDIASRCPROPNAME
```

<span data-ttu-id="4b709-123">Para obtener más información, vea la sección Comentarios de la página de propiedades [**revisión**](patch.md) .</span><span class="sxs-lookup"><span data-stu-id="4b709-123">For more information, see the Remarks section on the [**PATCH**](patch.md) property page.</span></span>

 

 




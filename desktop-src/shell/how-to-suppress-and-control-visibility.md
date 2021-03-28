---
description: En este tema se explica cómo controlar la visibilidad de los verbos.
title: Cómo suprimir y controlar la visibilidad de los verbos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f689d8b93ce9facb62b654f3f8be62f665e001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276744"
---
# <a name="how-to-suppress-and-control-verb-visibility"></a><span data-ttu-id="4719a-103">Cómo suprimir y controlar la visibilidad de los verbos</span><span class="sxs-lookup"><span data-stu-id="4719a-103">How to Suppress and Control Verb Visibility</span></span>

<span data-ttu-id="4719a-104">En este tema se explica cómo controlar la visibilidad de los verbos.</span><span class="sxs-lookup"><span data-stu-id="4719a-104">This topic tells you how to control verb visibility.</span></span>

## <a name="instructions"></a><span data-ttu-id="4719a-105">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="4719a-105">Instructions</span></span>


<span data-ttu-id="4719a-106">Puede usar la configuración de directiva de Windows para controlar la visibilidad de los verbos.</span><span class="sxs-lookup"><span data-stu-id="4719a-106">You can use Windows policy settings to control verb visibility.</span></span> <span data-ttu-id="4719a-107">Los verbos se pueden suprimir a través de la configuración de la Directiva agregando una subclave **SuppressionPolicy** o un valor GUID **SuppressionPolicyEx** a la subclave del registro del verbo.</span><span class="sxs-lookup"><span data-stu-id="4719a-107">Verbs can be suppressed through policy settings by adding a **SuppressionPolicy** subkey or a **SuppressionPolicyEx** GUID value to the verb's registry subkey.</span></span> <span data-ttu-id="4719a-108">Establezca el valor de la subclave **SuppressionPolicy** en el identificador de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="4719a-108">Set the value of the **SuppressionPolicy** subkey to the policy ID.</span></span> <span data-ttu-id="4719a-109">Si la Directiva está activada, se suprimen el verbo y su entrada de menú contextual asociada.</span><span class="sxs-lookup"><span data-stu-id="4719a-109">If the policy is turned on, the verb and its associated shortcut menu entry are suppressed.</span></span> <span data-ttu-id="4719a-110">Para ver los posibles valores de ID. de Directiva, consulte la enumeración [**restrictions**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) .</span><span class="sxs-lookup"><span data-stu-id="4719a-110">For possible policy ID values, see the [**RESTRICTIONS**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) enumeration.</span></span>

 

 




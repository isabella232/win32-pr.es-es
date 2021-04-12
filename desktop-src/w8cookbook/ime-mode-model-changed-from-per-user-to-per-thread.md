---
title: Cambios en el modelo de modo IME
description: Modelo de modo IME cambiado de por usuario a por subproceso
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781c322949f17d4d3313b6a9b7b5eff9b1e83b06
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359314"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a><span data-ttu-id="8c32d-103">Modelo de modo IME cambiado de por usuario a por subproceso</span><span class="sxs-lookup"><span data-stu-id="8c32d-103">IME mode model changed from per-user to per-thread</span></span>

## <a name="platforms"></a><span data-ttu-id="8c32d-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="8c32d-104">Platforms</span></span>

<dl> <span data-ttu-id="8c32d-105">Clientes-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8c32d-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="8c32d-106">Servidores: Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8c32d-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="8c32d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c32d-107">Description</span></span>

<span data-ttu-id="8c32d-108">En Windows 8, el modo de conversión de IME y el modo de oración IME se basaban en el contexto de usuario y el cambio de modo de una aplicación afectaba a todas las demás aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8c32d-108">In Windows 8, the IME Conversion Mode and IME Sentence Mode were based on the User context, and changing the mode of an application affected all other applications.</span></span> <span data-ttu-id="8c32d-109">Este comportamiento se puede deshabilitar mediante la configuración de la opción "permitirme establecer un método de entrada diferente para cada aplicación" en la sección Configuración avanzada del panel de control del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="8c32d-109">This behavior could be disabled by using the "Let me set a different input method for each app window" setting in the advanced settings section of the language control panel.</span></span>

<span data-ttu-id="8c32d-110">Con el fin de mejorar la compatibilidad, en Windows 8.1 los modos se almacenan en un contexto de entrada independientemente de la forma en que se establece el control "permitirme establecer un método de entrada diferente para cada ventana de la aplicación".</span><span class="sxs-lookup"><span data-stu-id="8c32d-110">In order to improve compatibility, in Windows 8.1 the modes are stored in an Input context regardless of how the "Let me set a different input method for each app window" control is set.</span></span> <span data-ttu-id="8c32d-111">En Windows 8.1, la configuración "permitirme establecer un método de entrada diferente para cada aplicación" afecta solo a la selección del propio método de entrada.</span><span class="sxs-lookup"><span data-stu-id="8c32d-111">In Windows 8.1, the "Let me set a different input method for each app window" setting affects only the selection of the input method itself.</span></span>

<span data-ttu-id="8c32d-112">Al iniciarse la aplicación, el modo IME se establece en los valores predeterminados siguientes:</span><span class="sxs-lookup"><span data-stu-id="8c32d-112">At application start up, the IME mode is set to the following defaults:</span></span>



|          | <span data-ttu-id="8c32d-113">Panel de entrada de software</span><span class="sxs-lookup"><span data-stu-id="8c32d-113">Software input panel</span></span> | <span data-ttu-id="8c32d-114">Teclado de hardware</span><span class="sxs-lookup"><span data-stu-id="8c32d-114">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="8c32d-115">KOR, JPN</span><span class="sxs-lookup"><span data-stu-id="8c32d-115">KOR, JPN</span></span> | <span data-ttu-id="8c32d-116">Activado</span><span class="sxs-lookup"><span data-stu-id="8c32d-116">On</span></span>                   | <span data-ttu-id="8c32d-117">Off</span><span class="sxs-lookup"><span data-stu-id="8c32d-117">Off</span></span>               |
| <span data-ttu-id="8c32d-118">CHS, CHT</span><span class="sxs-lookup"><span data-stu-id="8c32d-118">CHS,CHT</span></span>  | <span data-ttu-id="8c32d-119">Activado</span><span class="sxs-lookup"><span data-stu-id="8c32d-119">On</span></span>                   | <span data-ttu-id="8c32d-120">Activado</span><span class="sxs-lookup"><span data-stu-id="8c32d-120">On</span></span>                |



 

## <a name="manifestations"></a><span data-ttu-id="8c32d-121">Manifestaciones</span><span class="sxs-lookup"><span data-stu-id="8c32d-121">Manifestations</span></span>

<span data-ttu-id="8c32d-122">Cuando un usuario cambia el modo IME en una aplicación, el cambio no afecta a otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8c32d-122">When a user changes the IME mode on an application, the change doesn’t affect other applications.</span></span>

## <a name="resources"></a><span data-ttu-id="8c32d-123">Recursos</span><span class="sxs-lookup"><span data-stu-id="8c32d-123">Resources</span></span>

-   [<span data-ttu-id="8c32d-124">Valores del modo de conversión IME</span><span class="sxs-lookup"><span data-stu-id="8c32d-124">IME Conversion Mode Values</span></span>](../intl/ime-conversion-mode-values.md)
-   [<span data-ttu-id="8c32d-125">Valores del modo de oración IME</span><span class="sxs-lookup"><span data-stu-id="8c32d-125">IME Sentence Mode Values</span></span>](../intl/ime-sentence-mode-values.md)

 

 
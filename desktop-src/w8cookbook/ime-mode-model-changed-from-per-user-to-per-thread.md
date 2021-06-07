---
title: Cambios en el modelo de modo IME
description: Modelo de modo IME cambiado de por usuario a por subproceso
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30404b1a386c4346e7d8900481d8c5198972cdbe
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443255"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a><span data-ttu-id="9863e-103">Modelo de modo IME cambiado de por usuario a por subproceso</span><span class="sxs-lookup"><span data-stu-id="9863e-103">IME mode model changed from per-user to per-thread</span></span>

## <a name="platforms"></a><span data-ttu-id="9863e-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="9863e-104">Platforms</span></span>

<dl> <span data-ttu-id="9863e-105">Clientes: Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9863e-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="9863e-106">Servidores: Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9863e-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="9863e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="9863e-107">Description</span></span>

<span data-ttu-id="9863e-108">En Windows 8, el modo de conversión de IME y el modo de oración de IME se basaban en el contexto de usuario y el cambio del modo de una aplicación afectaba a todas las demás aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="9863e-108">In Windows 8, the IME Conversion Mode and IME Sentence Mode were based on the User context, and changing the mode of an application affected all other applications.</span></span> <span data-ttu-id="9863e-109">Este comportamiento podría deshabilitarse mediante el valor "Let me set a different input method for each app window" (Permitirme establecer un método de entrada diferente para cada ventana de la aplicación) en la sección de configuración avanzada del panel de control de idioma.</span><span class="sxs-lookup"><span data-stu-id="9863e-109">This behavior could be disabled by using the "Let me set a different input method for each app window" setting in the advanced settings section of the language control panel.</span></span>

<span data-ttu-id="9863e-110">Para mejorar la compatibilidad, en Windows 8.1 los modos se almacenan en un contexto de entrada independientemente de cómo se establezca el control "Let me set a different input method for each app window" (Permitirme establecer un método de entrada diferente para cada ventana de la aplicación).</span><span class="sxs-lookup"><span data-stu-id="9863e-110">In order to improve compatibility, in Windows 8.1 the modes are stored in an Input context regardless of how the "Let me set a different input method for each app window" control is set.</span></span> <span data-ttu-id="9863e-111">En Windows 8.1, el valor "Let me set a different input method for each app window" (Permitirme establecer un método de entrada diferente para cada ventana de la aplicación) solo afecta a la selección del propio método de entrada.</span><span class="sxs-lookup"><span data-stu-id="9863e-111">In Windows 8.1, the "Let me set a different input method for each app window" setting affects only the selection of the input method itself.</span></span>

<span data-ttu-id="9863e-112">Al iniciar la aplicación, el modo IME se establece en los valores predeterminados siguientes:</span><span class="sxs-lookup"><span data-stu-id="9863e-112">At application start up, the IME mode is set to the following defaults:</span></span>



| &nbsp;   | <span data-ttu-id="9863e-113">Panel de entrada de software</span><span class="sxs-lookup"><span data-stu-id="9863e-113">Software input panel</span></span> | <span data-ttu-id="9863e-114">Teclado de hardware</span><span class="sxs-lookup"><span data-stu-id="9863e-114">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="9863e-115">KOR, JPN</span><span class="sxs-lookup"><span data-stu-id="9863e-115">KOR, JPN</span></span> | <span data-ttu-id="9863e-116">Activado</span><span class="sxs-lookup"><span data-stu-id="9863e-116">On</span></span>                   | <span data-ttu-id="9863e-117">Desactivado</span><span class="sxs-lookup"><span data-stu-id="9863e-117">Off</span></span>               |
| <span data-ttu-id="9863e-118">CHS,CHT</span><span class="sxs-lookup"><span data-stu-id="9863e-118">CHS,CHT</span></span>  | <span data-ttu-id="9863e-119">Activado</span><span class="sxs-lookup"><span data-stu-id="9863e-119">On</span></span>                   | <span data-ttu-id="9863e-120">Activado</span><span class="sxs-lookup"><span data-stu-id="9863e-120">On</span></span>                |



 

## <a name="manifestations"></a><span data-ttu-id="9863e-121">Manifestaciones</span><span class="sxs-lookup"><span data-stu-id="9863e-121">Manifestations</span></span>

<span data-ttu-id="9863e-122">Cuando un usuario cambia el modo IME en una aplicación, el cambio no afecta a otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="9863e-122">When a user changes the IME mode on an application, the change doesn’t affect other applications.</span></span>

## <a name="resources"></a><span data-ttu-id="9863e-123">Recursos</span><span class="sxs-lookup"><span data-stu-id="9863e-123">Resources</span></span>

-   [<span data-ttu-id="9863e-124">Valores del modo de conversión de IME</span><span class="sxs-lookup"><span data-stu-id="9863e-124">IME Conversion Mode Values</span></span>](../intl/ime-conversion-mode-values.md)
-   [<span data-ttu-id="9863e-125">Valores del modo de oración de IME</span><span class="sxs-lookup"><span data-stu-id="9863e-125">IME Sentence Mode Values</span></span>](../intl/ime-sentence-mode-values.md)

 

 
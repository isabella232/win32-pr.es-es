---
description: Contiene el estado actual de generación de la señal de un PIN.
ms.assetid: 07D76F8D-C5B5-4500-BFA2-452989868027
title: Estructura de PWM_PIN_IS_STARTED_OUTPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_IS_STARTED_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 11350c3bb0fbec0f05ab3153c339f8fa30baeed5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659352"
---
# <a name="pwm_pin_is_started_output-structure"></a><span data-ttu-id="d0bd1-103">La \_ estructura de salida del PIN de PWM \_ es \_ iniciada \_</span><span class="sxs-lookup"><span data-stu-id="d0bd1-103">PWM\_PIN\_IS\_STARTED\_OUTPUT structure</span></span>

<span data-ttu-id="d0bd1-104">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="d0bd1-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d0bd1-105">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="d0bd1-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d0bd1-106">Contiene el estado actual de generación de la señal de un PIN.</span><span class="sxs-lookup"><span data-stu-id="d0bd1-106">Contains the current signal generation state of a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0bd1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0bd1-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_IS_STARTED_OUTPUT {
  BOOLEAN IsStarted;
} PWM_PIN_IS_STARTED_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="d0bd1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d0bd1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d0bd1-109">**IsStarted (**</span><span class="sxs-lookup"><span data-stu-id="d0bd1-109">**IsStarted**</span></span>
</dt> <dd>

<span data-ttu-id="d0bd1-110">Estado de generación de la señal actual del PIN.</span><span class="sxs-lookup"><span data-stu-id="d0bd1-110">The pin current signal generation state.</span></span> <span data-ttu-id="d0bd1-111">Un valor de true significa que el PIN se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="d0bd1-111">A value of true means that the pin is started.</span></span> <span data-ttu-id="d0bd1-112">Un valor de false significa que el PIN está detenido.</span><span class="sxs-lookup"><span data-stu-id="d0bd1-112">A value of false means that the pin is stopped.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d0bd1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0bd1-113">Requirements</span></span>



| <span data-ttu-id="d0bd1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0bd1-114">Requirement</span></span> | <span data-ttu-id="d0bd1-115">Value</span><span class="sxs-lookup"><span data-stu-id="d0bd1-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0bd1-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0bd1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d0bd1-117">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="d0bd1-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d0bd1-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0bd1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d0bd1-119">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="d0bd1-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d0bd1-120">Versión mínima de KMDF</span><span class="sxs-lookup"><span data-stu-id="d0bd1-120">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="d0bd1-121">1.19</span><span class="sxs-lookup"><span data-stu-id="d0bd1-121">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="d0bd1-122">Versión mínima de UMDF</span><span class="sxs-lookup"><span data-stu-id="d0bd1-122">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="d0bd1-123">2.19</span><span class="sxs-lookup"><span data-stu-id="d0bd1-123">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="d0bd1-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0bd1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0bd1-125"><dt>PWM. h (incluir PWM. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0bd1-125"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0bd1-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0bd1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0bd1-127">**\_ \_ \_ se inició el PIN de PWM de ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="d0bd1-127">**IOCTL\_PWM\_PIN\_IS\_STARTED**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**)
</dt> </dl>

 

 





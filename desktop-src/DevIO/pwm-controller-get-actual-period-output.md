---
description: Contiene el período de la señal de salida efectiva para un controlador de modulación de ancho de pulso (PWM).
ms.assetid: 280F564F-FF7F-4121-B726-9F9AF9E98EB7
title: Estructura de PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: f63057299a8ef37ed1b38151958d2e0061ad2727
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807406"
---
# <a name="pwm_controller_get_actual_period_output-structure"></a><span data-ttu-id="c2c86-103">La \_ \_ estructura de \_ \_ salida del período real \_ del controlador de PWM</span><span class="sxs-lookup"><span data-stu-id="c2c86-103">PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD\_OUTPUT structure</span></span>

<span data-ttu-id="c2c86-104">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="c2c86-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c2c86-105">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="c2c86-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c2c86-106">Contiene el período de la señal de salida efectiva para un controlador de modulación de ancho de pulso (PWM).</span><span class="sxs-lookup"><span data-stu-id="c2c86-106">Contains the effective output signal period for a Pulse Width Modulation (PWM) controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2c86-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2c86-107">Syntax</span></span>


```C++
typedef struct _PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT {
  PWM_PERIOD ActualPeriod;
} PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="c2c86-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="c2c86-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c2c86-109">**ActualPeriod**</span><span class="sxs-lookup"><span data-stu-id="c2c86-109">**ActualPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="c2c86-110">El período efectivo de la señal de salida como se mediría en los canales de salida del controlador.</span><span class="sxs-lookup"><span data-stu-id="c2c86-110">The effective output signal period as it would be measured on the output channels of the controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c2c86-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2c86-111">Requirements</span></span>



| <span data-ttu-id="c2c86-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2c86-112">Requirement</span></span> | <span data-ttu-id="c2c86-113">Value</span><span class="sxs-lookup"><span data-stu-id="c2c86-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2c86-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2c86-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c2c86-115">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="c2c86-115">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c2c86-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2c86-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c2c86-117">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="c2c86-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c2c86-118">Versión mínima de KMDF</span><span class="sxs-lookup"><span data-stu-id="c2c86-118">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="c2c86-119">1.19</span><span class="sxs-lookup"><span data-stu-id="c2c86-119">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="c2c86-120">Versión mínima de UMDF</span><span class="sxs-lookup"><span data-stu-id="c2c86-120">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="c2c86-121">2.19</span><span class="sxs-lookup"><span data-stu-id="c2c86-121">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="c2c86-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c2c86-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2c86-123"><dt>PWM. h (incluir PWM. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2c86-123"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2c86-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2c86-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2c86-125">**el \_ controlador de PWM de ioctl \_ obtiene el \_ \_ \_ período real**</span><span class="sxs-lookup"><span data-stu-id="c2c86-125">**IOCTL\_PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD**)
</dt> </dl>

 

 





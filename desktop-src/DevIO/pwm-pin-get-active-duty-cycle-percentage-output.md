---
description: Contiene el porcentaje de ciclo de servicio actual de un PIN o canal en un controlador de modulación de ancho de pulso (PWM).
ms.assetid: 09C0232A-DF5C-4A1C-8138-D3D65E45731B
title: Estructura de PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 607fcb1ab429e7cbe9aee593f75d48f0f9d308bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153086"
---
# <a name="pwm_pin_get_active_duty_cycle_percentage_output-structure"></a><span data-ttu-id="d384b-103">La \_ \_ estructura de \_ \_ salida del \_ porcentaje del ciclo de servicio \_ de un \_ PIN de PWM</span><span class="sxs-lookup"><span data-stu-id="d384b-103">PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_OUTPUT structure</span></span>

<span data-ttu-id="d384b-104">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="d384b-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d384b-105">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="d384b-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d384b-106">Contiene el porcentaje de ciclo de servicio actual de un PIN o canal en un controlador de modulación de ancho de pulso (PWM).</span><span class="sxs-lookup"><span data-stu-id="d384b-106">Contains the current duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="d384b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d384b-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="d384b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d384b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d384b-109">**Porcentaje**</span><span class="sxs-lookup"><span data-stu-id="d384b-109">**Percentage**</span></span>
</dt> <dd>

<span data-ttu-id="d384b-110">Ciclo de arancel de la señal de PWM actual, como un porcentaje de PWM \_ , que es un valor de ULONGLONG.</span><span class="sxs-lookup"><span data-stu-id="d384b-110">The current PWM signal duty cycle, as a PWM\_PERCENTAGE, which is a ULONGLONG value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d384b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d384b-111">Requirements</span></span>



| <span data-ttu-id="d384b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d384b-112">Requirement</span></span> | <span data-ttu-id="d384b-113">Value</span><span class="sxs-lookup"><span data-stu-id="d384b-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d384b-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d384b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d384b-115">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="d384b-115">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d384b-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d384b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d384b-117">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="d384b-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d384b-118">Versión mínima de KMDF</span><span class="sxs-lookup"><span data-stu-id="d384b-118">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="d384b-119">1.19</span><span class="sxs-lookup"><span data-stu-id="d384b-119">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="d384b-120">Versión mínima de UMDF</span><span class="sxs-lookup"><span data-stu-id="d384b-120">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="d384b-121">2.19</span><span class="sxs-lookup"><span data-stu-id="d384b-121">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="d384b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d384b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d384b-123"><dt>PWM. h (incluir PWM. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d384b-123"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d384b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d384b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d384b-125">**\_porcentaje de \_ \_ ciclo de \_ \_ servicio activo \_ \_ de ioctl de ioctl**</span><span class="sxs-lookup"><span data-stu-id="d384b-125">**IOCTL\_PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 





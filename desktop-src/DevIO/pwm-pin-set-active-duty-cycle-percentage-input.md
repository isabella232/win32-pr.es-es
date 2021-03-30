---
description: Contiene un porcentaje de ciclo de servicio deseado para un PIN o canal en un controlador de modulación de ancho de pulso (PWM).
ms.assetid: CA699703-2D9B-4841-99AD-9C27FF428394
title: Estructura de PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 98811ace7ce8fce760e10757b8bf012cc2b9b27d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423203"
---
# <a name="pwm_pin_set_active_duty_cycle_percentage_input-structure"></a><span data-ttu-id="90bad-103">\_Estructura de \_ \_ \_ \_ \_ entrada porcentual del porcentaje de ciclo de servicio activo \_</span><span class="sxs-lookup"><span data-stu-id="90bad-103">PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_INPUT structure</span></span>

<span data-ttu-id="90bad-104">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="90bad-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="90bad-105">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="90bad-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="90bad-106">Contiene un porcentaje de ciclo de servicio deseado para un PIN o canal en un controlador de modulación de ancho de pulso (PWM).</span><span class="sxs-lookup"><span data-stu-id="90bad-106">Contains a desired duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="90bad-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90bad-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT;
```



## <a name="members"></a><span data-ttu-id="90bad-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="90bad-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="90bad-109">**Porcentaje**</span><span class="sxs-lookup"><span data-stu-id="90bad-109">**Percentage**</span></span>
</dt> <dd>

<span data-ttu-id="90bad-110">El ciclo de servicio de la señal de PWM deseado, como un porcentaje de PWM \_ , que es un valor de ULONGLONG.</span><span class="sxs-lookup"><span data-stu-id="90bad-110">The desired PWM signal duty cycle, as a PWM\_PERCENTAGE, which is a ULONGLONG value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90bad-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90bad-111">Requirements</span></span>



| <span data-ttu-id="90bad-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="90bad-112">Requirement</span></span> | <span data-ttu-id="90bad-113">Value</span><span class="sxs-lookup"><span data-stu-id="90bad-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90bad-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90bad-114">Minimum supported client</span></span><br/> | <span data-ttu-id="90bad-115">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="90bad-115">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="90bad-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90bad-116">Minimum supported server</span></span><br/> | <span data-ttu-id="90bad-117">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="90bad-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="90bad-118">Versión mínima de KMDF</span><span class="sxs-lookup"><span data-stu-id="90bad-118">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="90bad-119">1.19</span><span class="sxs-lookup"><span data-stu-id="90bad-119">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="90bad-120">Versión mínima de UMDF</span><span class="sxs-lookup"><span data-stu-id="90bad-120">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="90bad-121">2.19</span><span class="sxs-lookup"><span data-stu-id="90bad-121">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="90bad-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90bad-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="90bad-123"><dt>PWM. h (incluir PWM. h)</dt></span><span class="sxs-lookup"><span data-stu-id="90bad-123"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90bad-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="90bad-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90bad-125">**\_porcentaje de \_ \_ ciclo de \_ arancel activo del conjunto \_ de \_ pines \_ de ioctl**</span><span class="sxs-lookup"><span data-stu-id="90bad-125">**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 





---
description: Contiene un valor de polaridad que se va a devolver.
ms.assetid: 432C10EF-AC08-4781-9BCA-A31E0DF12704
title: Estructura de PWM_PIN_GET_POLARITY_OUTPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_POLARITY_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 81cf7b658a0024c3280db1523af34aaf2ef17262
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998257"
---
# <a name="pwm_pin_get_polarity_output-structure"></a><span data-ttu-id="319a3-103">Estructura de salida de la \_ \_ \_ \_ estructura de los pines de PWM</span><span class="sxs-lookup"><span data-stu-id="319a3-103">PWM\_PIN\_GET\_POLARITY\_OUTPUT structure</span></span>

<span data-ttu-id="319a3-104">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="319a3-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="319a3-105">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="319a3-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="319a3-106">Contiene un valor de polaridad que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="319a3-106">Contains a polarity value to return.</span></span>

## <a name="syntax"></a><span data-ttu-id="319a3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="319a3-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_GET_POLARITY_OUTPUT {
  PWM_POLARITY Polarity;
} PWM_PIN_GET_POLARITY_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="319a3-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="319a3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="319a3-109">**Polaridad**</span><span class="sxs-lookup"><span data-stu-id="319a3-109">**Polarity**</span></span>
</dt> <dd>

<span data-ttu-id="319a3-110">Polaridad del PIN o canal como valor de polaridad de [**PWM \_**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) .</span><span class="sxs-lookup"><span data-stu-id="319a3-110">The polarity of the pin or channel as a [**PWM\_POLARITY**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) value.</span></span> <span data-ttu-id="319a3-111">La polaridad es alta o activa baja.</span><span class="sxs-lookup"><span data-stu-id="319a3-111">The polarity is either Active High or Active Low.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="319a3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="319a3-112">Requirements</span></span>



| <span data-ttu-id="319a3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="319a3-113">Requirement</span></span> | <span data-ttu-id="319a3-114">Value</span><span class="sxs-lookup"><span data-stu-id="319a3-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="319a3-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="319a3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="319a3-116">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="319a3-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="319a3-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="319a3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="319a3-118">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="319a3-118">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="319a3-119">Versión mínima de KMDF</span><span class="sxs-lookup"><span data-stu-id="319a3-119">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="319a3-120">1.19</span><span class="sxs-lookup"><span data-stu-id="319a3-120">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="319a3-121">Versión mínima de UMDF</span><span class="sxs-lookup"><span data-stu-id="319a3-121">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="319a3-122">2.19</span><span class="sxs-lookup"><span data-stu-id="319a3-122">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="319a3-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="319a3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="319a3-124"><dt>PWM. h (incluir PWM. h)</dt></span><span class="sxs-lookup"><span data-stu-id="319a3-124"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="319a3-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="319a3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="319a3-126">**PIN de PWM de IOCTL \_ \_ \_ obtener \_ polarización**</span><span class="sxs-lookup"><span data-stu-id="319a3-126">**IOCTL\_PWM\_PIN\_GET\_POLARITY**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_POLARITY**)
</dt> <dt>

[<span data-ttu-id="319a3-127">**polaridad de PWM \_**</span><span class="sxs-lookup"><span data-stu-id="319a3-127">**PWM\_POLARITY**</span></span>](/windows/win32/api/pwm/ne-pwm-pwm_polarity)
</dt> </dl>

 


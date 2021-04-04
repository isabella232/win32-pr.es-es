---
description: 'Más información sobre: estructuras PWM'
ms.assetid: 992E3913-C1C4-48C1-A550-475CF44AB065
title: Estructuras de PWM
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99511820f8500cd8df827a80664f6c274d732665
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998256"
---
# <a name="pwm-structures"></a><span data-ttu-id="cffb2-103">Estructuras de PWM</span><span class="sxs-lookup"><span data-stu-id="cffb2-103">PWM Structures</span></span>

<span data-ttu-id="cffb2-104">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="cffb2-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cffb2-105">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="cffb2-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cffb2-106">Las siguientes estructuras se usan con la modulación de ancho de pulsos:</span><span class="sxs-lookup"><span data-stu-id="cffb2-106">The following structures are used with Pulse Width Modulation:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cffb2-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="cffb2-107">In this section</span></span>



| <span data-ttu-id="cffb2-108">Tema</span><span class="sxs-lookup"><span data-stu-id="cffb2-108">Topic</span></span>                                                                                                                        | <span data-ttu-id="cffb2-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="cffb2-109">Description</span></span>                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cffb2-110">**el \_ controlador de PWM \_ obtiene la \_ \_ salida del período real \_**</span><span class="sxs-lookup"><span data-stu-id="cffb2-110">**PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD\_OUTPUT**</span></span>](pwm-controller-get-actual-period-output.md)<br/>                   | <span data-ttu-id="cffb2-111">Contiene el período de la señal de salida efectiva para un controlador de modulación de ancho de pulso (PWM).</span><span class="sxs-lookup"><span data-stu-id="cffb2-111">Contains the effective output signal period for a Pulse Width Modulation (PWM) controller.</span></span><br/>                    |
| [<span data-ttu-id="cffb2-112">**\_información del controlador de PWM \_**</span><span class="sxs-lookup"><span data-stu-id="cffb2-112">**PWM\_CONTROLLER\_INFO**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_controller_info)<br/>                                                              | <span data-ttu-id="cffb2-113">Representa la información estática que caracteriza un controlador de modulación de ancho de pulsos (PWM).</span><span class="sxs-lookup"><span data-stu-id="cffb2-113">Represents the static information that characterizes a Pulse Width Modulation (PWM) controller.</span></span> <br/>              |
| [<span data-ttu-id="cffb2-114">**\_entrada de \_ \_ período deseado \_ del conjunto de controladores de \_ PWM**</span><span class="sxs-lookup"><span data-stu-id="cffb2-114">**PWM\_CONTROLLER\_SET\_DESIRED\_PERIOD\_INPUT**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_controller_set_desired_period_input)<br/>                   | <span data-ttu-id="cffb2-115">Contiene un valor de entrada para un período de señal sugerido para el controlador de modulación de ancho de pulso (PWM).</span><span class="sxs-lookup"><span data-stu-id="cffb2-115">Contains an input value for a suggested signal period for the Pulse Width Modulation (PWM) controller.</span></span> <br/>       |
| [<span data-ttu-id="cffb2-116">**\_resultado del \_ \_ período deseado \_ del conjunto de controladores de \_ PWM**</span><span class="sxs-lookup"><span data-stu-id="cffb2-116">**PWM\_CONTROLLER\_SET\_DESIRED\_PERIOD\_OUTPUT**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_controller_set_desired_period_output)<br/>                 | <span data-ttu-id="cffb2-117">Contiene el período de la señal de salida efectiva del controlador de modulación de ancho de pulso (PWM).</span><span class="sxs-lookup"><span data-stu-id="cffb2-117">Contains the effective output signal period of the Pulse Width Modulation (PWM) controller.</span></span><br/>                   |
| [<span data-ttu-id="cffb2-118">**\_salida de \_ \_ porcentaje de \_ ciclo de servicio activo \_ \_ \_ de PWM**</span><span class="sxs-lookup"><span data-stu-id="cffb2-118">**PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_OUTPUT**</span></span>](pwm-pin-get-active-duty-cycle-percentage-output.md)<br/> | <span data-ttu-id="cffb2-119">Contiene el porcentaje de ciclo de servicio actual de un PIN o canal en un controlador de modulación de ancho de pulso (PWM).</span><span class="sxs-lookup"><span data-stu-id="cffb2-119">Contains the current duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span><br/> |
| [<span data-ttu-id="cffb2-120">**\_entrada de \_ \_ porcentaje de \_ ciclo de servicio activo \_ \_ del \_ PIN de PWM**</span><span class="sxs-lookup"><span data-stu-id="cffb2-120">**PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_INPUT**</span></span>](pwm-pin-set-active-duty-cycle-percentage-input.md)<br/>   | <span data-ttu-id="cffb2-121">Contiene un porcentaje de ciclo de servicio deseado para un PIN o canal en un controlador de modulación de ancho de pulso (PWM).</span><span class="sxs-lookup"><span data-stu-id="cffb2-121">Contains a desired duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span><br/>   |
| [<span data-ttu-id="cffb2-122">**\_salida de \_ polaridad de obtención de PIN de \_ PWM \_**</span><span class="sxs-lookup"><span data-stu-id="cffb2-122">**PWM\_PIN\_GET\_POLARITY\_OUTPUT**</span></span>](pwm-pin-get-polarity-output.md)<br/>                                            | <span data-ttu-id="cffb2-123">Contiene un valor de polaridad que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="cffb2-123">Contains a polarity value to return.</span></span><br/>                                                                          |
| [<span data-ttu-id="cffb2-124">**\_entrada de \_ polaridad de conjunto de PIN de \_ PWM \_**</span><span class="sxs-lookup"><span data-stu-id="cffb2-124">**PWM\_PIN\_SET\_POLARITY\_INPUT**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_pin_set_polarity_input)<br/>                                              | <span data-ttu-id="cffb2-125">Contiene un valor deseado para la polaridad de un PIN o canal.</span><span class="sxs-lookup"><span data-stu-id="cffb2-125">Contains a desired value for polarity of a pin or channel.</span></span><br/>                                                    |
| [<span data-ttu-id="cffb2-126">**\_salida de código PIN de PWM \_ \_ iniciada \_**</span><span class="sxs-lookup"><span data-stu-id="cffb2-126">**PWM\_PIN\_IS\_STARTED\_OUTPUT**</span></span>](pwm-pin-is-started-output.md)<br/>                                                | <span data-ttu-id="cffb2-127">Contiene el estado actual de generación de la señal de un PIN.</span><span class="sxs-lookup"><span data-stu-id="cffb2-127">Contains the current signal generation state of a pin.</span></span><br/>                                                        |



 

 

 





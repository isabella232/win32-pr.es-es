---
description: La modulación de ancho de pulsos (PWM) es la técnica de generación de una onda de impulso rectangular que tiene un ancho de pulsos que se modula para producir la variación del valor medio de la forma de onda.
ms.assetid: 16B1E46F-2C42-4D94-949E-BE8F53EB1E1E
title: API DE PWM
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 10b1951d9d96f49a9df9a51604767dbce360f9e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538884"
---
# <a name="pwm-api"></a><span data-ttu-id="ad4c1-103">API DE PWM</span><span class="sxs-lookup"><span data-stu-id="ad4c1-103">PWM API</span></span>

<span data-ttu-id="ad4c1-104">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="ad4c1-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ad4c1-105">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="ad4c1-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ad4c1-106">La modulación de ancho de pulsos (PWM) es la técnica de generación de una onda de impulso rectangular que tiene un ancho de pulsos que se modula para producir la variación del valor medio de la forma de onda.</span><span class="sxs-lookup"><span data-stu-id="ad4c1-106">Pulse Width Modulation (PWM) is the technique of generating a rectangular pulse wave that has a pulse width that is modulated to result in the variation of the average value of the waveform.</span></span> <span data-ttu-id="ad4c1-107">Entre los usos más comunes se incluyen motores cinemáticos de conducción, LED de atenuación u otras funciones relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ad4c1-107">Most common uses include driving servo motors, dimming LEDs, or other related functions.</span></span> <span data-ttu-id="ad4c1-108">PWM está pensado para usarse principalmente en escenarios de Internet de las cosas.</span><span class="sxs-lookup"><span data-stu-id="ad4c1-108">PWM is intended to be used primarily for Internet of Things scenarios.</span></span>

## <a name="about-pulse-width-modulation"></a><span data-ttu-id="ad4c1-109">Acerca de la modulación del ancho del pulso</span><span class="sxs-lookup"><span data-stu-id="ad4c1-109">About Pulse Width Modulation</span></span>

<span data-ttu-id="ad4c1-110">Una forma de onda de PWM se puede clasificar por dos parámetros:</span><span class="sxs-lookup"><span data-stu-id="ad4c1-110">A PWM waveform can be categorized by two parameters:</span></span>

-   <span data-ttu-id="ad4c1-111">Un período de onda (T)</span><span class="sxs-lookup"><span data-stu-id="ad4c1-111">A waveform period (T)</span></span>

-   <span data-ttu-id="ad4c1-112">El ciclo de servicio, donde la frecuencia de la forma de onda (f) es el recíproco del período f = 1/T</span><span class="sxs-lookup"><span data-stu-id="ad4c1-112">The duty cycle, where the waveform frequency (f) is the reciprocal of the period f=1/T</span></span>

<span data-ttu-id="ad4c1-113">El ciclo de servicio describe la proporción de **en** el / tiempo **activo** con respecto al intervalo normal o al **período** de tiempo.</span><span class="sxs-lookup"><span data-stu-id="ad4c1-113">The duty cycle describes the proportion of the **on**/**Active** time with respect to the regular interval or **Period** of time.</span></span> <span data-ttu-id="ad4c1-114">Un ciclo de derechos reducidos corresponde a un promedio de energía de salida baja, ya que la energía está desactivada durante la mayor parte del tiempo.</span><span class="sxs-lookup"><span data-stu-id="ad4c1-114">A low duty cycle corresponds to an average of low output power, because the power is off for most of the time.</span></span> <span data-ttu-id="ad4c1-115">El ciclo de servicio se expresa como un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="ad4c1-115">Duty cycle is expressed as a percentage.</span></span> <span data-ttu-id="ad4c1-116">Totalmente encendido es el 100%.</span><span class="sxs-lookup"><span data-stu-id="ad4c1-116">Fully on is 100%.</span></span> <span data-ttu-id="ad4c1-117">Totalmente desactivado es 0%.</span><span class="sxs-lookup"><span data-stu-id="ad4c1-117">Fully off is 0%.</span></span> <span data-ttu-id="ad4c1-118">La mitad **activa** es el 50%.</span><span class="sxs-lookup"><span data-stu-id="ad4c1-118">**Active** half the time is 50%.</span></span>

<span data-ttu-id="ad4c1-119">Los desarrolladores que deseen implementar PWM en sus aplicaciones de IoT deben investigar la documentación de los de [WinRT.](/uwp/api/windows.devices.pwm)</span><span class="sxs-lookup"><span data-stu-id="ad4c1-119">Developers looking to implement PWM in their IoT applications should investigate the [WinRT PWM documentation.](/uwp/api/windows.devices.pwm)</span></span>

## <a name="pulse-width-modulation-types"></a><span data-ttu-id="ad4c1-120">Tipos de modulación de ancho de pulsos</span><span class="sxs-lookup"><span data-stu-id="ad4c1-120">Pulse Width Modulation types</span></span>

<span data-ttu-id="ad4c1-121">PWM usa [estos códigos de control de e/s](pwm-control-codes.md), [estructuras](pwm-structures.md)y [enumeraciones.](pwm-enumeration-types.md)</span><span class="sxs-lookup"><span data-stu-id="ad4c1-121">PWM uses [these IO control codes](pwm-control-codes.md), [structures](pwm-structures.md), and [enumerations.](pwm-enumeration-types.md)</span></span>

<span data-ttu-id="ad4c1-122">PWM también utiliza la función siguiente: [**PwmParsePinPath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath).</span><span class="sxs-lookup"><span data-stu-id="ad4c1-122">PWM also uses the following function: [**PwmParsePinPath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath).</span></span>

 

 

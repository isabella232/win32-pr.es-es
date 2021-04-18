---
description: La supervisión de dígitos supervisa la llamada de dígitos.
ms.assetid: 6ba28fdf-87d5-4d39-9e12-8201585a86ee
title: Supervisión de dígitos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2454f6886bba4e859348df929c1a35f10c3d481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686634"
---
# <a name="digit-monitoring"></a><span data-ttu-id="9508b-103">Supervisión de dígitos</span><span class="sxs-lookup"><span data-stu-id="9508b-103">Digit Monitoring</span></span>

<span data-ttu-id="9508b-104">La supervisión de dígitos supervisa la llamada de dígitos.</span><span class="sxs-lookup"><span data-stu-id="9508b-104">Digit monitoring monitors the call for digits.</span></span> <span data-ttu-id="9508b-105">TAPI permite que los dígitos se señalen de acuerdo con dos métodos (modos de dígito):</span><span class="sxs-lookup"><span data-stu-id="9508b-105">TAPI allows digits to be signaled according to two methods (digit modes):</span></span>

-   <span data-ttu-id="9508b-106">Los dígitos de pulsos se señalan como secuencias giratorias o con impulsos.</span><span class="sxs-lookup"><span data-stu-id="9508b-106">Pulse Digits are signaled as pulse or rotary sequences.</span></span> <span data-ttu-id="9508b-107">Para la detección, estos impulsos se manifiestan como nada más que las secuencias de clics auditivos.</span><span class="sxs-lookup"><span data-stu-id="9508b-107">For detection, these pulses manifest themselves as nothing more than sequences of audible clicks.</span></span> <span data-ttu-id="9508b-108">Los dígitos de pulso válidos son de "0" a "9".</span><span class="sxs-lookup"><span data-stu-id="9508b-108">Valid pulse digits are '0' through '9'.</span></span>
-   <span data-ttu-id="9508b-109">Los dígitos DTMF se señalan como tonos DTMF (frecuencia múltiple de tono dual).</span><span class="sxs-lookup"><span data-stu-id="9508b-109">DTMF Digits are signaled as DTMF (Dual Tone Multiple Frequency) tones.</span></span> <span data-ttu-id="9508b-110">Los dígitos DTMF válidos son de ' 0 ' a ' 9 ', ' A '.</span><span class="sxs-lookup"><span data-stu-id="9508b-110">Valid DTMF digits are '0' through '9', 'A'.</span></span> <span data-ttu-id="9508b-111">' B ', ' C ', ' d ', ' \* ' y ' \# '.</span><span class="sxs-lookup"><span data-stu-id="9508b-111">'B', 'C', 'D', '\*', and '\#'.</span></span> <span data-ttu-id="9508b-112">Se pueden supervisar tanto el extremo inicial como el borde inferior de los dígitos DTMF.</span><span class="sxs-lookup"><span data-stu-id="9508b-112">Both the beginning and the down edge of DTMF digits can be monitored.</span></span>

<span data-ttu-id="9508b-113">Una aplicación puede habilitar o deshabilitar la supervisión de dígitos en una llamada especificada con [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits).</span><span class="sxs-lookup"><span data-stu-id="9508b-113">An application can enable or disable digit monitoring on a specified call with [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits).</span></span> <span data-ttu-id="9508b-114">Cuando está habilitada la supervisión de dígitos, los dígitos detectados hacen que la aplicación reciba una notificación con el mensaje de [**línea \_ MONITORDIGITS**](line-monitordigits.md) .</span><span class="sxs-lookup"><span data-stu-id="9508b-114">When digit monitoring is enabled, detected digits cause the application to be notified with the [**LINE\_MONITORDIGITS**](line-monitordigits.md) message.</span></span> <span data-ttu-id="9508b-115">Este mensaje proporciona el identificador de llamada en el que se ha detectado el dígito, así como el valor de dígito y el modo de dígito.</span><span class="sxs-lookup"><span data-stu-id="9508b-115">This message provides the call handle on which the digit was detected as well as the digit value and the digit mode.</span></span> <span data-ttu-id="9508b-116">El ámbito de la supervisión de dígitos está limitado por la duración de la llamada.</span><span class="sxs-lookup"><span data-stu-id="9508b-116">The scope of digit monitoring is bound by the lifetime of the call.</span></span> <span data-ttu-id="9508b-117">La supervisión de dígitos en una llamada finaliza en cuanto la llamada se *desconecta* o se queda *inactiva*.</span><span class="sxs-lookup"><span data-stu-id="9508b-117">Digit monitoring on a call ends as soon as the call *disconnects* or goes *idle*.</span></span>

 

 




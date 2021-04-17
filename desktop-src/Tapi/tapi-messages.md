---
description: Los mensajes se utilizan para notificar a la aplicación de eventos asincrónicos. Todos estos mensajes se envían a la aplicación a través del mecanismo de notificación de mensajes que la aplicación especificó en lineInitializeEx.
ms.assetid: d302819e-c522-470a-be5e-52625c9223a4
title: Mensajes TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58307a0230b76c6ad98c57f4590098f0dcf6b236
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688134"
---
# <a name="tapi-messages"></a><span data-ttu-id="247af-104">Mensajes TAPI</span><span class="sxs-lookup"><span data-stu-id="247af-104">TAPI Messages</span></span>

<span data-ttu-id="247af-105">Los mensajes se utilizan para notificar a la aplicación de eventos asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="247af-105">Messages are used to notify the application of asynchronous events.</span></span> <span data-ttu-id="247af-106">Todos estos mensajes se envían a la aplicación a través del mecanismo de notificación de mensajes que la aplicación especificó en [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="247af-106">All of these messages are sent to the application through the message notification mechanism that the application specified in [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span></span>

<span data-ttu-id="247af-107">El mensaje siempre contiene un identificador para el objeto pertinente (teléfono, línea o llamada), que la aplicación puede usar para determinar el tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="247af-107">The message always contains a handle to the relevant object (phone, line, or call), which the application can use to determine the message type.</span></span>

<span data-ttu-id="247af-108">Algunos mensajes se utilizan para notificar a la aplicación sobre un cambio en el estado de un objeto.</span><span class="sxs-lookup"><span data-stu-id="247af-108">Certain messages are used to notify the application about a change in an object's status.</span></span> <span data-ttu-id="247af-109">Estos mensajes proporcionan el identificador de objeto y proporcionan una indicación de qué elemento de Estado ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="247af-109">These messages provide the object handle and give an indication of which status item has changed.</span></span> <span data-ttu-id="247af-110">La aplicación puede llamar a la función "get status" correspondiente del objeto para obtener el estado completo del objeto.</span><span class="sxs-lookup"><span data-stu-id="247af-110">The application can call the appropriate "get status" function of the object to obtain the object's full status.</span></span>

<span data-ttu-id="247af-111">Cuando se produce un evento, los mensajes se pueden enviar a cero, una o más aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="247af-111">When an event occurs, messages can be sent to zero, one, or more applications.</span></span> <span data-ttu-id="247af-112">Las aplicaciones de destino para un mensaje se determinan mediante una serie de factores diferentes, incluido el significado del mensaje, el privilegio de la aplicación en el objeto, si la aplicación inició o no la solicitud para la que el mensaje es un resultado directo y el enmascaramiento de mensajes que ha establecido la aplicación.</span><span class="sxs-lookup"><span data-stu-id="247af-112">The target applications for a message are determined by a number of different factors including the meaning of the message, the application's privilege to the object, whether or not the application initiated the request for which the message is a direct result, and the message masking that has been set by the application.</span></span> <span data-ttu-id="247af-113">Tenga en cuenta los siguientes puntos acerca de los mensajes:</span><span class="sxs-lookup"><span data-stu-id="247af-113">Note the following points about messages:</span></span>

-   <span data-ttu-id="247af-114">Los mensajes de respuesta asincrónica solo se envían a la aplicación que originó la solicitud y no se pueden enmascarar.</span><span class="sxs-lookup"><span data-stu-id="247af-114">Asynchronous reply messages are only sent to the application that originated the request and cannot be masked.</span></span>
-   <span data-ttu-id="247af-115">Los mensajes que señalan la finalización de la generación de dígitos o de tono o la recopilación de dígitos solo se envían a la aplicación que solicitó la generación de dígitos o tono.</span><span class="sxs-lookup"><span data-stu-id="247af-115">Messages that signal the completion of digit or tone generation or the gathering of digits are only sent to the application that requested the digit or tone generation.</span></span>
-   <span data-ttu-id="247af-116">Los mensajes que indican que los cambios de estado de línea o dirección se envían a todas las aplicaciones que han abierto la línea, siempre y cuando el mensaje se haya habilitado a través de [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span><span class="sxs-lookup"><span data-stu-id="247af-116">Messages that indicate line or address state changes are sent to all applications that have opened the line, so long as the message has been enabled through [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span></span>
-   <span data-ttu-id="247af-117">Los mensajes que indican el estado de la llamada y los cambios de la información de llamada se envían a todas las aplicaciones que tienen un identificador a la llamada.</span><span class="sxs-lookup"><span data-stu-id="247af-117">Messages that indicate call state and call information changes are sent to all applications that have a handle to the call.</span></span>
-   <span data-ttu-id="247af-118">Los mensajes que señalan una detección de dígitos, detección de tono o detección de tipo de medio se envían a las aplicaciones que solicitaron la supervisión de ese evento.</span><span class="sxs-lookup"><span data-stu-id="247af-118">Messages that signal a digit detection, tone detection, or media type detection are sent to the applications that requested monitoring of that event.</span></span>

<span data-ttu-id="247af-119">Esta sección contiene la información de referencia para los siguientes mensajes TAPI:</span><span class="sxs-lookup"><span data-stu-id="247af-119">This section contains the reference information for the following TAPI messages:</span></span>

-   [<span data-ttu-id="247af-120">Mensajes de telefonía asistidos</span><span class="sxs-lookup"><span data-stu-id="247af-120">Assisted Telephony Messages</span></span>](assisted-telephony-messages.md)
-   [<span data-ttu-id="247af-121">Mensajes del centro de llamadas</span><span class="sxs-lookup"><span data-stu-id="247af-121">Call Center Messages</span></span>](call-center-messages.md)
-   [<span data-ttu-id="247af-122">Mensajes de error con formato</span><span class="sxs-lookup"><span data-stu-id="247af-122">Formatted Error Messages</span></span>](formatted-error-messages.md)
-   [<span data-ttu-id="247af-123">Mensajes de dispositivo de línea</span><span class="sxs-lookup"><span data-stu-id="247af-123">Line Device Messages</span></span>](line-device-messages.md)
-   [<span data-ttu-id="247af-124">Mensajes de dispositivo telefónico</span><span class="sxs-lookup"><span data-stu-id="247af-124">Phone Device Messages</span></span>](phone-device-messages.md)

 

 




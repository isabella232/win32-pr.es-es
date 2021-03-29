---
description: Winlogon envía mensajes a GINA mientras se muestran los cuadros de diálogo. Estos mensajes se encapsulan en el \_ mensaje SAS de WLX WM \_ como se indica a continuación.
ms.assetid: 3da1c3d2-5116-47c3-98e4-f29b33693c69
title: Envío de mensajes a GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2f7b5b0d8fbecafad0bcc36c84cf395813f767
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667113"
---
# <a name="sending-messages-to-the-gina"></a><span data-ttu-id="b3709-104">Envío de mensajes a GINA</span><span class="sxs-lookup"><span data-stu-id="b3709-104">Sending Messages to the GINA</span></span>

<span data-ttu-id="b3709-105">[*Winlogon*](../secgloss/w-gly.md) envía mensajes a [*Gina*](../secgloss/g-gly.md) mientras se muestran los cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b3709-105">[*Winlogon*](../secgloss/w-gly.md) sends messages to the [*GINA*](../secgloss/g-gly.md) while dialog boxes are displayed.</span></span> <span data-ttu-id="b3709-106">Estos mensajes se encapsulan en el \_ mensaje SAS de WLX WM \_ como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="b3709-106">These messages are all encapsulated in the WLX\_WM\_SAS message as follows.</span></span>



| <span data-ttu-id="b3709-107">Tipo de secuencia de atención segura en el parámetro wParam</span><span class="sxs-lookup"><span data-stu-id="b3709-107">Secure attention sequence type in wParam parameter</span></span> | <span data-ttu-id="b3709-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3709-108">Description</span></span>                                                                                                                                   |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3709-109">WLX \_ tipo de SAS \_ \_ Ctrl \_ ALT \_ Supr</span><span class="sxs-lookup"><span data-stu-id="b3709-109">WLX\_SAS\_TYPE\_CTRL\_ALT\_DEL</span></span>                     | <span data-ttu-id="b3709-110">Indica que se ha recibido una secuencia de teclas CTRL + ALT + SUPR.</span><span class="sxs-lookup"><span data-stu-id="b3709-110">Indicates that a CTRL+ALT+DEL key sequence was received.</span></span>                                                                                      |
| <span data-ttu-id="b3709-111">WLX \_ SAS \_ Type \_ SC \_ Insert</span><span class="sxs-lookup"><span data-stu-id="b3709-111">WLX\_SAS\_TYPE\_SC\_INSERT</span></span>                         | <span data-ttu-id="b3709-112">Indica que se ha insertado una [*tarjeta inteligente*](../secgloss/s-gly.md) en un dispositivo compatible.</span><span class="sxs-lookup"><span data-stu-id="b3709-112">Indicates that a [*smart card*](../secgloss/s-gly.md) has been inserted into a compatible device.</span></span> |
| <span data-ttu-id="b3709-113">WLX \_ SAS \_ tipo \_ SC \_ Remove</span><span class="sxs-lookup"><span data-stu-id="b3709-113">WLX\_SAS\_TYPE\_SC\_REMOVE</span></span>                         | <span data-ttu-id="b3709-114">Indica que se ha quitado una tarjeta inteligente de un dispositivo compatible.</span><span class="sxs-lookup"><span data-stu-id="b3709-114">Indicates that a smart card has been removed from a compatible device.</span></span>                                                                        |
| <span data-ttu-id="b3709-115">\_cierre de \_ \_ sesión de usuario de tipo SAS de WLX \_</span><span class="sxs-lookup"><span data-stu-id="b3709-115">WLX\_SAS\_TYPE\_USER\_LOGOFF</span></span>                       | <span data-ttu-id="b3709-116">Indica que un usuario solicitó el cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="b3709-116">Indicates that a user requested logoff.</span></span>                                                                                                       |
| <span data-ttu-id="b3709-117">WLX \_ tipo de SAS \_ \_ SCRNSVR \_ tiempo de espera</span><span class="sxs-lookup"><span data-stu-id="b3709-117">WLX\_SAS\_TYPE\_SCRNSVR\_TIMEOUT</span></span>                   | <span data-ttu-id="b3709-118">Indica que se debe ejecutar el protector de pantalla debido a la falta de intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="b3709-118">Indicates that the screen saver should be run due to lack of user input.</span></span>                                                                      |
| <span data-ttu-id="b3709-119">WLX \_ \_ tiempo de espera de tipo SAS \_</span><span class="sxs-lookup"><span data-stu-id="b3709-119">WLX\_SAS\_TYPE\_TIMEOUT</span></span>                            | <span data-ttu-id="b3709-120">Indica que no se ha recibido ninguna entrada de usuario dentro del período de tiempo de espera especificado.</span><span class="sxs-lookup"><span data-stu-id="b3709-120">Indicates that no user input was received within the specified time-out period.</span></span>                                                               |



 

<span data-ttu-id="b3709-121">En el caso de los tiempos de espera y cierres de sesión, Winlogon cerrará el cuadro de diálogo después de enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="b3709-121">For time-outs and logoffs, Winlogon will close the dialog box after the message has been sent.</span></span> <span data-ttu-id="b3709-122">Este mensaje se envía para que la operación del cuadro de diálogo pueda responder de una manera útil (por ejemplo, al cerrarse si se ha producido un cierre de sesión).</span><span class="sxs-lookup"><span data-stu-id="b3709-122">This message is sent so the dialog box operation can respond in a useful manner (for example, by closing itself down if a logoff has occurred).</span></span>

<span data-ttu-id="b3709-123">En el caso de los tiempos de espera de entrada, el cuadro de diálogo se cierra con el tiempo de espera de entrada de Code WLX \_ Dlg \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b3709-123">For input time-outs, the dialog box is closed with the code WLX\_DLG\_INPUT\_TIMEOUT.</span></span>

<span data-ttu-id="b3709-124">En el caso de los tiempos de espera del protector de pantalla, el cuadro de diálogo se cierra con el tiempo de espera del protector de pantalla Code WLX \_ Dlg \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b3709-124">For screen saver time-outs, the dialog box is closed with the code WLX\_DLG\_SCREEN\_SAVER\_TIMEOUT.</span></span>

<span data-ttu-id="b3709-125">Para los cierres de sesión, la operación del cuadro de diálogo se cierra con el código WLX \_ Dlg \_ cierre de sesión del usuario \_ .</span><span class="sxs-lookup"><span data-stu-id="b3709-125">For logoffs, the dialog box operation is closed with the code WLX\_DLG\_USER\_LOGOFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3709-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b3709-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3709-127">Inicializando Winlogon</span><span class="sxs-lookup"><span data-stu-id="b3709-127">Initializing Winlogon</span></span>](initializing-winlogon.md)
</dt> <dt>

[<span data-ttu-id="b3709-128">Estados de Winlogon</span><span class="sxs-lookup"><span data-stu-id="b3709-128">Winlogon States</span></span>](winlogon-states.md)
</dt> <dt>

[<span data-ttu-id="b3709-129">Cuadro de diálogo compatible Tiempo de servicio operaciones de salida</span><span class="sxs-lookup"><span data-stu-id="b3709-129">Supported Dialog Box Service Time-out Operations</span></span>](supported-dialog-box-service-time-out-operations.md)
</dt> <dt>

[<span data-ttu-id="b3709-130">Funciones de compatibilidad con Winlogon</span><span class="sxs-lookup"><span data-stu-id="b3709-130">Winlogon Support Functions</span></span>](authentication-functions.md)
</dt> </dl>

 

 

---
title: Cómo procesar notificaciones de selector de fecha y hora
description: En esta sección se muestra cómo procesar las notificaciones del selector de fecha y hora.
ms.assetid: DBF624F0-89E0-435B-BE96-60B7A4CEDA61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa1214ebd671b4ae222990bde4b44586e6d7b11
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424185"
---
# <a name="how-to-process-date-and-time-picker-notifications"></a><span data-ttu-id="bc6d2-103">Cómo procesar notificaciones de selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="bc6d2-103">How to Process Date and Time Picker Notifications</span></span>

<span data-ttu-id="bc6d2-104">En esta sección se muestra cómo procesar las notificaciones del selector de fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="bc6d2-104">This section demonstrates how to process date and time picker notifications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="bc6d2-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="bc6d2-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="bc6d2-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="bc6d2-106">Technologies</span></span>

-   [<span data-ttu-id="bc6d2-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="bc6d2-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="bc6d2-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bc6d2-108">Prerequisites</span></span>

-   <span data-ttu-id="bc6d2-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="bc6d2-109">C/C++</span></span>
-   <span data-ttu-id="bc6d2-110">Programación Interfaz de usuario Windows</span><span class="sxs-lookup"><span data-stu-id="bc6d2-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="bc6d2-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="bc6d2-111">Instructions</span></span>


<span data-ttu-id="bc6d2-112">Un control selector de fecha y hora (DTP) envía mensajes de notificación a la ventana primaria cuando se producen eventos, normalmente desencadenados por la entrada del usuario, en el control .</span><span class="sxs-lookup"><span data-stu-id="bc6d2-112">A date and time picker (DTP) control sends notification messages to the parent window when events, usually triggered by input from the user, occur in the control.</span></span> <span data-ttu-id="bc6d2-113">La aplicación debe incluir código para determinar el tipo de mensaje de notificación y responder correctamente.</span><span class="sxs-lookup"><span data-stu-id="bc6d2-113">Your application must include code to determine the type of notification message and respond appropriately.</span></span>

<span data-ttu-id="bc6d2-114">Si tiene previsto usar campos de devolución de llamada con los controles DTP de la aplicación, debe estar preparado para controlar los códigos de [notificación \_ DTN FORMATQUERY,](dtn-formatquery.md) [DTN \_ FORMAT](dtn-format.md)y [ \_ DTN WMKEYDOWN.](dtn-wmkeydown.md)</span><span class="sxs-lookup"><span data-stu-id="bc6d2-114">If you plan to use callback fields with the DTP controls in your application, you must be prepared to handle [DTN\_FORMATQUERY](dtn-formatquery.md), [DTN\_FORMAT](dtn-format.md), and [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification codes.</span></span> <span data-ttu-id="bc6d2-115">Para obtener información adicional sobre los campos de devolución de llamada, vea [Campos de devolución de llamada](date-and-time-picker-controls.md).</span><span class="sxs-lookup"><span data-stu-id="bc6d2-115">For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).</span></span>

<span data-ttu-id="bc6d2-116">El siguiente ejemplo de código de C++ identifica el mensaje de notificación enviado por un control DTP y llama a la función adecuada definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bc6d2-116">The following C++ code example identifies the notification message sent by a DTP control and calls the appropriate application-defined function.</span></span> <span data-ttu-id="bc6d2-117">Consulte los temas siguientes para obtener ejemplos de código que ilustran cómo procesar las notificaciones que aparecen en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="bc6d2-117">Refer to the following topics for code examples that illustrate how to process the notifications that appear in this example.</span></span>

|   <span data-ttu-id="bc6d2-118">Temas</span><span class="sxs-lookup"><span data-stu-id="bc6d2-118">Topics</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc6d2-119">Cómo procesar la notificación \_ DATETIMECHANGE de DTN</span><span class="sxs-lookup"><span data-stu-id="bc6d2-119">How to Process the DTN\_DATETIMECHANGE Notification</span></span>](process-the-dtn-datetimechange-notification.md) |
| [<span data-ttu-id="bc6d2-120">Cómo procesar la notificación FORMATQUERY de DTN \_</span><span class="sxs-lookup"><span data-stu-id="bc6d2-120">How to Process the DTN\_FORMATQUERY Notification</span></span>](process-the-dtn-formatquery-notification.md)       |
| [<span data-ttu-id="bc6d2-121">Cómo procesar la notificación DTN \_ FORMAT</span><span class="sxs-lookup"><span data-stu-id="bc6d2-121">How to Process the DTN\_FORMAT Notification</span></span>](process-the-dtn-format-notfication.md)                  |
| [<span data-ttu-id="bc6d2-122">Cómo procesar la notificación \_ WMKEYDOWN de DTN</span><span class="sxs-lookup"><span data-stu-id="bc6d2-122">How to Process the DTN\_WMKEYDOWN Notification</span></span>](process-the-dtn-wmkeydown-notification.md)           |



 



```C++
BOOL WINAPI DoNotify(HWND hwnd, WPARAM wParam, LPARAM lParam)
{
    LPNMHDR hdr = (LPNMHDR)lParam;

    switch(hdr->code){

        case DTN_DATETIMECHANGE:{
            LPNMDATETIMECHANGE lpChange = (LPNMDATETIMECHANGE)lParam;
            DoDateTimeChange(lpChange);
        }
        break;

        case DTN_FORMATQUERY:{
            LPNMDATETIMEFORMATQUERY lpDTFQuery = (LPNMDATETIMEFORMATQUERY)lParam;

            // Process DTN_FORMATQUERY to ensure that the control
            // displays callback information properly.
            DoFormatQuery(hdr->hwndFrom, lpDTFQuery);
        }
        break;

        case DTN_FORMAT:{
            LPNMDATETIMEFORMAT lpNMFormat = (LPNMDATETIMEFORMAT) lParam;

            // Process DTN_FORMAT to supply information about callback
            // fields (fields) in the DTP control.
            DoFormat(hdr->hwndFrom, lpNMFormat);
        }
        break;

        case DTN_WMKEYDOWN:{
            LPNMDATETIMEWMKEYDOWN lpDTKeystroke = 
                            (LPNMDATETIMEWMKEYDOWN)lParam;

            // Process DTN_WMKEYDOWN to respond to a user's keystroke in
            // a callback field.
            DoWMKeydown(hdr->hwndFrom, lpDTKeystroke);
        }
        break;
    }

    // All of the above notifications require the owner to return zero.
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="bc6d2-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bc6d2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc6d2-124">Notificaciones del selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="bc6d2-124">Date and Time Picker Notifications</span></span>](bumper-date-and-time-picker-control-reference-notifications.md)
</dt> <dt>

[<span data-ttu-id="bc6d2-125">Referencia del control selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="bc6d2-125">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="bc6d2-126">Usar controles selectores de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="bc6d2-126">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="bc6d2-127">Selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="bc6d2-127">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 





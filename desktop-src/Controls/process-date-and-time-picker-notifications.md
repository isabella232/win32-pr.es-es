---
title: Cómo procesar notificaciones de selector de fecha y hora
description: En esta sección se muestra cómo procesar las notificaciones de selector de fecha y hora.
ms.assetid: DBF624F0-89E0-435B-BE96-60B7A4CEDA61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b904c464677a81151b03e3ae89085847e4e8bdf
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104078635"
---
# <a name="how-to-process-date-and-time-picker-notifications"></a><span data-ttu-id="00476-103">Cómo procesar notificaciones de selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="00476-103">How to Process Date and Time Picker Notifications</span></span>

<span data-ttu-id="00476-104">En esta sección se muestra cómo procesar las notificaciones de selector de fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="00476-104">This section demonstrates how to process date and time picker notifications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="00476-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="00476-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="00476-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="00476-106">Technologies</span></span>

-   [<span data-ttu-id="00476-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="00476-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="00476-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="00476-108">Prerequisites</span></span>

-   <span data-ttu-id="00476-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="00476-109">C/C++</span></span>
-   <span data-ttu-id="00476-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="00476-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="00476-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="00476-111">Instructions</span></span>


<span data-ttu-id="00476-112">Un control de selector de fecha y hora (DTP) envía mensajes de notificación a la ventana primaria cuando los eventos, normalmente desencadenados por la entrada del usuario, se producen en el control.</span><span class="sxs-lookup"><span data-stu-id="00476-112">A date and time picker (DTP) control sends notification messages to the parent window when events, usually triggered by input from the user, occur in the control.</span></span> <span data-ttu-id="00476-113">La aplicación debe incluir código para determinar el tipo de mensaje de notificación y responder de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="00476-113">Your application must include code to determine the type of notification message and respond appropriately.</span></span>

<span data-ttu-id="00476-114">Si planea usar campos de devolución de llamada con los controles de DTP en la aplicación, debe estar preparado para controlar los códigos de notificación [DTN \_ FORMATQUERY](dtn-formatquery.md), [DTN \_ ](dtn-format.md)y [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) .</span><span class="sxs-lookup"><span data-stu-id="00476-114">If you plan to use callback fields with the DTP controls in your application, you must be prepared to handle [DTN\_FORMATQUERY](dtn-formatquery.md), [DTN\_FORMAT](dtn-format.md), and [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification codes.</span></span> <span data-ttu-id="00476-115">Para obtener más información sobre los campos de devolución de llamada, vea [campos de devolución de llamada](date-and-time-picker-controls.md).</span><span class="sxs-lookup"><span data-stu-id="00476-115">For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).</span></span>

<span data-ttu-id="00476-116">En el siguiente ejemplo de código de C++ se identifica el mensaje de notificación enviado por un control de DTP y se llama a la función definida por la aplicación adecuada.</span><span class="sxs-lookup"><span data-stu-id="00476-116">The following C++ code example identifies the notification message sent by a DTP control and calls the appropriate application-defined function.</span></span> <span data-ttu-id="00476-117">Consulte los siguientes temas para obtener ejemplos de código que muestran cómo procesar las notificaciones que aparecen en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="00476-117">Refer to the following topics for code examples that illustrate how to process the notifications that appear in this example.</span></span>

|                                                                                                        |
|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00476-118">Cómo procesar la notificación de \_ DATETIMECHANGE de DTN</span><span class="sxs-lookup"><span data-stu-id="00476-118">How to Process the DTN\_DATETIMECHANGE Notification</span></span>](process-the-dtn-datetimechange-notification.md) |
| [<span data-ttu-id="00476-119">Cómo procesar la notificación de DTN \_ FORMATQUERY</span><span class="sxs-lookup"><span data-stu-id="00476-119">How to Process the DTN\_FORMATQUERY Notification</span></span>](process-the-dtn-formatquery-notification.md)       |
| [<span data-ttu-id="00476-120">Cómo procesar la notificación de \_ formato DTN</span><span class="sxs-lookup"><span data-stu-id="00476-120">How to Process the DTN\_FORMAT Notification</span></span>](process-the-dtn-format-notfication.md)                  |
| [<span data-ttu-id="00476-121">Cómo procesar la notificación de \_ WMKEYDOWN de DTN</span><span class="sxs-lookup"><span data-stu-id="00476-121">How to Process the DTN\_WMKEYDOWN Notification</span></span>](process-the-dtn-wmkeydown-notification.md)           |



 



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



## <a name="related-topics"></a><span data-ttu-id="00476-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="00476-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00476-123">Notificaciones de selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="00476-123">Date and Time Picker Notifications</span></span>](bumper-date-and-time-picker-control-reference-notifications.md)
</dt> <dt>

[<span data-ttu-id="00476-124">Referencia de control de selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="00476-124">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="00476-125">Usar controles de selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="00476-125">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="00476-126">Selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="00476-126">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 





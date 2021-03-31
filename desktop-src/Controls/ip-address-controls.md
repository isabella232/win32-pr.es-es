---
title: Acerca de los controles de dirección IP
description: Un control de dirección de protocolo de Internet (IP) permite al usuario escribir una dirección IP en un formato fácil de entender.
ms.assetid: cf6a59fc-661c-420a-a67f-a42619946357
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb8cf39400c97d211d83b5496067fe6d4772e1e7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995660"
---
# <a name="about-ip-address-controls"></a><span data-ttu-id="0c9fe-103">Acerca de los controles de dirección IP</span><span class="sxs-lookup"><span data-stu-id="0c9fe-103">About IP Address Controls</span></span>

<span data-ttu-id="0c9fe-104">Un control de dirección de protocolo de Internet (IP) permite al usuario escribir una dirección IP en un formato fácil de entender.</span><span class="sxs-lookup"><span data-stu-id="0c9fe-104">An Internet Protocol (IP) address control allows the user to enter an IP address in an easily understood format.</span></span> <span data-ttu-id="0c9fe-105">Este control también permite a la aplicación obtener la dirección en formato numérico en lugar de en formato de texto.</span><span class="sxs-lookup"><span data-stu-id="0c9fe-105">This control also allows the application to obtain the address in numeric form rather than in text form.</span></span>

-   [<span data-ttu-id="0c9fe-106">Acerca de los controles de dirección IP</span><span class="sxs-lookup"><span data-stu-id="0c9fe-106">About IP Address Controls</span></span>](#about-ip-address-controls)
-   [<span data-ttu-id="0c9fe-107">Crear un control de dirección IP</span><span class="sxs-lookup"><span data-stu-id="0c9fe-107">Creating an IP Address Control</span></span>](#creating-an-ip-address-control)
-   [<span data-ttu-id="0c9fe-108">¿Controla una dirección IP un control de edición?</span><span class="sxs-lookup"><span data-stu-id="0c9fe-108">Is an IP Address Control an Edit Control?</span></span>](#is-an-ip-address-control-an-edit-control)

## <a name="about-ip-address-controls"></a><span data-ttu-id="0c9fe-109">Acerca de los controles de dirección IP</span><span class="sxs-lookup"><span data-stu-id="0c9fe-109">About IP Address Controls</span></span>

<span data-ttu-id="0c9fe-110">Windows Internet Explorer versión 4,0 introduce el control de dirección IP, un nuevo control similar a un control de edición que permite al usuario escribir una dirección numérica en formato de protocolo de Internet (IP).</span><span class="sxs-lookup"><span data-stu-id="0c9fe-110">Windows Internet Explorer Version 4.0 introduces the IP address control, a new control similar to an edit control that allows the user to enter a numeric address in Internet protocol (IP) format.</span></span> <span data-ttu-id="0c9fe-111">Este formato consta de campos de 4 3 dígitos.</span><span class="sxs-lookup"><span data-stu-id="0c9fe-111">This format consists of four three-digit fields.</span></span> <span data-ttu-id="0c9fe-112">Cada campo se trata individualmente; los números de campo son de base cero y continúan de izquierda a derecha, como se muestra en esta ilustración.</span><span class="sxs-lookup"><span data-stu-id="0c9fe-112">Each field is treated individually; the field numbers are zero-based and proceed from left to right as shown in this figure.</span></span>

![diagrama que muestra los valores de cada uno de los cuatro campos de un control de dirección IP](images/ipa-scrn.png)

<span data-ttu-id="0c9fe-114">El control solo permite escribir texto numérico en cada uno de los campos.</span><span class="sxs-lookup"><span data-stu-id="0c9fe-114">The control allows only numeric text to be entered in each of the fields.</span></span> <span data-ttu-id="0c9fe-115">Una vez especificados tres dígitos en un campo determinado, el foco de teclado se mueve automáticamente al siguiente campo.</span><span class="sxs-lookup"><span data-stu-id="0c9fe-115">Once three digits have been entered in a given field, keyboard focus is automatically moved to the next field.</span></span> <span data-ttu-id="0c9fe-116">Si la aplicación no necesita llenar todo el campo, el usuario puede escribir menos de tres dígitos.</span><span class="sxs-lookup"><span data-stu-id="0c9fe-116">If filling the entire field is not required by the application, the user can enter fewer than three digits.</span></span> <span data-ttu-id="0c9fe-117">Por ejemplo, si el campo solo debe contener el número veinte, escribir "21" y presionar la tecla llevará al usuario al siguiente campo.</span><span class="sxs-lookup"><span data-stu-id="0c9fe-117">For example, if the field should only contain the number twenty-one, typing "21" and pressing the key will take the user to the next field.</span></span>

<span data-ttu-id="0c9fe-118">El intervalo predeterminado para cada campo es de 0 a 255, pero la aplicación puede establecer el intervalo en cualquier valor entre esos límites con el mensaje [**IPM \_ SetRange**](ipm-setrange.md) .</span><span class="sxs-lookup"><span data-stu-id="0c9fe-118">The default range for each field is 0 to 255, but the application can set the range to any values between those limits with the [**IPM\_SETRANGE**](ipm-setrange.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="0c9fe-119">El control de direcciones IP se implementa en la versión 4,71 y versiones posteriores de Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="0c9fe-119">The IP address control is implemented in version 4.71 and later of Comctl32.dll.</span></span>

 

## <a name="creating-an-ip-address-control"></a><span data-ttu-id="0c9fe-120">Crear un control de dirección IP</span><span class="sxs-lookup"><span data-stu-id="0c9fe-120">Creating an IP Address Control</span></span>

<span data-ttu-id="0c9fe-121">Antes de crear un control de dirección IP, llame a [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) con la marca de **clases de \_ Internet \_ de ICC** establecida en el miembro **dwICC** de la estructura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) .</span><span class="sxs-lookup"><span data-stu-id="0c9fe-121">Before creating an IP address control, call [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) with the **ICC\_INTERNET\_CLASSES** flag set in the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

<span data-ttu-id="0c9fe-122">Utilice la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear un control de dirección IP.</span><span class="sxs-lookup"><span data-stu-id="0c9fe-122">Use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create an IP address control.</span></span> <span data-ttu-id="0c9fe-123">El nombre de clase del control es [**WC \_ IPAddress**](common-control-window-classes.md), que se define en commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="0c9fe-123">The class name for the control is [**WC\_IPADDRESS**](common-control-window-classes.md), which is defined in Commctrl.h.</span></span> <span data-ttu-id="0c9fe-124">No existe ningún estilo específico del control de direcciones IP; sin embargo, dado que se trata de un control secundario, use el estilo de [**WS \_ Child**](/windows/desktop/winmsg/window-styles) como mínimo.</span><span class="sxs-lookup"><span data-stu-id="0c9fe-124">No IP address control-specific styles exist; however, because this is a child control, use the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) style as a minimum.</span></span>

## <a name="is-an-ip-address-control-an-edit-control"></a><span data-ttu-id="0c9fe-125">¿Controla una dirección IP un control de edición?</span><span class="sxs-lookup"><span data-stu-id="0c9fe-125">Is an IP Address Control an Edit Control?</span></span>

<span data-ttu-id="0c9fe-126">Un control de dirección IP no es un control de edición y no responde a \_ los mensajes em.</span><span class="sxs-lookup"><span data-stu-id="0c9fe-126">An IP address control is not an edit control and it will not respond to EM\_ messages.</span></span> <span data-ttu-id="0c9fe-127">Sin embargo, enviará a la ventana propietaria las siguientes notificaciones de control de edición a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="0c9fe-127">It will, however, send the owner window the following edit control notifications through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="0c9fe-128">Tenga en cuenta que el control de direcciones IP también enviará notificaciones de IPN privadas \_ a través del mensaje de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0c9fe-128">Note that the IP address control will also send private IPN\_ notifications through the [**WM\_NOTIFY**](wm-notify.md) message.</span></span>



|                                   |                                                                                                                                                                                                         |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c9fe-129">**Notificación**</span><span class="sxs-lookup"><span data-stu-id="0c9fe-129">**Notification**</span></span>                  | <span data-ttu-id="0c9fe-130">**Motivo de la notificación**</span><span class="sxs-lookup"><span data-stu-id="0c9fe-130">**Reason for notification**</span></span>                                                                                                                                                                             |
| [<span data-ttu-id="0c9fe-131">EN \_ SETFOCUS</span><span class="sxs-lookup"><span data-stu-id="0c9fe-131">EN\_SETFOCUS</span></span>](en-setfocus.md)   | <span data-ttu-id="0c9fe-132">Se envía cuando el control de dirección IP obtiene el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="0c9fe-132">Sent when the IP address control gains the keyboard focus.</span></span>                                                                                                                                              |
| [<span data-ttu-id="0c9fe-133">EN \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="0c9fe-133">EN\_KILLFOCUS</span></span>](en-killfocus.md) | <span data-ttu-id="0c9fe-134">Se envía cuando el control de dirección IP pierde el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="0c9fe-134">Sent when the IP address control loses the keyboard focus.</span></span>                                                                                                                                              |
| [<span data-ttu-id="0c9fe-135">EN \_ cambio</span><span class="sxs-lookup"><span data-stu-id="0c9fe-135">EN\_CHANGE</span></span>](en-change.md)       | <span data-ttu-id="0c9fe-136">Se envía cuando cambia cualquier campo del control de dirección IP.</span><span class="sxs-lookup"><span data-stu-id="0c9fe-136">Sent when any field in the IP address control changes.</span></span> <span data-ttu-id="0c9fe-137">Al igual que la notificación de [ \_ cambio de en](en-change.md) un control estándar de edición, esta notificación se recibe una vez actualizada la pantalla.</span><span class="sxs-lookup"><span data-stu-id="0c9fe-137">Like the [EN\_CHANGE](en-change.md) notification from a standard edit control, this notification is received after the screen has been updated.</span></span> |



 

 

 
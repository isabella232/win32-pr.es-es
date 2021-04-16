---
title: IP Address Control
description: Esta sección contiene información sobre los elementos de programación utilizados con controles de direcciones IP.
ms.assetid: vs|controls|~\controls\ipaddress\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c80fc87a12ce49038f4c1836e684fa0f8895bd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486698"
---
# <a name="ip-address-control"></a><span data-ttu-id="48e47-103">IP Address Control</span><span class="sxs-lookup"><span data-stu-id="48e47-103">IP Address Control</span></span>

<span data-ttu-id="48e47-104">Esta sección contiene información sobre los elementos de programación utilizados con controles de direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="48e47-104">This section contains information about the programming elements used with IP address controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="48e47-105">Temas de introducción</span><span class="sxs-lookup"><span data-stu-id="48e47-105">Overviews</span></span>



| <span data-ttu-id="48e47-106">Tema</span><span class="sxs-lookup"><span data-stu-id="48e47-106">Topic</span></span>                                          | <span data-ttu-id="48e47-107">Contenido</span><span class="sxs-lookup"><span data-stu-id="48e47-107">Contents</span></span>                                                                                                                    |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48e47-108">Controles de direcciones IP</span><span class="sxs-lookup"><span data-stu-id="48e47-108">IP Address Controls</span></span>](ip-address-controls.md) | <span data-ttu-id="48e47-109">Un control de dirección de protocolo de Internet (IP) permite al usuario escribir una dirección IP en un formato fácil de entender.</span><span class="sxs-lookup"><span data-stu-id="48e47-109">An Internet Protocol (IP) address control allows the user to enter an IP address in an easily understood format.</span></span><br/> |



 

### <a name="macros"></a><span data-ttu-id="48e47-110">Macros</span><span class="sxs-lookup"><span data-stu-id="48e47-110">Macros</span></span>



| <span data-ttu-id="48e47-111">Tema</span><span class="sxs-lookup"><span data-stu-id="48e47-111">Topic</span></span>                                         | <span data-ttu-id="48e47-112">Contenido</span><span class="sxs-lookup"><span data-stu-id="48e47-112">Contents</span></span>                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48e47-113">**PRIMERA \_ dirección IP**</span><span class="sxs-lookup"><span data-stu-id="48e47-113">**FIRST\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress)   | <span data-ttu-id="48e47-114">Extrae el valor de campo 0 de una dirección IP empaquetada recuperada con el mensaje de [**\_ GETADDRESS IPM**](ipm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="48e47-114">Extracts the field 0 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |
| [<span data-ttu-id="48e47-115">**CUARTO \_ direcciónIP**</span><span class="sxs-lookup"><span data-stu-id="48e47-115">**FOURTH\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) | <span data-ttu-id="48e47-116">Extrae el valor del campo 3 de una dirección IP empaquetada recuperada con el mensaje de [**\_ GETADDRESS de IPM**](ipm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="48e47-116">Extracts the field 3 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |
| [<span data-ttu-id="48e47-117">**MAKEIPADDRESS**</span><span class="sxs-lookup"><span data-stu-id="48e47-117">**MAKEIPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress)        | <span data-ttu-id="48e47-118">Empaqueta cuatro valores de byte en un solo LPARAM adecuado para su uso con el mensaje [**\_ SETADDRESS de IPM**](ipm-setaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="48e47-118">Packs four byte-values into a single LPARAM suitable for use with the [**IPM\_SETADDRESS**](ipm-setaddress.md) message.</span></span> <br/>  |
| [<span data-ttu-id="48e47-119">**MAKEIPRANGE**</span><span class="sxs-lookup"><span data-stu-id="48e47-119">**MAKEIPRANGE**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange)            | <span data-ttu-id="48e47-120">Empaqueta dos valores de byte en un solo LPARAM adecuado para su uso con el mensaje de [**\_ intrange IPM**](ipm-setrange.md) .</span><span class="sxs-lookup"><span data-stu-id="48e47-120">Packs two byte-values into a single LPARAM suitable for use with the [**IPM\_SETRANGE**](ipm-setrange.md) message.</span></span> <br/>       |
| [<span data-ttu-id="48e47-121">**SEGUNDA \_ dirección IP**</span><span class="sxs-lookup"><span data-stu-id="48e47-121">**SECOND\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress) | <span data-ttu-id="48e47-122">Extrae el valor del campo 1 de una dirección IP empaquetada recuperada con el mensaje [**\_ GETADDRESS de IPM**](ipm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="48e47-122">Extracts the field 1 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |
| [<span data-ttu-id="48e47-123">**TERCERA \_ dirección IP**</span><span class="sxs-lookup"><span data-stu-id="48e47-123">**THIRD\_IPADDRESS**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)   | <span data-ttu-id="48e47-124">Extrae el valor del campo 2 de una dirección IP empaquetada recuperada con el mensaje de [**\_ GETADDRESS de IPM**](ipm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="48e47-124">Extracts the field 2 value from a packed IP address retrieved with the [**IPM\_GETADDRESS**](ipm-getaddress.md) message.</span></span> <br/> |



 

### <a name="messages"></a><span data-ttu-id="48e47-125">error de Hadoop</span><span class="sxs-lookup"><span data-stu-id="48e47-125">Messages</span></span>



| <span data-ttu-id="48e47-126">Tema</span><span class="sxs-lookup"><span data-stu-id="48e47-126">Topic</span></span>                                         | <span data-ttu-id="48e47-127">Contenido</span><span class="sxs-lookup"><span data-stu-id="48e47-127">Contents</span></span>                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48e47-128">**IPM \_ CLEARADDRESS**</span><span class="sxs-lookup"><span data-stu-id="48e47-128">**IPM\_CLEARADDRESS**</span></span>](ipm-clearaddress.md) | <span data-ttu-id="48e47-129">Borra el contenido del control de dirección IP.</span><span class="sxs-lookup"><span data-stu-id="48e47-129">Clears the contents of the IP address control.</span></span> <br/>                                                                            |
| [<span data-ttu-id="48e47-130">**IPM \_ GETADDRESS**</span><span class="sxs-lookup"><span data-stu-id="48e47-130">**IPM\_GETADDRESS**</span></span>](ipm-getaddress.md)     | <span data-ttu-id="48e47-131">Obtiene los valores de dirección de los cuatro campos del control de dirección IP.</span><span class="sxs-lookup"><span data-stu-id="48e47-131">Gets the address values for all four fields in the IP address control.</span></span> <br/>                                                    |
| [<span data-ttu-id="48e47-132">**IPM \_ esblanco**</span><span class="sxs-lookup"><span data-stu-id="48e47-132">**IPM\_ISBLANK**</span></span>](ipm-isblank.md)           | <span data-ttu-id="48e47-133">Determina si todos los campos del control de dirección IP están en blanco.</span><span class="sxs-lookup"><span data-stu-id="48e47-133">Determines if all fields in the IP address control are blank.</span></span> <br/>                                                             |
| [<span data-ttu-id="48e47-134">**IPM \_ SETADDRESS**</span><span class="sxs-lookup"><span data-stu-id="48e47-134">**IPM\_SETADDRESS**</span></span>](ipm-setaddress.md)     | <span data-ttu-id="48e47-135">Establece los valores de dirección de los cuatro campos en el control de dirección IP.</span><span class="sxs-lookup"><span data-stu-id="48e47-135">Sets the address values for all four fields in the IP address control.</span></span> <br/>                                                    |
| [<span data-ttu-id="48e47-136">**SETFOCUS de la IPM \_**</span><span class="sxs-lookup"><span data-stu-id="48e47-136">**IPM\_SETFOCUS**</span></span>](ipm-setfocus.md)         | <span data-ttu-id="48e47-137">Establece el foco de teclado en el campo especificado en el control de dirección IP.</span><span class="sxs-lookup"><span data-stu-id="48e47-137">Sets the keyboard focus to the specified field in the IP address control.</span></span> <span data-ttu-id="48e47-138">Se seleccionará todo el texto de ese campo.</span><span class="sxs-lookup"><span data-stu-id="48e47-138">All of the text in that field will be selected.</span></span> <br/> |
| [<span data-ttu-id="48e47-139">**IPM \_ SetRange**</span><span class="sxs-lookup"><span data-stu-id="48e47-139">**IPM\_SETRANGE**</span></span>](ipm-setrange.md)         | <span data-ttu-id="48e47-140">Establece el intervalo válido para el campo especificado en el control de dirección IP.</span><span class="sxs-lookup"><span data-stu-id="48e47-140">Sets the valid range for the specified field in the IP address control.</span></span> <br/>                                                   |



 

### <a name="notifications"></a><span data-ttu-id="48e47-141">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="48e47-141">Notifications</span></span>



| <span data-ttu-id="48e47-142">Tema</span><span class="sxs-lookup"><span data-stu-id="48e47-142">Topic</span></span>                                     | <span data-ttu-id="48e47-143">Contenido</span><span class="sxs-lookup"><span data-stu-id="48e47-143">Contents</span></span>                                                                                                                                                                                   |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48e47-144">IPN \_ FIELDCHANGED</span><span class="sxs-lookup"><span data-stu-id="48e47-144">IPN\_FIELDCHANGED</span></span>](ipn-fieldchanged.md) | <span data-ttu-id="48e47-145">Se envía cuando el usuario cambia un campo en el control o se mueve de un campo a otro.</span><span class="sxs-lookup"><span data-stu-id="48e47-145">Sent when the user changes a field in the control or moves from one field to another.</span></span> <span data-ttu-id="48e47-146">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="48e47-146">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/> |



 

### <a name="structures"></a><span data-ttu-id="48e47-147">Estructuras</span><span class="sxs-lookup"><span data-stu-id="48e47-147">Structures</span></span>



| <span data-ttu-id="48e47-148">Tema</span><span class="sxs-lookup"><span data-stu-id="48e47-148">Topic</span></span>                              | <span data-ttu-id="48e47-149">Contenido</span><span class="sxs-lookup"><span data-stu-id="48e47-149">Contents</span></span>                                                                                              |
|------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48e47-150">**NMIPADDRESS**</span><span class="sxs-lookup"><span data-stu-id="48e47-150">**NMIPADDRESS**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) | <span data-ttu-id="48e47-151">Contiene información del código de notificación [ \_ FIELDCHANGED de IPN](ipn-fieldchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="48e47-151">Contains information for the [IPN\_FIELDCHANGED](ipn-fieldchanged.md) notification code.</span></span> <br/> |



 

 

 






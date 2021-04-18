---
description: El gráfico está abriendo un archivo o ha terminado de abrir un archivo.
ms.assetid: 352867e1-025f-4adb-be32-f7941c0ec8cf
title: EC_OPENING_FILE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf275a2f9b64f9a30c8049b5207622270edc5098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680989"
---
# <a name="ec_opening_file"></a><span data-ttu-id="a4a0d-103">\_archivo de apertura de EC \_</span><span class="sxs-lookup"><span data-stu-id="a4a0d-103">EC\_OPENING\_FILE</span></span>

<span data-ttu-id="a4a0d-104">El gráfico está abriendo un archivo o ha terminado de abrir un archivo.</span><span class="sxs-lookup"><span data-stu-id="a4a0d-104">The graph is opening a file, or has finished opening a file.</span></span>

## <a name="parameters"></a><span data-ttu-id="a4a0d-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a4a0d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4a0d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="a4a0d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a4a0d-107">**True** si el gráfico se está iniciando para abrir un archivo, o **false** si el gráfico ya no abre el archivo.</span><span class="sxs-lookup"><span data-stu-id="a4a0d-107">**TRUE** if the graph is starting to open a file, or **FALSE** if the graph is no longer opening the file.</span></span>

</dd> <dt>

<span data-ttu-id="a4a0d-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a4a0d-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a4a0d-109">Cero.</span><span class="sxs-lookup"><span data-stu-id="a4a0d-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="a4a0d-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="a4a0d-110">Default Action</span></span>

<span data-ttu-id="a4a0d-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a4a0d-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4a0d-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a4a0d-112">Remarks</span></span>

<span data-ttu-id="a4a0d-113">Un filtro puede enviar este evento si se tarda mucho tiempo en abrir un archivo.</span><span class="sxs-lookup"><span data-stu-id="a4a0d-113">A filter can send this event if it spends significant time opening a file.</span></span> <span data-ttu-id="a4a0d-114">(Por ejemplo, el archivo podría estar ubicado en una red). La aplicación puede usar este evento para ajustar su interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="a4a0d-114">(For example, the file might be located on a network.) The application can use this event to adjust its user interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4a0d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4a0d-115">Requirements</span></span>



| <span data-ttu-id="a4a0d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4a0d-116">Requirement</span></span> | <span data-ttu-id="a4a0d-117">Value</span><span class="sxs-lookup"><span data-stu-id="a4a0d-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a4a0d-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4a0d-118">Header</span></span><br/> | <dl> <span data-ttu-id="a4a0d-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4a0d-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4a0d-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4a0d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4a0d-121">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="a4a0d-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="a4a0d-122">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="a4a0d-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





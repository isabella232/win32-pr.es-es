---
description: La interfaz IWiaAppErrorHandler permite a las aplicaciones mostrar ventanas de errores (durante las transferencias de datos) desde las que el usuario puede elegir si desea continuar, cancelar o anular la transferencia.
ms.assetid: ac2597e6-2857-4694-bea7-1ea65d63b365
title: Interfaz IWiaAppErrorHandler (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6ccac7b689055bfaab926a8db46b4632606811d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720540"
---
# <a name="iwiaapperrorhandler-interface"></a><span data-ttu-id="cdeb8-103">Interfaz IWiaAppErrorHandler</span><span class="sxs-lookup"><span data-stu-id="cdeb8-103">IWiaAppErrorHandler interface</span></span>

<span data-ttu-id="cdeb8-104">La interfaz **IWiaAppErrorHandler** permite a las aplicaciones mostrar ventanas de errores (durante las transferencias de datos) desde las que el usuario puede elegir si desea continuar, cancelar o anular la transferencia.</span><span class="sxs-lookup"><span data-stu-id="cdeb8-104">The **IWiaAppErrorHandler** interface enables applications to display error windows (during data transfers) from which the user can choose whether to continue, cancel, or abort the transfer.</span></span>

## <a name="members"></a><span data-ttu-id="cdeb8-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="cdeb8-105">Members</span></span>

<span data-ttu-id="cdeb8-106">La interfaz **IWiaAppErrorHandler** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cdeb8-106">The **IWiaAppErrorHandler** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cdeb8-107">**IWiaAppErrorHandler** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cdeb8-107">**IWiaAppErrorHandler** also has these types of members:</span></span>

-   [<span data-ttu-id="cdeb8-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="cdeb8-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cdeb8-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="cdeb8-109">Methods</span></span>

<span data-ttu-id="cdeb8-110">La interfaz **IWiaAppErrorHandler** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="cdeb8-110">The **IWiaAppErrorHandler** interface has these methods.</span></span>



| <span data-ttu-id="cdeb8-111">Método</span><span class="sxs-lookup"><span data-stu-id="cdeb8-111">Method</span></span>                                                        | <span data-ttu-id="cdeb8-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="cdeb8-112">Description</span></span>                                                                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cdeb8-113">**GetWindow**</span><span class="sxs-lookup"><span data-stu-id="cdeb8-113">**GetWindow**</span></span>](-wia-iwiaapperrorhandler-getwindow.md)       | <span data-ttu-id="cdeb8-114">Obtiene un identificador para el cuadro de diálogo que muestra los mensajes de error y proporciona uno o varios botones para continuar, cancelar o anular la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cdeb8-114">Gets a handle to the dialog box that displays error messages and provides one or more buttons to continue, cancel, or abort the application.</span></span><br/> |
| [<span data-ttu-id="cdeb8-115">**ReportStatus**</span><span class="sxs-lookup"><span data-stu-id="cdeb8-115">**ReportStatus**</span></span>](-wia-iwiaapperrorhandler-reportstatus.md) | <span data-ttu-id="cdeb8-116">Controla el estado del dispositivo y los mensajes de error durante las transferencias de datos de imagen y muestra los mensajes al usuario.</span><span class="sxs-lookup"><span data-stu-id="cdeb8-116">Handles device status and error messages during image data transfers and displays the messages to the user.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="cdeb8-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cdeb8-117">Remarks</span></span>

<span data-ttu-id="cdeb8-118">El objeto de control de errores, o de devolución de llamada, que implementa esta interfaz se pasa a [**IWiaTransfer::D scargar**](-wia-iwiatransfer-download.md) y [**IWiaTransfer:: upload**](-wia-iwiatransfer-upload.md).</span><span class="sxs-lookup"><span data-stu-id="cdeb8-118">The error handling, or callback, object that implements this interface is passed into [**IWiaTransfer::Download**](-wia-iwiatransfer-download.md) and [**IWiaTransfer::Upload**](-wia-iwiatransfer-upload.md).</span></span>

<span data-ttu-id="cdeb8-119">Esta interfaz no está diseñada para controlar los errores detectados fuera de las transferencias de datos de la imagen, por ejemplo, errores al obtener o establecer las propiedades del dispositivo o las devoluciones de llamada no devueltas en un controlador.</span><span class="sxs-lookup"><span data-stu-id="cdeb8-119">This interface is not designed to handle errors encountered outside of image data transfers, for example, errors in getting or setting device properties or unreturned callbacks into a driver.</span></span>

<span data-ttu-id="cdeb8-120">Un controlador de errores de controlador debe implementar [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md), en lugar de **IWiaAppErrorHandler**.</span><span class="sxs-lookup"><span data-stu-id="cdeb8-120">A driver error handler should implement [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md), instead of **IWiaAppErrorHandler**.</span></span>

<span data-ttu-id="cdeb8-121">El objeto que implementa esta interfaz también debe implementar [**IWiaTransferCallback**](-wia-iwiatransfercallback.md).</span><span class="sxs-lookup"><span data-stu-id="cdeb8-121">The object that implements this interface should also implement [**IWiaTransferCallback**](-wia-iwiatransfercallback.md).</span></span>

<span data-ttu-id="cdeb8-122">Si desea que un controlador de errores de controlador y un controlador de errores predeterminado muestren ventanas de mensajes de error, pero no desea crear un controlador de errores completo para la aplicación, implemente esta interfaz e implemente también el método [**IWiaAppErrorHandler:: ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) para devolver el estado de WIA \_ \_ no \_ controlado.</span><span class="sxs-lookup"><span data-stu-id="cdeb8-122">If you want a driver error handler and default error handler to display error message windows, but you do not want to create a complete error handler for the application, implement this interface and also implement the [**IWiaAppErrorHandler::ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) method to return WIA\_STATUS\_NOT\_HANDLED.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdeb8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdeb8-123">Requirements</span></span>



| <span data-ttu-id="cdeb8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdeb8-124">Requirement</span></span> | <span data-ttu-id="cdeb8-125">Value</span><span class="sxs-lookup"><span data-stu-id="cdeb8-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cdeb8-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cdeb8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cdeb8-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cdeb8-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cdeb8-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cdeb8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cdeb8-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cdeb8-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cdeb8-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cdeb8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdeb8-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdeb8-131"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="cdeb8-132">IDL</span><span class="sxs-lookup"><span data-stu-id="cdeb8-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cdeb8-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cdeb8-133"><dt>Wia.idl</dt></span></span> </dl> |



 

 

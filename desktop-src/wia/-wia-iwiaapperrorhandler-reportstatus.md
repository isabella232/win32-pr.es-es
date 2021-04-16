---
description: Controla el estado del dispositivo y los mensajes de error durante las transferencias de datos de imagen y muestra los mensajes al usuario.
ms.assetid: 8d3ba598-8649-4108-aebc-94f2bcb64ad8
title: 'IWiaAppErrorHandler:: ReportStatus (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 1285b5391014919d7108f207917b0c44c03fa360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705779"
---
# <a name="iwiaapperrorhandlerreportstatus-method"></a><span data-ttu-id="9c559-103">IWiaAppErrorHandler:: ReportStatus (método)</span><span class="sxs-lookup"><span data-stu-id="9c559-103">IWiaAppErrorHandler::ReportStatus method</span></span>

<span data-ttu-id="9c559-104">Controla el estado del dispositivo y los mensajes de error durante las transferencias de datos de imagen y muestra los mensajes al usuario.</span><span class="sxs-lookup"><span data-stu-id="9c559-104">Handles device status and error messages during image data transfers and displays the messages to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c559-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c559-105">Syntax</span></span>


```C++
HRESULT ReportStatus(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaItem2,
  [in] HRESULT   hrStatus,
  [in] LONG      lPercentComplete
);
```



## <a name="parameters"></a><span data-ttu-id="9c559-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c559-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c559-107">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9c559-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c559-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="9c559-108">Type: **LONG**</span></span>

<span data-ttu-id="9c559-109">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9c559-109">Not used.</span></span> <span data-ttu-id="9c559-110">Establecer en 0.</span><span class="sxs-lookup"><span data-stu-id="9c559-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="9c559-111">*pWiaItem2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9c559-111">*pWiaItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c559-112">Tipo: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="9c559-112">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="9c559-113">Puntero al elemento que se va a transferir.</span><span class="sxs-lookup"><span data-stu-id="9c559-113">Pointer to the item being transferred.</span></span>

</dd> <dt>

<span data-ttu-id="9c559-114">_hrStatus \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="9c559-114">_hrStatus\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c559-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9c559-115">Type: **HRESULT**</span></span>

<span data-ttu-id="9c559-116">Código de estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c559-116">Device status code.</span></span>

</dd> <dt>

<span data-ttu-id="9c559-117">*lPercentComplete* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9c559-117">*lPercentComplete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c559-118">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="9c559-118">Type: **LONG**</span></span>

<span data-ttu-id="9c559-119">Porcentaje completado de la operación actual.</span><span class="sxs-lookup"><span data-stu-id="9c559-119">Percentage completed of current operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c559-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c559-120">Return value</span></span>

<span data-ttu-id="9c559-121">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9c559-121">Type: **HRESULT**</span></span>

<span data-ttu-id="9c559-122">Devuelve *hrStatus* si no es posible la recuperación del error.</span><span class="sxs-lookup"><span data-stu-id="9c559-122">Returns *hrStatus* if recovery from the error is not possible.</span></span> <span data-ttu-id="9c559-123">De lo contrario, devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="9c559-123">Otherwise, it returns one of the following values.</span></span>



| <span data-ttu-id="9c559-124">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9c559-124">Return code</span></span>                                                                                              | <span data-ttu-id="9c559-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c559-125">Description</span></span>                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9c559-126"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9c559-126"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="9c559-127">Si *hrStatus* es un error, se realizó la acción adecuada para corregir el error y la transferencia puede continuar.</span><span class="sxs-lookup"><span data-stu-id="9c559-127">If *hrStatus* is an error, the appropriate action was taken to correct the error, and the transfer can continue.</span></span> <span data-ttu-id="9c559-128">Si *hrStatus* es informativo, se informa al usuario con un cuadro de diálogo no modal y decidió no cancelar la transferencia.</span><span class="sxs-lookup"><span data-stu-id="9c559-128">If *hrStatus* is informational, the user was informed with a modeless dialog box and chose not to cancel the transfer.</span></span><br/> |
| <dl> <span data-ttu-id="9c559-129"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="9c559-129"><dt>**S\_FALSE**</dt></span></span> </dl>                  | <span data-ttu-id="9c559-130">El usuario canceló la transferencia del cuadro de diálogo no modal del controlador de errores.</span><span class="sxs-lookup"><span data-stu-id="9c559-130">The user cancelled the transfer from the error handler modeless dialog box.</span></span> <span data-ttu-id="9c559-131">Este valor se puede devolver en cualquier momento, independientemente de lo que sea *hrStatus* .</span><span class="sxs-lookup"><span data-stu-id="9c559-131">This value can be returned at any point no matter what *hrStatus* is.</span></span> <br/>                                                                                      |
| <dl> <span data-ttu-id="9c559-132"><dt>**Estado de WIA \_ \_ no \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="9c559-132"><dt>**WIA\_STATUS\_NOT\_HANDLED**</dt></span></span> </dl> | <span data-ttu-id="9c559-133">No se realizó ninguna acción. es decir, no se presentó ningún cuadro de diálogo al usuario.</span><span class="sxs-lookup"><span data-stu-id="9c559-133">No action was taken; that is, no dialog box was presented to the user.</span></span> <span data-ttu-id="9c559-134">Se invocará el siguiente controlador de errores.</span><span class="sxs-lookup"><span data-stu-id="9c559-134">The next error handler will be invoked.</span></span> <span data-ttu-id="9c559-135">El orden de los controladores de errores es: aplicación, controlador y valor predeterminado del sistema.</span><span class="sxs-lookup"><span data-stu-id="9c559-135">The order of error handlers is: application, driver, and system default.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="9c559-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c559-136">Remarks</span></span>

<span data-ttu-id="9c559-137">El parámetro *lPercentComplete* habilita una ventana de controlador de errores para mostrar el progreso.</span><span class="sxs-lookup"><span data-stu-id="9c559-137">The *lPercentComplete* parameter enables an error handler window to show progress.</span></span> <span data-ttu-id="9c559-138">Por ejemplo, un controlador podría proporcionar una estimación del tiempo que tarda "calentamiento".</span><span class="sxs-lookup"><span data-stu-id="9c559-138">For example, a driver might provide an estimate of how long "warming up" takes.</span></span> <span data-ttu-id="9c559-139">El parámetro *lPercentComplete* pasado a **IWiaAppErrorHandler:: ReportStatus** es el mismo valor que el **lPercentComplete** que el controlador establece en la estructura [**WiaTransferParams**](-wia-wiatransferparams.md) .</span><span class="sxs-lookup"><span data-stu-id="9c559-139">The *lPercentComplete* parameter passed into **IWiaAppErrorHandler::ReportStatus** is the same value as the **lPercentComplete** that the driver sets into the [**WiaTransferParams**](-wia-wiatransferparams.md) structure.</span></span>

<span data-ttu-id="9c559-140">Un controlador de errores puede usar las macros SUCCEEDED y FAILed para averiguar si *hrStatus* tiene un \_ error de gravedad o una gravedad \_ correcta.</span><span class="sxs-lookup"><span data-stu-id="9c559-140">An error handler can use the SUCCEEDED and FAILED macros to find out if *hrStatus* has SEVERITY\_ERROR or SEVERITY\_SUCCESS.</span></span>

<span data-ttu-id="9c559-141">Si *hrStatus* es el éxito de la gravedad \_ , se debe permitir que el usuario cancele la transferencia.</span><span class="sxs-lookup"><span data-stu-id="9c559-141">If *hrStatus* is SEVERITY\_SUCCESS, the user should be allowed to cancel the transfer.</span></span>

<span data-ttu-id="9c559-142">Si *hrStatus* es \_ un error de gravedad, el controlador de errores debería mostrar un cuadro de diálogo modal perteneciente a la ventana primaria de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9c559-142">If *hrStatus* is SEVERITY\_ERROR, the error handler should display a modal dialog box owned by the application parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c559-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c559-143">Requirements</span></span>



| <span data-ttu-id="9c559-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c559-144">Requirement</span></span> | <span data-ttu-id="9c559-145">Value</span><span class="sxs-lookup"><span data-stu-id="9c559-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c559-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c559-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9c559-147">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9c559-147">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9c559-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c559-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9c559-149">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c559-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9c559-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c559-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c559-151"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c559-151"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="9c559-152">IDL</span><span class="sxs-lookup"><span data-stu-id="9c559-152">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9c559-153"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9c559-153"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="9c559-154">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9c559-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="9c559-155"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c559-155"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 





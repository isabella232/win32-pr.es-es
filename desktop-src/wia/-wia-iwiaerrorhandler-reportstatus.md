---
description: Controla el estado y los mensajes de error durante las transferencias de datos de imagen y los muestra al usuario.
ms.assetid: 23e85c63-80b9-4510-854d-289c8d23be2d
title: 'IWiaErrorHandler:: ReportStatus (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 30a082502d4c7bc5b789fd1ec19fdb76f63d8fab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667487"
---
# <a name="iwiaerrorhandlerreportstatus-method"></a><span data-ttu-id="182b7-103">IWiaErrorHandler:: ReportStatus (método)</span><span class="sxs-lookup"><span data-stu-id="182b7-103">IWiaErrorHandler::ReportStatus method</span></span>

<span data-ttu-id="182b7-104">Controla el estado y los mensajes de error durante las transferencias de datos de imagen y los muestra al usuario.</span><span class="sxs-lookup"><span data-stu-id="182b7-104">Handles status and error messages during image data transfers and displays them to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="182b7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="182b7-105">Syntax</span></span>


```C++
HRESULT ReportStatus(
  [in] HWND     hwndParent,
  [in] IUnknown *punkItem,
  [in] HRESULT  hrStatus,
  [in] LONG     cbResLength,
  [in] BYTE     *pbData
);
```



## <a name="parameters"></a><span data-ttu-id="182b7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="182b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="182b7-107">*hwndParent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="182b7-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="182b7-108">Tipo: **hWnd**</span><span class="sxs-lookup"><span data-stu-id="182b7-108">Type: **HWND**</span></span>

<span data-ttu-id="182b7-109">**HWnd** que es la ventana primaria de la ventana de mensaje.</span><span class="sxs-lookup"><span data-stu-id="182b7-109">**HWND** that is the parent window for the message window.</span></span>

</dd> <dt>

<span data-ttu-id="182b7-110">*punkItem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="182b7-110">*punkItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="182b7-111">Tipo: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="182b7-111">Type: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="182b7-112">Puntero a la interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) del elemento que se va a transferir.</span><span class="sxs-lookup"><span data-stu-id="182b7-112">Pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the item being transferred.</span></span> <span data-ttu-id="182b7-113">Este objeto implementa mínimamente [_ *IWiaItem2* \*](-wia-iwiaitem2.md) y [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span><span class="sxs-lookup"><span data-stu-id="182b7-113">This object minimally implements [_ *IWiaItem2*\*](-wia-iwiaitem2.md) and [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span></span>

</dd> <dt>

<span data-ttu-id="182b7-114">*hrStatus* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="182b7-114">*hrStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="182b7-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="182b7-115">Type: **HRESULT**</span></span>

<span data-ttu-id="182b7-116">**HRESULT** que es el código de estado recibido por [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="182b7-116">**HRESULT** that is the status code received by [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> <dt>

<span data-ttu-id="182b7-117">*cbResLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="182b7-117">*cbResLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="182b7-118">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="182b7-118">Type: **LONG**</span></span>

<span data-ttu-id="182b7-119">**Long** que es el tamaño de los datos a los que hace referencia *pbData*.</span><span class="sxs-lookup"><span data-stu-id="182b7-119">**LONG** that is the size of the data referred to by *pbData*.</span></span>

</dd> <dt>

<span data-ttu-id="182b7-120">*pbData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="182b7-120">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="182b7-121">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="182b7-121">Type: \**BYTE\** _</span></span>

<span data-ttu-id="182b7-122">Puntero al búfer de datos tal y como lo recibe [_ *BandedDataCallback* \*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="182b7-122">Pointer to the data buffer as received by [_ *BandedDataCallback*\*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="182b7-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="182b7-123">Return value</span></span>

<span data-ttu-id="182b7-124">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="182b7-124">Type: **HRESULT**</span></span>

<span data-ttu-id="182b7-125">Devuelve *hrStatus* si el error no se puede recuperar de.</span><span class="sxs-lookup"><span data-stu-id="182b7-125">Returns *hrStatus* if the error cannot be recovered from.</span></span> <span data-ttu-id="182b7-126">De lo contrario, devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="182b7-126">Otherwise, it returns one of the following values.</span></span>



| <span data-ttu-id="182b7-127">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="182b7-127">Return code</span></span>                                                                             | <span data-ttu-id="182b7-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="182b7-128">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="182b7-129"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="182b7-129"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="182b7-130">Se realizó la acción adecuada para corregir el error y la transferencia puede continuar.</span><span class="sxs-lookup"><span data-stu-id="182b7-130">The appropriate action was taken to correct the error and the transfer can continue.</span></span> <br/> |
| <dl> <span data-ttu-id="182b7-131"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="182b7-131"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="182b7-132">No se realizó ninguna acción para controlar el estado del error o del informe al usuario.</span><span class="sxs-lookup"><span data-stu-id="182b7-132">No action was taken to handle the error or report status to the user.</span></span> <br/>                |
| <dl> <span data-ttu-id="182b7-133"><dt>**E \_ anular**</dt></span><span class="sxs-lookup"><span data-stu-id="182b7-133"><dt>**E\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="182b7-134">El usuario decidió anular la transferencia en respuesta al cuadro de diálogo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="182b7-134">The user chose to abort the transfer in response to the displayed dialog box.</span></span> <br/>        |



 

## <a name="remarks"></a><span data-ttu-id="182b7-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="182b7-135">Remarks</span></span>

<span data-ttu-id="182b7-136">La adquisición de imágenes de Windows (WIA) 2,0 llama a **IWiaErrorHandler:: ReportStatus** cuando el controlador envía un mensaje de [](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback) **\_ \_ \_ Estado de dispositivo MSG de ti** a BandedDataCallback.</span><span class="sxs-lookup"><span data-stu-id="182b7-136">Windows Image Acquisition (WIA) 2.0 calls **IWiaErrorHandler::ReportStatus** when the driver sends an **IT\_MSG\_DEVICE\_STATUS** message to [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span> <span data-ttu-id="182b7-137">Este método controla el mensaje y muestra información al usuario sobre el estado o el error.</span><span class="sxs-lookup"><span data-stu-id="182b7-137">This method handles the message and displays information to the user about the status or error.</span></span> <span data-ttu-id="182b7-138">Si el mensaje es un error, el método permite al usuario elegir, si es posible, si intenta recuperar el error y continuar con la transferencia o anular la operación.</span><span class="sxs-lookup"><span data-stu-id="182b7-138">If the message is about an error, the method lets the user choose, if possible, whether to try to recover from the error and continue the transfer or to abort.</span></span>

<span data-ttu-id="182b7-139">*hrStatus* se establece en \_ la transferencia de estado de WIA \_ \_ Inicio para informar al controlador de que se ha iniciado una transferencia.</span><span class="sxs-lookup"><span data-stu-id="182b7-139">*hrStatus* is set to WIA\_STATUS\_TRANSFER\_BEGIN to inform the handler a transfer has started.</span></span> <span data-ttu-id="182b7-140">Se establece en fin de \_ la transferencia de estado de WIA \_ \_ cuando se completa la transferencia.</span><span class="sxs-lookup"><span data-stu-id="182b7-140">It is set to WIA\_STATUS\_TRANSFER\_END when the transfer is complete.</span></span>

<span data-ttu-id="182b7-141">Si *hrStatus* es el éxito de la gravedad \_ , se debe permitir que el usuario cancele la transferencia.</span><span class="sxs-lookup"><span data-stu-id="182b7-141">If *hrStatus* is SEVERITY\_SUCCESS, the user should be allowed to cancel the transfer.</span></span>

## <a name="requirements"></a><span data-ttu-id="182b7-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="182b7-142">Requirements</span></span>



| <span data-ttu-id="182b7-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="182b7-143">Requirement</span></span> | <span data-ttu-id="182b7-144">Value</span><span class="sxs-lookup"><span data-stu-id="182b7-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="182b7-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="182b7-145">Minimum supported client</span></span><br/> | <span data-ttu-id="182b7-146">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="182b7-146">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="182b7-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="182b7-147">Minimum supported server</span></span><br/> | <span data-ttu-id="182b7-148">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="182b7-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="182b7-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="182b7-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="182b7-150"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="182b7-150"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="182b7-151">IDL</span><span class="sxs-lookup"><span data-stu-id="182b7-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="182b7-152"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="182b7-152"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="182b7-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="182b7-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="182b7-154"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="182b7-154"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 

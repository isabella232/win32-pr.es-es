---
description: El método RenderOutputPins crea la parte de vista previa del gráfico de filtro.
ms.assetid: 66bcb698-cd85-4c22-bfef-2e51973958f1
title: 'IRenderEngine:: RenderOutputPins (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.RenderOutputPins
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e7356df1bb79aa3b1901ee6d3de22510a6df1a9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680714"
---
# <a name="irenderenginerenderoutputpins-method"></a><span data-ttu-id="53518-103">IRenderEngine:: RenderOutputPins (método)</span><span class="sxs-lookup"><span data-stu-id="53518-103">IRenderEngine::RenderOutputPins method</span></span>

> [!Note]  
> <span data-ttu-id="53518-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="53518-104">\[Deprecated.</span></span> <span data-ttu-id="53518-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="53518-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="53518-106">El `RenderOutputPins` método crea la parte de vista previa del gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="53518-106">The `RenderOutputPins` method creates the previewing portion of the filter graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="53518-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53518-107">Syntax</span></span>


```C++
HRESULT RenderOutputPins();
```



## <a name="parameters"></a><span data-ttu-id="53518-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53518-108">Parameters</span></span>

<span data-ttu-id="53518-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="53518-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="53518-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53518-110">Return value</span></span>

<span data-ttu-id="53518-111">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="53518-111">Returns an **HRESULT** values.</span></span> <span data-ttu-id="53518-112">Estos son los valores posibles:</span><span class="sxs-lookup"><span data-stu-id="53518-112">The following are possible values:</span></span>



| <span data-ttu-id="53518-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="53518-113">Return code</span></span>                                                                                                  | <span data-ttu-id="53518-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="53518-114">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="53518-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="53518-115"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="53518-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="53518-116">Success.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="53518-117"><dt>**\_no se \_ representa el audio VFW S \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="53518-117"><dt>**VFW\_S\_AUDIO\_NOT\_RENDERED**</dt></span></span> </dl>  | <span data-ttu-id="53518-118">No se puede reproducir la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="53518-118">Cannot play back the audio stream.</span></span><br/>                              |
| <dl> <span data-ttu-id="53518-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="53518-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                 | <span data-ttu-id="53518-120">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="53518-120">Invalid argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="53518-121"><dt>**el \_ motor de representación E \_ \_ está \_ roto**</dt></span><span class="sxs-lookup"><span data-stu-id="53518-121"><dt>**E\_RENDER\_ENGINE\_IS\_BROKEN**</dt></span></span> </dl> | <span data-ttu-id="53518-122">No se pudo realizar la operación porque el proyecto no se representó correctamente.</span><span class="sxs-lookup"><span data-stu-id="53518-122">Operation failed because project was not rendered successfully.</span></span><br/> |
| <dl> <span data-ttu-id="53518-123"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="53518-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>                 | <span data-ttu-id="53518-124">error inesperado.</span><span class="sxs-lookup"><span data-stu-id="53518-124">Unexpected error.</span></span><br/>                                               |



 

## <a name="remarks"></a><span data-ttu-id="53518-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53518-125">Remarks</span></span>

<span data-ttu-id="53518-126">Antes de llamar a este método, llame a [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) para compilar el front-end del gráfico.</span><span class="sxs-lookup"><span data-stu-id="53518-126">Before calling this method, call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) to build the front end of the graph.</span></span> <span data-ttu-id="53518-127">Para realizar una operación distinta de la vista previa, no llame a este método.</span><span class="sxs-lookup"><span data-stu-id="53518-127">To perform an operation other than preview, do not call this method.</span></span> <span data-ttu-id="53518-128">En su lugar, llame a [**IRenderEngine:: GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) para obtener punteros a los pin de salida.</span><span class="sxs-lookup"><span data-stu-id="53518-128">Instead, call [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) to obtain pointers to the output pins.</span></span>

<span data-ttu-id="53518-129">Si no hay ninguna tarjeta de sonido en el equipo del usuario, este método devuelve VFW \_ s \_ audio \_ no \_ representado.</span><span class="sxs-lookup"><span data-stu-id="53518-129">If there is no sound card on the user's computer, this method returns VFW\_S\_AUDIO\_NOT\_RENDERED.</span></span> <span data-ttu-id="53518-130">En este caso, no habrá vista previa de audio, pero la vista previa de vídeo no se ve afectada.</span><span class="sxs-lookup"><span data-stu-id="53518-130">There will not be audio preview in this case, but video preview is unaffected.</span></span>

<span data-ttu-id="53518-131">Si el PIN es de un grupo de vídeos, este método crea una ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="53518-131">If the pin is from a video group, this method creates a video window.</span></span> <span data-ttu-id="53518-132">El subproceso que realiza la llamada debe enviar los mensajes (por ejemplo, para desplace la ventana o responder a los clics del mouse en el área cliente de la ventana).</span><span class="sxs-lookup"><span data-stu-id="53518-132">The calling thread must dispatch messages—for example, to move the window, or respond to mouse clicks in the window's client area.</span></span>

> [!Note]  
> <span data-ttu-id="53518-133">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="53518-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="53518-134">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="53518-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="53518-135">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="53518-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="53518-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53518-136">Requirements</span></span>



| <span data-ttu-id="53518-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="53518-137">Requirement</span></span> | <span data-ttu-id="53518-138">Value</span><span class="sxs-lookup"><span data-stu-id="53518-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53518-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53518-139">Header</span></span><br/>  | <dl> <span data-ttu-id="53518-140"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="53518-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="53518-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="53518-141">Library</span></span><br/> | <dl> <span data-ttu-id="53518-142"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53518-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53518-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="53518-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53518-144">**Interfaz IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="53518-144">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="53518-145">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="53518-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





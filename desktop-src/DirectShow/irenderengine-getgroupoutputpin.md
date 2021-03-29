---
description: El método GetGroupOutputPin recupera el PIN de salida para el grupo especificado.
ms.assetid: be4e17b6-15bf-43b1-8d93-d52d08c8bce6
title: 'IRenderEngine:: GetGroupOutputPin (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetGroupOutputPin
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 21e603e15f598c6d493e179a147391cb941a6c7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680615"
---
# <a name="irenderenginegetgroupoutputpin-method"></a><span data-ttu-id="e6049-103">IRenderEngine:: GetGroupOutputPin (método)</span><span class="sxs-lookup"><span data-stu-id="e6049-103">IRenderEngine::GetGroupOutputPin method</span></span>

> [!Note]  
> <span data-ttu-id="e6049-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="e6049-104">\[Deprecated.</span></span> <span data-ttu-id="e6049-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e6049-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e6049-106">El `GetGroupOutputPin` método recupera el PIN de salida para el grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="e6049-106">The `GetGroupOutputPin` method retrieves the output pin for the specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6049-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6049-107">Syntax</span></span>


```C++
HRESULT GetGroupOutputPin(
        long Group,
  [out] IPin **ppRenderPin
);
```



## <a name="parameters"></a><span data-ttu-id="e6049-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6049-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6049-109">*Grupo*</span><span class="sxs-lookup"><span data-stu-id="e6049-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="e6049-110">Índice de base cero que especifica el grupo.</span><span class="sxs-lookup"><span data-stu-id="e6049-110">Zero-based index that specifies the group.</span></span>

</dd> <dt>

<span data-ttu-id="e6049-111">*ppRenderPin* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e6049-111">*ppRenderPin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6049-112">Recibe un puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="e6049-112">Receives a pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6049-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6049-113">Return value</span></span>

<span data-ttu-id="e6049-114">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e6049-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e6049-115">Entre los valores posibles figuran los siguientes:</span><span class="sxs-lookup"><span data-stu-id="e6049-115">Possible values include the following:</span></span>



| <span data-ttu-id="e6049-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e6049-116">Return code</span></span>                                                                                                  | <span data-ttu-id="e6049-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6049-117">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e6049-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e6049-118"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="e6049-119">El grupo no tiene un PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="e6049-119">Group does not have an output pin.</span></span><br/>                              |
| <dl> <span data-ttu-id="e6049-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e6049-120"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="e6049-121">Correcto.</span><span class="sxs-lookup"><span data-stu-id="e6049-121">Success.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e6049-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e6049-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                 | <span data-ttu-id="e6049-123">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="e6049-123">Invalid argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="e6049-124"><dt>**E \_ debe \_ inicializar el \_ representador**</dt></span><span class="sxs-lookup"><span data-stu-id="e6049-124"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl>       | <span data-ttu-id="e6049-125">No se pudo inicializar el motor de representación.</span><span class="sxs-lookup"><span data-stu-id="e6049-125">Render engine failed to initialize.</span></span><br/>                             |
| <dl> <span data-ttu-id="e6049-126"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="e6049-126"><dt>**E\_POINTER**</dt></span></span> </dl>                    | <span data-ttu-id="e6049-127">Puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="e6049-127">Invalid pointer.</span></span><br/>                                                |
| <dl> <span data-ttu-id="e6049-128"><dt>**el \_ motor de representación E \_ \_ está \_ roto**</dt></span><span class="sxs-lookup"><span data-stu-id="e6049-128"><dt>**E\_RENDER\_ENGINE\_IS\_BROKEN**</dt></span></span> </dl> | <span data-ttu-id="e6049-129">No se pudo realizar la operación porque el proyecto no se representó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e6049-129">Operation failed because project was not rendered successfully.</span></span><br/> |
| <dl> <span data-ttu-id="e6049-130"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="e6049-130"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>                 | <span data-ttu-id="e6049-131">error inesperado.</span><span class="sxs-lookup"><span data-stu-id="e6049-131">Unexpected error.</span></span><br/>                                               |



 

## <a name="remarks"></a><span data-ttu-id="e6049-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6049-132">Remarks</span></span>

<span data-ttu-id="e6049-133">Antes de llamar a este método, llame a [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) para compilar el front-end del gráfico.</span><span class="sxs-lookup"><span data-stu-id="e6049-133">Before calling this method, call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) to build the front end of the graph.</span></span> <span data-ttu-id="e6049-134">Cada grupo representa un flujo multimedia único y el front-end tiene un PIN de salida correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e6049-134">Each group represents a single media stream, and the front end has a corresponding output pin.</span></span>

<span data-ttu-id="e6049-135">Puede usar este método para crear la parte de representación de un gráfico de escritura de archivos.</span><span class="sxs-lookup"><span data-stu-id="e6049-135">You can use this method to create the rendering portion of a file-writing graph.</span></span> <span data-ttu-id="e6049-136">Conecte los pin de salida a filtros de multiplexor y filtros de escritura de archivo.</span><span class="sxs-lookup"><span data-stu-id="e6049-136">Connect the output pins to multiplexer filters and file writer filters.</span></span> <span data-ttu-id="e6049-137">Para obtener más información, vea [representar un proyecto](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="e6049-137">For more information, see [Rendering a Project](rendering-a-project.md).</span></span>

<span data-ttu-id="e6049-138">En la vista previa, no es necesario llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="e6049-138">For preview, you don't need to call this method.</span></span> <span data-ttu-id="e6049-139">Simplemente llame a **ConnectFrontEnd** seguido de [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md).</span><span class="sxs-lookup"><span data-stu-id="e6049-139">Just call **ConnectFrontEnd** followed by [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md).</span></span>

<span data-ttu-id="e6049-140">Si el método devuelve S \_ correcto, la interfaz **IPin** que devuelve tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="e6049-140">If the method returns S\_OK, the **IPin** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="e6049-141">Asegúrese de liberar la interfaz cuando termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="e6049-141">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="e6049-142">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="e6049-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e6049-143">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e6049-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e6049-144">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e6049-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e6049-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6049-145">Requirements</span></span>



| <span data-ttu-id="e6049-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6049-146">Requirement</span></span> | <span data-ttu-id="e6049-147">Value</span><span class="sxs-lookup"><span data-stu-id="e6049-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6049-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6049-148">Header</span></span><br/>  | <dl> <span data-ttu-id="e6049-149"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6049-149"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e6049-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6049-150">Library</span></span><br/> | <dl> <span data-ttu-id="e6049-151"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6049-151"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6049-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6049-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6049-153">**Interfaz IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="e6049-153">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="e6049-154">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="e6049-154">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





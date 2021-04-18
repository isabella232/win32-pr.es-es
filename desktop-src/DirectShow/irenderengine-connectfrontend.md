---
description: El método ConnectFrontEnd crea el front-end del gráfico de filtro a partir de la escala de tiempo actual.
ms.assetid: ac484fd6-b88d-4c3a-bc4d-f118083d706d
title: 'IRenderEngine:: ConnectFrontEnd (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.ConnectFrontEnd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 58ebd8e162f376b6ef942397e601139c46d8e4cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680616"
---
# <a name="irenderengineconnectfrontend-method"></a><span data-ttu-id="a8bf2-103">IRenderEngine:: ConnectFrontEnd (método)</span><span class="sxs-lookup"><span data-stu-id="a8bf2-103">IRenderEngine::ConnectFrontEnd method</span></span>

> [!Note]  
> <span data-ttu-id="a8bf2-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="a8bf2-104">\[Deprecated.</span></span> <span data-ttu-id="a8bf2-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a8bf2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a8bf2-106">El `ConnectFrontEnd` método crea el front-end del gráfico de filtro a partir de la escala de tiempo actual.</span><span class="sxs-lookup"><span data-stu-id="a8bf2-106">The `ConnectFrontEnd` method builds the front end of the filter graph from the current timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8bf2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8bf2-107">Syntax</span></span>


```C++
HRESULT ConnectFrontEnd();
```



## <a name="parameters"></a><span data-ttu-id="a8bf2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8bf2-108">Parameters</span></span>

<span data-ttu-id="a8bf2-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a8bf2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8bf2-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8bf2-110">Return value</span></span>

<span data-ttu-id="a8bf2-111">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a8bf2-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a8bf2-112">Entre los posibles valores devueltos se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a8bf2-112">Possible return values include the following:</span></span>



| <span data-ttu-id="a8bf2-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a8bf2-113">Return code</span></span>                                                                                                  | <span data-ttu-id="a8bf2-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8bf2-114">Description</span></span>                                                                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a8bf2-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a8bf2-115"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="a8bf2-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="a8bf2-116">Success.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="a8bf2-117"><dt>**S \_ WARN \_ OUTPUTRESET**</dt></span><span class="sxs-lookup"><span data-stu-id="a8bf2-117"><dt>**S\_WARN\_OUTPUTRESET**</dt></span></span> </dl>          | <span data-ttu-id="a8bf2-118">Se eliminó la parte de representación del gráfico.</span><span class="sxs-lookup"><span data-stu-id="a8bf2-118">Rendering portion of the graph was deleted.</span></span><br/>                         |
| <dl> <span data-ttu-id="a8bf2-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a8bf2-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                 | <span data-ttu-id="a8bf2-120">No se ha establecido una escala de tiempo para este motor de representación.</span><span class="sxs-lookup"><span data-stu-id="a8bf2-120">No timeline set for this render engine.</span></span><br/>                             |
| <dl> <span data-ttu-id="a8bf2-121"><dt>**E \_ debe \_ inicializar el \_ representador**</dt></span><span class="sxs-lookup"><span data-stu-id="a8bf2-121"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl>       | <span data-ttu-id="a8bf2-122">No se pudo inicializar el motor de representación.</span><span class="sxs-lookup"><span data-stu-id="a8bf2-122">Render engine failed to initialize.</span></span><br/>                                 |
| <dl> <span data-ttu-id="a8bf2-123"><dt>**el \_ motor de representación E \_ \_ está \_ roto**</dt></span><span class="sxs-lookup"><span data-stu-id="a8bf2-123"><dt>**E\_RENDER\_ENGINE\_IS\_BROKEN**</dt></span></span> </dl> | <span data-ttu-id="a8bf2-124">No se pudo realizar la operación porque el proyecto no se representó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a8bf2-124">Operation failed because the project was not rendered successfully.</span></span><br/> |
| <dl> <span data-ttu-id="a8bf2-125"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="a8bf2-125"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>                 | <span data-ttu-id="a8bf2-126">error inesperado.</span><span class="sxs-lookup"><span data-stu-id="a8bf2-126">Unexpected error.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="a8bf2-127"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="a8bf2-127"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl>      | <span data-ttu-id="a8bf2-128">Tipo de medio no válido.</span><span class="sxs-lookup"><span data-stu-id="a8bf2-128">Invalid media type.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="a8bf2-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8bf2-129">Remarks</span></span>

<span data-ttu-id="a8bf2-130">Este método no genera la parte de representación del gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="a8bf2-130">This method does not build the rendering portion of the filter graph.</span></span> <span data-ttu-id="a8bf2-131">La aplicación debe conectar los pin de salida en el front-end a los filtros de representación deseados:</span><span class="sxs-lookup"><span data-stu-id="a8bf2-131">The application must connect the output pins on the front end to the desired rendering filters:</span></span>

-   <span data-ttu-id="a8bf2-132">Para obtener una vista previa, llame al método [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md) .</span><span class="sxs-lookup"><span data-stu-id="a8bf2-132">To preview, call the [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md) method.</span></span>
-   <span data-ttu-id="a8bf2-133">Para generar un archivo, llame a [**IRenderEngine:: GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) para recuperar el PIN de salida de cada grupo y, a continuación, conecte los pin a un filtro de multiplexor.</span><span class="sxs-lookup"><span data-stu-id="a8bf2-133">To output a file, call [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) to retrieve the output pin for each group, then connect the pins to a multiplexer filter.</span></span>

<span data-ttu-id="a8bf2-134">Si usa el motor de representación básico, los terminales de salida del front-end generan datos sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="a8bf2-134">If you are using the basic render engine, the output pins on the front end produce uncompressed data.</span></span> <span data-ttu-id="a8bf2-135">Si usa el motor de representación inteligente, los pin de salida generan datos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="a8bf2-135">If you are using the smart render engine, the output pins produce compressed data.</span></span>

<span data-ttu-id="a8bf2-136">Si cambia la escala de tiempo después de compilar el gráfico de filtros, debe volver a llamar `ConnectFrontEnd` a para volver a generar el front-end.</span><span class="sxs-lookup"><span data-stu-id="a8bf2-136">If you change the timeline after you build the filter graph, you must call `ConnectFrontEnd` again to rebuild the front end.</span></span> <span data-ttu-id="a8bf2-137">El método conserva la parte de representación del gráfico siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="a8bf2-137">The method preserves the rendering portion of the graph whenever possible.</span></span> <span data-ttu-id="a8bf2-138">Sin embargo, si agrega o elimina un grupo, o cambia el orden de los grupos, `ConnectFrontEnd` elimina la parte de representación y la aplicación debe recompilarla.</span><span class="sxs-lookup"><span data-stu-id="a8bf2-138">However, if you add or delete a group, or change the order of the groups, `ConnectFrontEnd` deletes the rendering portion and your application must rebuild it.</span></span> <span data-ttu-id="a8bf2-139">Si el método elimina la parte de representación, devuelve S \_ WARN \_ OUTPUTRESET.</span><span class="sxs-lookup"><span data-stu-id="a8bf2-139">If the method deletes the rendering portion, it returns S\_WARN\_OUTPUTRESET.</span></span>

> [!Note]  
> <span data-ttu-id="a8bf2-140">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="a8bf2-140">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a8bf2-141">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a8bf2-141">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a8bf2-142">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a8bf2-142">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a8bf2-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8bf2-143">Requirements</span></span>



| <span data-ttu-id="a8bf2-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8bf2-144">Requirement</span></span> | <span data-ttu-id="a8bf2-145">Value</span><span class="sxs-lookup"><span data-stu-id="a8bf2-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bf2-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8bf2-146">Header</span></span><br/>  | <dl> <span data-ttu-id="a8bf2-147"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8bf2-147"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a8bf2-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a8bf2-148">Library</span></span><br/> | <dl> <span data-ttu-id="a8bf2-149"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8bf2-149"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8bf2-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8bf2-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8bf2-151">**Interfaz IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="a8bf2-151">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="a8bf2-152">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="a8bf2-152">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





---
description: El método GetGroupCompressor recupera el filtro de compresión para el grupo especificado.
ms.assetid: 9d71e659-7abb-48c6-b9bd-5239560dc150
title: 'ISmartRenderEngine:: GetGroupCompressor (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.GetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd866daa225ab398e1a578aa8d21e73bad15e96d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680301"
---
# <a name="ismartrenderenginegetgroupcompressor-method"></a><span data-ttu-id="9f7fc-103">ISmartRenderEngine:: GetGroupCompressor (método)</span><span class="sxs-lookup"><span data-stu-id="9f7fc-103">ISmartRenderEngine::GetGroupCompressor method</span></span>

> [!Note]  
> <span data-ttu-id="9f7fc-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="9f7fc-104">\[Deprecated.</span></span> <span data-ttu-id="9f7fc-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9f7fc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9f7fc-106">El `GetGroupCompressor` método recupera el filtro de compresión para el grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="9f7fc-106">The `GetGroupCompressor` method retrieves the compression filter for the specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f7fc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f7fc-107">Syntax</span></span>


```C++
HRESULT GetGroupCompressor(
   long        Group,
   IBaseFilter **pCompressor
);
```



## <a name="parameters"></a><span data-ttu-id="9f7fc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f7fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f7fc-109">*Grupo*</span><span class="sxs-lookup"><span data-stu-id="9f7fc-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="9f7fc-110">Índice de base cero del grupo.</span><span class="sxs-lookup"><span data-stu-id="9f7fc-110">Zero-based index of the group.</span></span>

</dd> <dt>

<span data-ttu-id="9f7fc-111">*pCompressor*</span><span class="sxs-lookup"><span data-stu-id="9f7fc-111">*pCompressor*</span></span> 
</dt> <dd>

<span data-ttu-id="9f7fc-112">Recibe un puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro de compresión.</span><span class="sxs-lookup"><span data-stu-id="9f7fc-112">Receives a pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the compression filter.</span></span> <span data-ttu-id="9f7fc-113">Recibe el valor **null** si no hay ningún filtro de compresión.</span><span class="sxs-lookup"><span data-stu-id="9f7fc-113">It receives the value **NULL** if there is no compression filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f7fc-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f7fc-114">Return value</span></span>

<span data-ttu-id="9f7fc-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9f7fc-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9f7fc-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9f7fc-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f7fc-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f7fc-117">Remarks</span></span>

<span data-ttu-id="9f7fc-118">Use este método para establecer las propiedades del filtro de compresión, como la velocidad de fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="9f7fc-118">Use this method to set properties on the compression filter, such as the key-frame rate.</span></span> <span data-ttu-id="9f7fc-119">Llame a este método después de llamar a [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md), pero antes de representar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="9f7fc-119">Call this method after calling [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md), but before rendering the project.</span></span> <span data-ttu-id="9f7fc-120">A continuación, consulte el PIN de salida del filtro de compresión para la interfaz [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) , que contiene los métodos para establecer los parámetros de compresión.</span><span class="sxs-lookup"><span data-stu-id="9f7fc-120">Then query the compression filter's output pin for the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface, which contains methods for setting compression parameters.</span></span> <span data-ttu-id="9f7fc-121">Suelte la interfaz cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="9f7fc-121">Release the interface when you are done.</span></span> <span data-ttu-id="9f7fc-122">Si realiza cambios posteriores en la escala de tiempo, llame a **ConnectFrontEnd** y, a continuación, llame de nuevo a **GetGroupCompressor** para restablecer los parámetros de compresión.</span><span class="sxs-lookup"><span data-stu-id="9f7fc-122">If you make any subsequent changes to the timeline, call **ConnectFrontEnd**, and then call **GetGroupCompressor** again to reset the compression parameters.</span></span>

<span data-ttu-id="9f7fc-123">En la devolución, si el valor de \* *pCompressor* no es **null**, la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="9f7fc-123">On return, if the value of \**pCompressor* is non-**NULL**, the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface has an outstanding reference count.</span></span> <span data-ttu-id="9f7fc-124">Asegúrese de liberar la interfaz cuando haya terminado de usarla.</span><span class="sxs-lookup"><span data-stu-id="9f7fc-124">Be sure to release the interface when you are done using it.</span></span>

> [!Note]  
> <span data-ttu-id="9f7fc-125">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="9f7fc-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9f7fc-126">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9f7fc-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9f7fc-127">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9f7fc-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9f7fc-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f7fc-128">Requirements</span></span>



| <span data-ttu-id="9f7fc-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f7fc-129">Requirement</span></span> | <span data-ttu-id="9f7fc-130">Value</span><span class="sxs-lookup"><span data-stu-id="9f7fc-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f7fc-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f7fc-131">Header</span></span><br/>  | <dl> <span data-ttu-id="9f7fc-132"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f7fc-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9f7fc-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f7fc-133">Library</span></span><br/> | <dl> <span data-ttu-id="9f7fc-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f7fc-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f7fc-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f7fc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f7fc-136">**Interfaz ISmartRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="9f7fc-136">**ISmartRenderEngine Interface**</span></span>](ismartrenderengine.md)
</dt> <dt>

[<span data-ttu-id="9f7fc-137">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="9f7fc-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





---
description: El \_ método de filtro Put especifica un filtro de origen para que lo use el detector de medios.
ms.assetid: 59382cb0-c472-48b8-9cc5-52f9dbc61a07
title: 'IMediaDet: método de ut_Filter de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd07ee3e2a18dcceae752e3923fd5fbdc88c0313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679532"
---
# <a name="imediadetput_filter-method"></a><span data-ttu-id="3c978-103">IMediaDet::p \_ método de filtro UT</span><span class="sxs-lookup"><span data-stu-id="3c978-103">IMediaDet::put\_Filter method</span></span>

> [!Note]  
> <span data-ttu-id="3c978-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="3c978-104">\[Deprecated.</span></span> <span data-ttu-id="3c978-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3c978-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3c978-106">El `put_Filter` método especifica un filtro de origen para que lo use el detector de medios.</span><span class="sxs-lookup"><span data-stu-id="3c978-106">The `put_Filter` method specifies a source filter for the media detector to use.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3c978-107">No agregue el filtro de origen a su propio gráfico de filtros o utilice un filtro que ya esté en un gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="3c978-107">Do not add the source filter to your own filter graph, or use a filter that is already in a filter graph.</span></span> <span data-ttu-id="3c978-108">El objeto de detector de medios crea automáticamente un gráfico de filtro interno y el filtro en otro gráfico puede producir resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="3c978-108">The media detector object automatically builds an internal filter graph, and putting the filter in another graph can cause unexpected results.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3c978-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c978-109">Syntax</span></span>


```C++
HRESULT put_Filter(
  [in] IUnknown *newVal
);
```



## <a name="parameters"></a><span data-ttu-id="3c978-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c978-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c978-111">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3c978-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c978-112">Puntero a la interfaz **IUnknown** del filtro de origen.</span><span class="sxs-lookup"><span data-stu-id="3c978-112">Pointer to the source filter's **IUnknown** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c978-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c978-113">Return value</span></span>

<span data-ttu-id="3c978-114">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3c978-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3c978-115">Entre los valores posibles figuran los siguientes:</span><span class="sxs-lookup"><span data-stu-id="3c978-115">Possible values include the following:</span></span>



| <span data-ttu-id="3c978-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3c978-116">Return code</span></span>                                                                                   | <span data-ttu-id="3c978-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c978-117">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="3c978-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3c978-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3c978-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="3c978-119">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="3c978-120"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="3c978-120"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="3c978-121">*newVal* no apunta a un filtro.</span><span class="sxs-lookup"><span data-stu-id="3c978-121">*newVal* does not point to a filter.</span></span><br/> |
| <dl> <span data-ttu-id="3c978-122"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="3c978-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3c978-123">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="3c978-123">**NULL** pointer argument.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="3c978-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c978-124">Remarks</span></span>

<span data-ttu-id="3c978-125">Para la mayoría de las aplicaciones, es más sencillo llamar al método [**IMediaDet: \_ :p**](imediadet-put-filename.md) el nombre del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="3c978-125">For most applications, it is simpler to call the [**IMediaDet::put\_Filename**](imediadet-put-filename.md) method with the name of a source file.</span></span>

> [!Note]  
> <span data-ttu-id="3c978-126">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="3c978-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3c978-127">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3c978-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3c978-128">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3c978-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3c978-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c978-129">Requirements</span></span>



| <span data-ttu-id="3c978-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c978-130">Requirement</span></span> | <span data-ttu-id="3c978-131">Value</span><span class="sxs-lookup"><span data-stu-id="3c978-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c978-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c978-132">Header</span></span><br/>  | <dl> <span data-ttu-id="3c978-133"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c978-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3c978-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c978-134">Library</span></span><br/> | <dl> <span data-ttu-id="3c978-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c978-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c978-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c978-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c978-137">**Interfaz IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="3c978-137">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="3c978-138">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="3c978-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





---
description: El \_ método get Filter recupera un puntero al filtro de origen utilizado actualmente por el detector de medios.
ms.assetid: 23d603c1-445d-425a-973e-7bfe0a2d19f2
title: 'Método IMediaDet:: get_Filter (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f80b5d5021ca7f04cd56dc319fb5416c3361108
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680896"
---
# <a name="imediadetget_filter-method"></a><span data-ttu-id="95bd1-103">IMediaDet:: get ( \_ método de filtro)</span><span class="sxs-lookup"><span data-stu-id="95bd1-103">IMediaDet::get\_Filter method</span></span>

> [!Note]  
> <span data-ttu-id="95bd1-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="95bd1-104">\[Deprecated.</span></span> <span data-ttu-id="95bd1-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="95bd1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="95bd1-106">El `get_Filter` método recupera un puntero al filtro de origen utilizado actualmente por el detector de medios.</span><span class="sxs-lookup"><span data-stu-id="95bd1-106">The `get_Filter` method retrieves a pointer to the source filter currently used by the media detector.</span></span>

## <a name="syntax"></a><span data-ttu-id="95bd1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95bd1-107">Syntax</span></span>


```C++
HRESULT get_Filter(
  [out, retval] IUnknown **ppVal
);
```



## <a name="parameters"></a><span data-ttu-id="95bd1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95bd1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95bd1-109">*ppVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="95bd1-109">*ppVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="95bd1-110">Recibe un puntero a la interfaz **IUnknown** del filtro.</span><span class="sxs-lookup"><span data-stu-id="95bd1-110">Receives a pointer to the filter's **IUnknown** interface.</span></span> <span data-ttu-id="95bd1-111">Si no hay ningún filtro de origen en uso, el valor se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="95bd1-111">If no source filter is in use, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95bd1-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95bd1-112">Return value</span></span>

<span data-ttu-id="95bd1-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="95bd1-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="95bd1-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="95bd1-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="95bd1-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95bd1-115">Remarks</span></span>

<span data-ttu-id="95bd1-116">Cuando el método devuelve un valor, si *\* ppVal* no es **null**, la interfaz **IUnknown** tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="95bd1-116">When the method returns, if *\*ppVal* is not **NULL**, the **IUnknown** interface has an outstanding reference count.</span></span> <span data-ttu-id="95bd1-117">Suelte la interfaz cuando termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="95bd1-117">Release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="95bd1-118">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="95bd1-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="95bd1-119">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="95bd1-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="95bd1-120">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="95bd1-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="95bd1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95bd1-121">Requirements</span></span>



| <span data-ttu-id="95bd1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="95bd1-122">Requirement</span></span> | <span data-ttu-id="95bd1-123">Value</span><span class="sxs-lookup"><span data-stu-id="95bd1-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95bd1-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95bd1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="95bd1-125"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="95bd1-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="95bd1-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="95bd1-126">Library</span></span><br/> | <dl> <span data-ttu-id="95bd1-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95bd1-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95bd1-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="95bd1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95bd1-129">**Interfaz IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="95bd1-129">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="95bd1-130">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="95bd1-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





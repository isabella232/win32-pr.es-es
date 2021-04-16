---
description: 'Nota: esta interfaz está en desuso.'
ms.assetid: 86095fcf-3364-42a0-95db-08223fa3cc20
title: IAMFilterData::P método arseFilterData (Fil \_ Data. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.ParseFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 18e1367813adff6b0debdfb698644731668bfc5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679393"
---
# <a name="iamfilterdataparsefilterdata-method"></a><span data-ttu-id="2d531-103">IAMFilterData::P método arseFilterData</span><span class="sxs-lookup"><span data-stu-id="2d531-103">IAMFilterData::ParseFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="2d531-104">Esta interfaz está desusada.</span><span class="sxs-lookup"><span data-stu-id="2d531-104">This interface has been deprecated.</span></span> <span data-ttu-id="2d531-105">Las nuevas aplicaciones no deben utilizarla.</span><span class="sxs-lookup"><span data-stu-id="2d531-105">New applications should not use it.</span></span>

 

<span data-ttu-id="2d531-106">El `ParseFilterData` método desempaqueta los datos binarios del registro para un filtro.</span><span class="sxs-lookup"><span data-stu-id="2d531-106">The `ParseFilterData` method unpacks the binary registry data for a filter.</span></span>

<span data-ttu-id="2d531-107">Normalmente no hay ningún motivo para que una aplicación llame a este método.</span><span class="sxs-lookup"><span data-stu-id="2d531-107">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="2d531-108">El método [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) proporciona una manera más cómoda de acceder a los datos del registro del filtro.</span><span class="sxs-lookup"><span data-stu-id="2d531-108">The [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method provides a more convenient way to access the filter registry data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d531-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d531-109">Syntax</span></span>


```C++
HRESULT ParseFilterData(
  [in]  BYTE  *rgbFilterData,
  [in]  ULONG cb,
  [out] BYTE  **prgbRegFilter2
);
```



## <a name="parameters"></a><span data-ttu-id="2d531-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2d531-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d531-111">*rgbFilterData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2d531-111">*rgbFilterData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d531-112">Puntero a los datos del registro binarios.</span><span class="sxs-lookup"><span data-stu-id="2d531-112">Pointer to the binary registry data.</span></span> <span data-ttu-id="2d531-113">Puede obtener estos datos recuperando la propiedad "FilterData" del moniker del filtro.</span><span class="sxs-lookup"><span data-stu-id="2d531-113">You can get this data by retrieving the "FilterData" property from the filter moniker.</span></span> <span data-ttu-id="2d531-114">Los datos se almacenan como una **SAFEARRAY** de bytes ( \_ matriz de VT UI1 \| VT \_ ).</span><span class="sxs-lookup"><span data-stu-id="2d531-114">The data is stored as a **SAFEARRAY** of bytes (VT\_UI1 \| VT\_ARRAY).</span></span>

</dd> <dt>

<span data-ttu-id="2d531-115">*CB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2d531-115">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d531-116">Especifica el tamaño de los datos binarios, en bytes.</span><span class="sxs-lookup"><span data-stu-id="2d531-116">Specifies the size of the binary data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2d531-117">*prgbRegFilter2* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2d531-117">*prgbRegFilter2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d531-118">Dirección de una variable que recibe un puntero a los datos desempaquetados.</span><span class="sxs-lookup"><span data-stu-id="2d531-118">Address of a variable that receives a pointer to the unpacked data.</span></span> <span data-ttu-id="2d531-119">Cuando el método devuelve, convierte este puntero en un tipo [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) para tener acceso a los datos del filtro.</span><span class="sxs-lookup"><span data-stu-id="2d531-119">When the method returns, cast this pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) type to access the filter data.</span></span> <span data-ttu-id="2d531-120">El llamador debe liberar la memoria mediante una llamada al método **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="2d531-120">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d531-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2d531-121">Return value</span></span>

<span data-ttu-id="2d531-122">Si el método se ejecuta correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="2d531-122">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="2d531-123">Si se produce un error, devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="2d531-123">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d531-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2d531-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2d531-125">El encabezado Fil \_ Data. h se encuentra en el directorio de [ejemplo del asignador](mapper-sample.md) en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="2d531-125">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2d531-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d531-126">Requirements</span></span>



| <span data-ttu-id="2d531-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d531-127">Requirement</span></span> | <span data-ttu-id="2d531-128">Value</span><span class="sxs-lookup"><span data-stu-id="2d531-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d531-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d531-129">Header</span></span><br/> | <dl> <span data-ttu-id="2d531-130"><dt>Fil \_ Data. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d531-130"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="2d531-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2d531-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="2d531-132"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d531-132"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2d531-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d531-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d531-134">**Interfaz IAMFilterData**</span><span class="sxs-lookup"><span data-stu-id="2d531-134">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 





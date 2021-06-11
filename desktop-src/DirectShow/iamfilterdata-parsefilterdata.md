---
description: Obtenga información sobre el método IAMFilterData::P arseFilterData y desempaquete los datos binarios del Registro para un filtro. Esta interfaz está desusada.
ms.assetid: 86095fcf-3364-42a0-95db-08223fa3cc20
title: Método IAMFilterData::P arseFilterData (Fil \_ data.h)
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
ms.openlocfilehash: 9560280fa6f16699af907cdb5cf682b9c4bb1277
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989450"
---
# <a name="iamfilterdataparsefilterdata-method"></a><span data-ttu-id="2b2db-104">IAMFilterData::P arseFilterData (método)</span><span class="sxs-lookup"><span data-stu-id="2b2db-104">IAMFilterData::ParseFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="2b2db-105">Esta interfaz está desusada.</span><span class="sxs-lookup"><span data-stu-id="2b2db-105">This interface has been deprecated.</span></span> <span data-ttu-id="2b2db-106">Las nuevas aplicaciones no deben usarla.</span><span class="sxs-lookup"><span data-stu-id="2b2db-106">New applications should not use it.</span></span>

 

<span data-ttu-id="2b2db-107">El `ParseFilterData` método desempaquete los datos binarios del Registro para un filtro.</span><span class="sxs-lookup"><span data-stu-id="2b2db-107">The `ParseFilterData` method unpacks the binary registry data for a filter.</span></span>

<span data-ttu-id="2b2db-108">Normalmente no hay ninguna razón para que una aplicación llame a este método.</span><span class="sxs-lookup"><span data-stu-id="2b2db-108">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="2b2db-109">El [**método IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) proporciona una manera más cómoda de acceder a los datos del Registro de filtro.</span><span class="sxs-lookup"><span data-stu-id="2b2db-109">The [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method provides a more convenient way to access the filter registry data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b2db-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b2db-110">Syntax</span></span>


```C++
HRESULT ParseFilterData(
  [in]  BYTE  *rgbFilterData,
  [in]  ULONG cb,
  [out] BYTE  **prgbRegFilter2
);
```



## <a name="parameters"></a><span data-ttu-id="2b2db-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b2db-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b2db-112">*rgbFilterData* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2b2db-112">*rgbFilterData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b2db-113">Puntero a los datos binarios del Registro.</span><span class="sxs-lookup"><span data-stu-id="2b2db-113">Pointer to the binary registry data.</span></span> <span data-ttu-id="2b2db-114">Puede obtener estos datos recuperando la propiedad "FilterData" del moniker de filtro.</span><span class="sxs-lookup"><span data-stu-id="2b2db-114">You can get this data by retrieving the "FilterData" property from the filter moniker.</span></span> <span data-ttu-id="2b2db-115">Los datos se almacenan como **SAFEARRAY** de bytes (VT \_ UI1 \| VT \_ ARRAY).</span><span class="sxs-lookup"><span data-stu-id="2b2db-115">The data is stored as a **SAFEARRAY** of bytes (VT\_UI1 \| VT\_ARRAY).</span></span>

</dd> <dt>

<span data-ttu-id="2b2db-116">*cb* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2b2db-116">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b2db-117">Especifica el tamaño de los datos binarios, en bytes.</span><span class="sxs-lookup"><span data-stu-id="2b2db-117">Specifies the size of the binary data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2b2db-118">*prgbRegFilter2* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2b2db-118">*prgbRegFilter2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b2db-119">Dirección de una variable que recibe un puntero a los datos desempaquetados.</span><span class="sxs-lookup"><span data-stu-id="2b2db-119">Address of a variable that receives a pointer to the unpacked data.</span></span> <span data-ttu-id="2b2db-120">Cuando el método devuelve un resultado, convierte este puntero a un [**tipo REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) para tener acceso a los datos del filtro.</span><span class="sxs-lookup"><span data-stu-id="2b2db-120">When the method returns, cast this pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) type to access the filter data.</span></span> <span data-ttu-id="2b2db-121">El autor de la llamada debe liberar la memoria llamando al **método CoTaskMemFree.**</span><span class="sxs-lookup"><span data-stu-id="2b2db-121">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b2db-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b2db-122">Return value</span></span>

<span data-ttu-id="2b2db-123">Si el método se realiza correctamente, devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2b2db-123">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="2b2db-124">Si se produce un error, devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="2b2db-124">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b2db-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2b2db-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2b2db-126">El encabezado Fil \_ data.h se encuentra en el directorio [Ejemplo del](mapper-sample.md) asignador en la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="2b2db-126">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2b2db-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b2db-127">Requirements</span></span>



| <span data-ttu-id="2b2db-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b2db-128">Requirement</span></span> | <span data-ttu-id="2b2db-129">Value</span><span class="sxs-lookup"><span data-stu-id="2b2db-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b2db-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b2db-130">Header</span></span><br/> | <dl> <span data-ttu-id="2b2db-131"><dt>Fil \_ data.h</dt></span><span class="sxs-lookup"><span data-stu-id="2b2db-131"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="2b2db-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2b2db-132">DLL</span></span><br/>    | <dl> <span data-ttu-id="2b2db-133"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b2db-133"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2b2db-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b2db-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b2db-135">**IamFilterData (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="2b2db-135">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 





---
description: Obtenga información sobre el método IAMFilterData::CreateFilterData, que crea datos binarios del Registro para un filtro. Esta interfaz está desusada.
ms.assetid: ab6972ef-7c28-4cd1-b007-eb70f9aeb2cb
title: Método IAMFilterData::CreateFilterData (Fil \_ data.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.CreateFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 0a0126266fc33dca030abad65ccf9f0d35f6e195
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989460"
---
# <a name="iamfilterdatacreatefilterdata-method"></a><span data-ttu-id="3513b-104">IamFilterData::CreateFilterData (método)</span><span class="sxs-lookup"><span data-stu-id="3513b-104">IAMFilterData::CreateFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="3513b-105">Esta interfaz está desusada.</span><span class="sxs-lookup"><span data-stu-id="3513b-105">This interface has been deprecated.</span></span> <span data-ttu-id="3513b-106">Las nuevas aplicaciones no deben usarla.</span><span class="sxs-lookup"><span data-stu-id="3513b-106">New applications should not use it.</span></span>

 

<span data-ttu-id="3513b-107">El `CreateFilterData` método crea datos binarios del Registro para un filtro.</span><span class="sxs-lookup"><span data-stu-id="3513b-107">The `CreateFilterData` method creates binary registry data for a filter.</span></span> <span data-ttu-id="3513b-108">Estos datos se pueden escribir en el Registro como una subclave REG BINARY denominada FilterData, bajo la clave \_ CLSID del filtro.</span><span class="sxs-lookup"><span data-stu-id="3513b-108">This data can be written to the registry as a REG\_BINARY subkey named FilterData, under the filter's CLSID key.</span></span>

<span data-ttu-id="3513b-109">Normalmente no hay ninguna razón para que una aplicación llame a este método.</span><span class="sxs-lookup"><span data-stu-id="3513b-109">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="3513b-110">El [**método IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) crea automáticamente los datos binarios y los agrega a la ubicación correcta del Registro.</span><span class="sxs-lookup"><span data-stu-id="3513b-110">The [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method automatically creates the binary data and adds it to the correct location in the registry.</span></span> <span data-ttu-id="3513b-111">Para obtener más información, [vea Cómo registrar filtros de DirectShow.](how-to-register-directshow-filters.md)</span><span class="sxs-lookup"><span data-stu-id="3513b-111">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3513b-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3513b-112">Syntax</span></span>


```C++
HRESULT CreateFilterData(
  [in]  REGFILTER2 *prf2,
  [out] BYTE       **prgbFilterData,
  [out] ULONG      *pcb
);
```



## <a name="parameters"></a><span data-ttu-id="3513b-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3513b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3513b-114">*prf2* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="3513b-114">*prf2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3513b-115">Puntero a una [**estructura REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) que contiene la información del filtro.</span><span class="sxs-lookup"><span data-stu-id="3513b-115">Pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) structure that contains the filter information.</span></span>

</dd> <dt>

<span data-ttu-id="3513b-116">*prgbFilterData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3513b-116">*prgbFilterData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3513b-117">Dirección de una variable que recibe un puntero a los datos binarios.</span><span class="sxs-lookup"><span data-stu-id="3513b-117">Address of a variable that receives a pointer to the binary data.</span></span> <span data-ttu-id="3513b-118">El método asigna la memoria para los datos.</span><span class="sxs-lookup"><span data-stu-id="3513b-118">The method allocates the memory for the data.</span></span> <span data-ttu-id="3513b-119">El autor de la llamada debe liberar la memoria llamando al **método CoTaskMemFree.**</span><span class="sxs-lookup"><span data-stu-id="3513b-119">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> <dt>

<span data-ttu-id="3513b-120">*y* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3513b-120">*pcb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3513b-121">Puntero a una variable que recibe el tamaño de los datos binarios, en bytes.</span><span class="sxs-lookup"><span data-stu-id="3513b-121">Pointer to a variable that receives the size of the binary data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3513b-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3513b-122">Return value</span></span>

<span data-ttu-id="3513b-123">Si el método se realiza correctamente, devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3513b-123">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="3513b-124">Si se produce un error, devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="3513b-124">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3513b-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3513b-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3513b-126">El encabezado Fil \_ data.h se encuentra en el directorio [Ejemplo del](mapper-sample.md) asignador en la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="3513b-126">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3513b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3513b-127">Requirements</span></span>



| <span data-ttu-id="3513b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3513b-128">Requirement</span></span> | <span data-ttu-id="3513b-129">Value</span><span class="sxs-lookup"><span data-stu-id="3513b-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3513b-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3513b-130">Header</span></span><br/> | <dl> <span data-ttu-id="3513b-131"><dt>Fil \_ data.h</dt></span><span class="sxs-lookup"><span data-stu-id="3513b-131"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="3513b-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3513b-132">DLL</span></span><br/>    | <dl> <span data-ttu-id="3513b-133"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3513b-133"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3513b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="3513b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3513b-135">**IamFilterData (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="3513b-135">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 





---
description: 'Nota: esta interfaz está en desuso.'
ms.assetid: ab6972ef-7c28-4cd1-b007-eb70f9aeb2cb
title: 'IAMFilterData:: CreateFilterData (método) (Fil \_ Data. h)'
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
ms.openlocfilehash: 4c83f19de8e709f9890b23957f730fbbac12dd7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679394"
---
# <a name="iamfilterdatacreatefilterdata-method"></a><span data-ttu-id="5ae4a-103">IAMFilterData:: CreateFilterData (método)</span><span class="sxs-lookup"><span data-stu-id="5ae4a-103">IAMFilterData::CreateFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="5ae4a-104">Esta interfaz está desusada.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-104">This interface has been deprecated.</span></span> <span data-ttu-id="5ae4a-105">Las nuevas aplicaciones no deben utilizarla.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-105">New applications should not use it.</span></span>

 

<span data-ttu-id="5ae4a-106">El `CreateFilterData` método crea datos binarios del registro para un filtro.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-106">The `CreateFilterData` method creates binary registry data for a filter.</span></span> <span data-ttu-id="5ae4a-107">Estos datos se pueden escribir en el registro como una \_ subclave reg binaria denominada FilterData, en la clave CLSID del filtro.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-107">This data can be written to the registry as a REG\_BINARY subkey named FilterData, under the filter's CLSID key.</span></span>

<span data-ttu-id="5ae4a-108">Normalmente no hay ningún motivo para que una aplicación llame a este método.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-108">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="5ae4a-109">El método [**IFilterMapper2:: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) crea automáticamente los datos binarios y los agrega a la ubicación correcta en el registro.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-109">The [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method automatically creates the binary data and adds it to the correct location in the registry.</span></span> <span data-ttu-id="5ae4a-110">Para obtener más información, consulte [Cómo registrar filtros de DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="5ae4a-110">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5ae4a-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ae4a-111">Syntax</span></span>


```C++
HRESULT CreateFilterData(
  [in]  REGFILTER2 *prf2,
  [out] BYTE       **prgbFilterData,
  [out] ULONG      *pcb
);
```



## <a name="parameters"></a><span data-ttu-id="5ae4a-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ae4a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ae4a-113">*PRF2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5ae4a-113">*prf2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ae4a-114">Puntero a una estructura [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) que contiene la información del filtro.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-114">Pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) structure that contains the filter information.</span></span>

</dd> <dt>

<span data-ttu-id="5ae4a-115">*prgbFilterData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5ae4a-115">*prgbFilterData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ae4a-116">Dirección de una variable que recibe un puntero a los datos binarios.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-116">Address of a variable that receives a pointer to the binary data.</span></span> <span data-ttu-id="5ae4a-117">El método asigna la memoria para los datos.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-117">The method allocates the memory for the data.</span></span> <span data-ttu-id="5ae4a-118">El llamador debe liberar la memoria mediante una llamada al método **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="5ae4a-118">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> <dt>

<span data-ttu-id="5ae4a-119">*PCB* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5ae4a-119">*pcb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ae4a-120">Puntero a una variable que recibe el tamaño de los datos binarios, en bytes.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-120">Pointer to a variable that receives the size of the binary data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ae4a-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ae4a-121">Return value</span></span>

<span data-ttu-id="5ae4a-122">Si el método se ejecuta correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-122">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="5ae4a-123">Si se produce un error, devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-123">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ae4a-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ae4a-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5ae4a-125">El encabezado Fil \_ Data. h se encuentra en el directorio de [ejemplo del asignador](mapper-sample.md) en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="5ae4a-125">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5ae4a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ae4a-126">Requirements</span></span>



| <span data-ttu-id="5ae4a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ae4a-127">Requirement</span></span> | <span data-ttu-id="5ae4a-128">Value</span><span class="sxs-lookup"><span data-stu-id="5ae4a-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ae4a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ae4a-129">Header</span></span><br/> | <dl> <span data-ttu-id="5ae4a-130"><dt>Fil \_ Data. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ae4a-130"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="5ae4a-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5ae4a-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="5ae4a-132"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ae4a-132"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5ae4a-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ae4a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ae4a-134">**Interfaz IAMFilterData**</span><span class="sxs-lookup"><span data-stu-id="5ae4a-134">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 





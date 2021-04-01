---
title: IDeliveryOptimizationJob2 AddFile (método)
description: El método AddFile agrega un solo archivo a un trabajo existente.
keywords:
- AddFile (método)
- Método AddFile, interfaz IDeliveryOptimizationJob2
- Interfaz IDeliveryOptimizationJob2, método AddFile
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.AddFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8225db8cccb1e1d3bb364ba1dc29f30526fe36b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150076"
---
# <a name="ideliveryoptimizationjob2addfilewithranges-method"></a><span data-ttu-id="bea1c-106">IDeliveryOptimizationJob2:: AddFileWithRanges (método)</span><span class="sxs-lookup"><span data-stu-id="bea1c-106">IDeliveryOptimizationJob2::AddFileWithRanges method</span></span>

<span data-ttu-id="bea1c-107">El método AddFile agrega un solo archivo a un trabajo existente.</span><span class="sxs-lookup"><span data-stu-id="bea1c-107">The AddFile method adds a single file to an existing DO job.</span></span>

## <a name="syntax"></a><span data-ttu-id="bea1c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bea1c-108">Syntax</span></span>

```C++
HRESULT AddFile(
  [in]                              LPCWSTR       fileId,
  [in, unique]                      LPCWSTR       remoteUrl,
  [in]                              DWORD         rangeCount,
  [in, size_is(rangeCount), unique] BG_FILE_RANGE ranges[],
  [in]                              REFIID        riid,
  [out]                             void          **object
);
```

## <a name="parameters"></a><span data-ttu-id="bea1c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bea1c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bea1c-110">*fileid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bea1c-110">*fileId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bea1c-111">Cadena de identificador de archivo que identifica de forma única el archivo que se va a descargar.</span><span class="sxs-lookup"><span data-stu-id="bea1c-111">The file ID string, which uniquely identifies the file to be downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="bea1c-112">*remoteUrl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bea1c-112">*remoteUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bea1c-113">La dirección URL del archivo que intentará conectarse para descargar el archivo.</span><span class="sxs-lookup"><span data-stu-id="bea1c-113">The file URL that DO will attempt to connect to download the file.</span></span>

</dd> <dt>

<span data-ttu-id="bea1c-114">*rangeCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bea1c-114">*rangeCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bea1c-115">Número de elementos contenidos en *rangos*.</span><span class="sxs-lookup"><span data-stu-id="bea1c-115">The number of items contained in *ranges*.</span></span> <span data-ttu-id="bea1c-116">Un valor cero significa que no se utiliza ningún intervalo para el archivo.</span><span class="sxs-lookup"><span data-stu-id="bea1c-116">A zero value means that no ranges are used for the file.</span></span>

</dd> <dt>

<span data-ttu-id="bea1c-117">*intervalos* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="bea1c-117">*ranges* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bea1c-118">La lista de intervalos opcional.</span><span class="sxs-lookup"><span data-stu-id="bea1c-118">The optional range list.</span></span> <span data-ttu-id="bea1c-119">Cada intervalo de la lista es una estructura de [**BG_FILE_RANGE**](bg-file-range.md) .</span><span class="sxs-lookup"><span data-stu-id="bea1c-119">Each range in the list is a [**BG_FILE_RANGE**](bg-file-range.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="bea1c-120">*riid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bea1c-120">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bea1c-121">El tipo de objeto contenido en el objeto.</span><span class="sxs-lookup"><span data-stu-id="bea1c-121">The type of object contained in object.</span></span> <span data-ttu-id="bea1c-122">Debe ser de tipo IID_IDeliveryOptimizationFile.</span><span class="sxs-lookup"><span data-stu-id="bea1c-122">This must by of type IID_IDeliveryOptimizationFile.</span></span>

</dd> <dt>

<span data-ttu-id="bea1c-123">*objeto* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bea1c-123">*object* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bea1c-124">El objeto IDeliveryOptimizationFile, que representa el archivo de descarga.</span><span class="sxs-lookup"><span data-stu-id="bea1c-124">The IDeliveryOptimizationFile object, which represents the download file.</span></span> 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bea1c-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bea1c-125">Return value</span></span>

<span data-ttu-id="bea1c-126">Este método devuelve S_OK si se realiza correctamente o uno de los valores HRESULT estándar en caso de error.</span><span class="sxs-lookup"><span data-stu-id="bea1c-126">This method returns S_OK on success or one of the standard HRESULT values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="bea1c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bea1c-127">Requirements</span></span>

| <span data-ttu-id="bea1c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="bea1c-128">Requirement</span></span> | <span data-ttu-id="bea1c-129">Value</span><span class="sxs-lookup"><span data-stu-id="bea1c-129">Value</span></span> |
|---------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="bea1c-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bea1c-130">Minimum supported client</span></span>  | <span data-ttu-id="bea1c-131">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="bea1c-131">Windows 10, version 1803 \[desktop apps only\]</span></span>                                  |
| <span data-ttu-id="bea1c-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bea1c-132">Minimum supported server</span></span>  | <span data-ttu-id="bea1c-133">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="bea1c-133">Windows Server, version 1709 \[desktop apps only\]</span></span>                              |
| <span data-ttu-id="bea1c-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bea1c-134">Header</span></span>                    | <span data-ttu-id="bea1c-135">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="bea1c-135">Deliveryoptimization.h</span></span>                                                          |
| <span data-ttu-id="bea1c-136">IDL</span><span class="sxs-lookup"><span data-stu-id="bea1c-136">IDL</span></span>                       | <span data-ttu-id="bea1c-137">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="bea1c-137">DeliveryOptimization.idl</span></span>                                                        |
| <span data-ttu-id="bea1c-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bea1c-138">Library</span></span>                   | <span data-ttu-id="bea1c-139">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="bea1c-139">Dosvc.lib</span></span>                                                                       |
| <span data-ttu-id="bea1c-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bea1c-140">DLL</span></span>                       | <span data-ttu-id="bea1c-141">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="bea1c-141">Dosvc.dll</span></span>                                                                       |
| <span data-ttu-id="bea1c-142">IID</span><span class="sxs-lookup"><span data-stu-id="bea1c-142">IID</span></span>                       | <span data-ttu-id="bea1c-143">IID_IDeliveryOptimizationJob se define como EE2584CF-A69C-4848-B633-2649962B3EF7</span><span class="sxs-lookup"><span data-stu-id="bea1c-143">IID_IDeliveryOptimizationJob is defined as EE2584CF-A69C-4848-B633-2649962B3EF7</span></span> |

## <a name="see-also"></a><span data-ttu-id="bea1c-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="bea1c-144">See also</span></span>

[<span data-ttu-id="bea1c-145">**IDeliveryOptimizationJob2**</span><span class="sxs-lookup"><span data-stu-id="bea1c-145">**IDeliveryOptimizationJob2**</span></span>](ideliveryoptimizationjob2.md)

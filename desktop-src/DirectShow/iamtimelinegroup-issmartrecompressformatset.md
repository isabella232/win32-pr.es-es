---
description: El método IsSmartRecompressFormatSet determina si se ha establecido un formato de recompresión inteligente para el grupo.
ms.assetid: d2b7ecc7-2348-402d-8d96-e0922e06a685
title: 'IAMTimelineGroup:: IsSmartRecompressFormatSet (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.IsSmartRecompressFormatSet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 078649fd42cd44596ff27558b29d14b6f8cbeddc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680303"
---
# <a name="iamtimelinegroupissmartrecompressformatset-method"></a><span data-ttu-id="d4cb4-103">IAMTimelineGroup:: IsSmartRecompressFormatSet (método)</span><span class="sxs-lookup"><span data-stu-id="d4cb4-103">IAMTimelineGroup::IsSmartRecompressFormatSet method</span></span>

> [!Note]  
> <span data-ttu-id="d4cb4-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="d4cb4-104">\[Deprecated.</span></span> <span data-ttu-id="d4cb4-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d4cb4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d4cb4-106">El `IsSmartRecompressFormatSet` método determina si se ha establecido un formato de recompresión inteligente para el grupo.</span><span class="sxs-lookup"><span data-stu-id="d4cb4-106">The `IsSmartRecompressFormatSet` method determines whether a smart recompression format was set for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4cb4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4cb4-107">Syntax</span></span>


```C++
HRESULT IsSmartRecompressFormatSet(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="d4cb4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d4cb4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4cb4-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="d4cb4-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="d4cb4-110">Recibe un valor booleano que indica si se ha establecido un formato de compresión.</span><span class="sxs-lookup"><span data-stu-id="d4cb4-110">Receives a Boolean value indicating whether a compression format was set.</span></span> <span data-ttu-id="d4cb4-111">Si **es true**, se ha establecido un formato de compresión.</span><span class="sxs-lookup"><span data-stu-id="d4cb4-111">If **TRUE**, a compression format was set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4cb4-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4cb4-112">Return value</span></span>

<span data-ttu-id="d4cb4-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d4cb4-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d4cb4-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d4cb4-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4cb4-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4cb4-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d4cb4-116">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="d4cb4-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d4cb4-117">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d4cb4-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d4cb4-118">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d4cb4-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d4cb4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4cb4-119">Requirements</span></span>



| <span data-ttu-id="d4cb4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4cb4-120">Requirement</span></span> | <span data-ttu-id="d4cb4-121">Value</span><span class="sxs-lookup"><span data-stu-id="d4cb4-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4cb4-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4cb4-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d4cb4-123"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4cb4-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d4cb4-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d4cb4-124">Library</span></span><br/> | <dl> <span data-ttu-id="d4cb4-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4cb4-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4cb4-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4cb4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4cb4-127">**Interfaz IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="d4cb4-127">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="d4cb4-128">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="d4cb4-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





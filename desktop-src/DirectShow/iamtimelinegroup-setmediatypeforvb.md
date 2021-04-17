---
description: El método SetMediaTypeForVB especifica el tipo de medio de grupo para los clientes de automatización.
ms.assetid: 86f52088-a0dd-40be-98a0-8adc09b264dd
title: 'IAMTimelineGroup:: SetMediaTypeForVB (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaTypeForVB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1371b1d6c906666ca30e5df2d26dbe20eddf1745
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690792"
---
# <a name="iamtimelinegroupsetmediatypeforvb-method"></a><span data-ttu-id="7de7c-103">IAMTimelineGroup:: SetMediaTypeForVB (método)</span><span class="sxs-lookup"><span data-stu-id="7de7c-103">IAMTimelineGroup::SetMediaTypeForVB method</span></span>

> [!Note]  
> <span data-ttu-id="7de7c-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="7de7c-104">\[Deprecated.</span></span> <span data-ttu-id="7de7c-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7de7c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7de7c-106">El `SetMediaTypeForVB` método especifica el tipo de medio de grupo para los clientes de automatización.</span><span class="sxs-lookup"><span data-stu-id="7de7c-106">The `SetMediaTypeForVB` method specifies the group media type, for Automation clients.</span></span>

## <a name="syntax"></a><span data-ttu-id="7de7c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7de7c-107">Syntax</span></span>


```C++
HRESULT SetMediaTypeForVB(
  [in] long Val
);
```



## <a name="parameters"></a><span data-ttu-id="7de7c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7de7c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7de7c-109">*Val* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7de7c-109">*Val* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7de7c-110">Valor que especifica el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="7de7c-110">Value that specifies the media type.</span></span> <span data-ttu-id="7de7c-111">Establezca el valor en 0 para vídeo, o en 1 para audio.</span><span class="sxs-lookup"><span data-stu-id="7de7c-111">Set the value to 0 for video, or 1 for audio.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7de7c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7de7c-112">Return value</span></span>

<span data-ttu-id="7de7c-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="7de7c-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7de7c-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7de7c-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7de7c-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7de7c-115">Remarks</span></span>

<span data-ttu-id="7de7c-116">Este método está destinado a los clientes de automatización.</span><span class="sxs-lookup"><span data-stu-id="7de7c-116">This method is intended for Automation clients.</span></span> <span data-ttu-id="7de7c-117">En el caso de las aplicaciones de C++, utilice el método [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="7de7c-117">For C++ applications, use the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="7de7c-118">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="7de7c-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7de7c-119">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7de7c-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7de7c-120">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7de7c-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7de7c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7de7c-121">Requirements</span></span>



| <span data-ttu-id="7de7c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7de7c-122">Requirement</span></span> | <span data-ttu-id="7de7c-123">Value</span><span class="sxs-lookup"><span data-stu-id="7de7c-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7de7c-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7de7c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7de7c-125"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="7de7c-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7de7c-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7de7c-126">Library</span></span><br/> | <dl> <span data-ttu-id="7de7c-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7de7c-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7de7c-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="7de7c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7de7c-129">**Interfaz IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="7de7c-129">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="7de7c-130">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="7de7c-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





---
description: 'El método SetMediaLength2 especifica la duración del archivo de código fuente. Este método es equivalente a IAMTimelineSrc:: SetMediaLength, pero toma un valor REFTIME.'
ms.assetid: 1a1dcf23-2041-4791-bce7-0ecbe33df592
title: 'IAMTimelineSrc:: SetMediaLength2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4deb42cdd917fe7d79a420b15247b4bdf5ee52bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680570"
---
# <a name="iamtimelinesrcsetmedialength2-method"></a><span data-ttu-id="9595f-104">IAMTimelineSrc:: SetMediaLength2 (método)</span><span class="sxs-lookup"><span data-stu-id="9595f-104">IAMTimelineSrc::SetMediaLength2 method</span></span>

> [!Note]  
> <span data-ttu-id="9595f-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="9595f-105">\[Deprecated.</span></span> <span data-ttu-id="9595f-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9595f-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9595f-107">El `SetMediaLength2` método especifica la duración del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="9595f-107">The `SetMediaLength2` method specifies the duration of the source file.</span></span> <span data-ttu-id="9595f-108">Este método es equivalente a [**IAMTimelineSrc:: SetMediaLength**](iamtimelinesrc-setmedialength.md), pero toma un valor [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="9595f-108">This method is equivalent to [**IAMTimelineSrc::SetMediaLength**](iamtimelinesrc-setmedialength.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="9595f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9595f-109">Syntax</span></span>


```C++
HRESULT SetMediaLength2(
   REFTIME Length
);
```



## <a name="parameters"></a><span data-ttu-id="9595f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9595f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9595f-111">*Duración*</span><span class="sxs-lookup"><span data-stu-id="9595f-111">*Length*</span></span> 
</dt> <dd>

<span data-ttu-id="9595f-112">Longitud del medio, en segundos.</span><span class="sxs-lookup"><span data-stu-id="9595f-112">Media length, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9595f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9595f-113">Return value</span></span>

<span data-ttu-id="9595f-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9595f-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9595f-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9595f-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9595f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9595f-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9595f-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="9595f-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9595f-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9595f-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9595f-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9595f-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9595f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9595f-120">Requirements</span></span>



| <span data-ttu-id="9595f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9595f-121">Requirement</span></span> | <span data-ttu-id="9595f-122">Value</span><span class="sxs-lookup"><span data-stu-id="9595f-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9595f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9595f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9595f-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="9595f-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9595f-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9595f-125">Library</span></span><br/> | <dl> <span data-ttu-id="9595f-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9595f-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9595f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9595f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9595f-128">**Interfaz IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="9595f-128">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="9595f-129">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="9595f-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





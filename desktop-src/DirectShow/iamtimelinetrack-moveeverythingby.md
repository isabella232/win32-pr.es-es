---
description: 'Método IAMTimelineTrack::MoveEverythingBy: este método no se admite.'
ms.assetid: f263116b-e492-4468-9829-124a096c9d74
title: Método IAMTimelineTrack::MoveEverythingBy (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.MoveEverythingBy
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fe85cf17c92c0809189e12e8ad40ceb1d1f3fd25
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094593"
---
# <a name="iamtimelinetrackmoveeverythingby-method"></a><span data-ttu-id="576d1-103">IamTimelineTrack::MoveEverythingBy (método)</span><span class="sxs-lookup"><span data-stu-id="576d1-103">IAMTimelineTrack::MoveEverythingBy method</span></span>

<span data-ttu-id="576d1-104">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="576d1-104">This method is not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="576d1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="576d1-105">Syntax</span></span>


```C++
HRESULT MoveEverythingBy(
   REFERENCE_TIME Start,
   REFERENCE_TIME MoveBy
);
```



## <a name="parameters"></a><span data-ttu-id="576d1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="576d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="576d1-107">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="576d1-107">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="576d1-108">Reservado.</span><span class="sxs-lookup"><span data-stu-id="576d1-108">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="576d1-109">*MoveBy*</span><span class="sxs-lookup"><span data-stu-id="576d1-109">*MoveBy*</span></span> 
</dt> <dd>

<span data-ttu-id="576d1-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="576d1-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="576d1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="576d1-111">Return value</span></span>

<span data-ttu-id="576d1-112">Si este método se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="576d1-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="576d1-113">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="576d1-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="576d1-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="576d1-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="576d1-115">El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="576d1-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="576d1-116">Para obtener Qedit.h, descargue Microsoft Windows SDK [Update para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="576d1-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="576d1-117">Qedit.h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3.5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="576d1-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="576d1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="576d1-118">Requirements</span></span>



| <span data-ttu-id="576d1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="576d1-119">Requirement</span></span> | <span data-ttu-id="576d1-120">Value</span><span class="sxs-lookup"><span data-stu-id="576d1-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="576d1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="576d1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="576d1-122"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="576d1-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="576d1-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="576d1-123">Library</span></span><br/> | <dl> <span data-ttu-id="576d1-124"><dt>Strmiids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="576d1-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="576d1-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="576d1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="576d1-126">**IamTimelineTrack (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="576d1-126">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> </dl>

 

 





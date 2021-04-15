---
description: No se admite este método.
ms.assetid: f263116b-e492-4468-9829-124a096c9d74
title: 'IAMTimelineTrack:: MoveEverythingBy (método) (QEDIT. h)'
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
ms.openlocfilehash: 4eded92548c047e6d5102e603a5ab0554bd1f4fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690115"
---
# <a name="iamtimelinetrackmoveeverythingby-method"></a><span data-ttu-id="67bde-103">IAMTimelineTrack:: MoveEverythingBy (método)</span><span class="sxs-lookup"><span data-stu-id="67bde-103">IAMTimelineTrack::MoveEverythingBy method</span></span>

<span data-ttu-id="67bde-104">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="67bde-104">This method is not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="67bde-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67bde-105">Syntax</span></span>


```C++
HRESULT MoveEverythingBy(
   REFERENCE_TIME Start,
   REFERENCE_TIME MoveBy
);
```



## <a name="parameters"></a><span data-ttu-id="67bde-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67bde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67bde-107">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="67bde-107">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="67bde-108">Reservado.</span><span class="sxs-lookup"><span data-stu-id="67bde-108">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="67bde-109">*MoveBy*</span><span class="sxs-lookup"><span data-stu-id="67bde-109">*MoveBy*</span></span> 
</dt> <dd>

<span data-ttu-id="67bde-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="67bde-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67bde-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67bde-111">Return value</span></span>

<span data-ttu-id="67bde-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="67bde-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="67bde-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="67bde-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="67bde-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67bde-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="67bde-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="67bde-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="67bde-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="67bde-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="67bde-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="67bde-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="67bde-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67bde-118">Requirements</span></span>



| <span data-ttu-id="67bde-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="67bde-119">Requirement</span></span> | <span data-ttu-id="67bde-120">Value</span><span class="sxs-lookup"><span data-stu-id="67bde-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67bde-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67bde-121">Header</span></span><br/>  | <dl> <span data-ttu-id="67bde-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="67bde-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="67bde-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="67bde-123">Library</span></span><br/> | <dl> <span data-ttu-id="67bde-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67bde-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67bde-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="67bde-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67bde-126">**Interfaz IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="67bde-126">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> </dl>

 

 





---
description: El método AreYouBlank determina si la pista está en blanco (no contiene objetos de origen).
ms.assetid: 05d02753-6e40-4307-9445-c3cbc835f75e
title: 'IAMTimelineTrack:: AreYouBlank (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.AreYouBlank
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 289fac360f989504d3eb5108f8c2388ac4a06b09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690077"
---
# <a name="iamtimelinetrackareyoublank-method"></a><span data-ttu-id="42c57-103">IAMTimelineTrack:: AreYouBlank (método)</span><span class="sxs-lookup"><span data-stu-id="42c57-103">IAMTimelineTrack::AreYouBlank method</span></span>

> [!Note]  
> <span data-ttu-id="42c57-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="42c57-104">\[Deprecated.</span></span> <span data-ttu-id="42c57-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="42c57-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="42c57-106">El `AreYouBlank` método determina si la pista está en blanco (no contiene objetos de origen).</span><span class="sxs-lookup"><span data-stu-id="42c57-106">The `AreYouBlank` method determines whether the track is blank (contains no source objects).</span></span>

## <a name="syntax"></a><span data-ttu-id="42c57-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42c57-107">Syntax</span></span>


```C++
HRESULT AreYouBlank(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="42c57-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42c57-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42c57-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="42c57-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="42c57-110">Recibe un valor booleano que especifica si la pista está en blanco.</span><span class="sxs-lookup"><span data-stu-id="42c57-110">Receives a Boolean value specifying whether the track is blank.</span></span> <span data-ttu-id="42c57-111">Si el valor es **true**, la pista está en blanco y no contiene ningún objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="42c57-111">If the value is **TRUE**, the track is blank and contains no source objects.</span></span> <span data-ttu-id="42c57-112">Si es **false**, la pista no está en blanco.</span><span class="sxs-lookup"><span data-stu-id="42c57-112">If **FALSE**, the track is not blank.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42c57-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42c57-113">Return value</span></span>

<span data-ttu-id="42c57-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="42c57-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="42c57-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="42c57-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="42c57-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42c57-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="42c57-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="42c57-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="42c57-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="42c57-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="42c57-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="42c57-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="42c57-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42c57-120">Requirements</span></span>



| <span data-ttu-id="42c57-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="42c57-121">Requirement</span></span> | <span data-ttu-id="42c57-122">Value</span><span class="sxs-lookup"><span data-stu-id="42c57-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42c57-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42c57-123">Header</span></span><br/>  | <dl> <span data-ttu-id="42c57-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="42c57-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="42c57-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="42c57-125">Library</span></span><br/> | <dl> <span data-ttu-id="42c57-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42c57-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42c57-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="42c57-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42c57-128">**Interfaz IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="42c57-128">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="42c57-129">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="42c57-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





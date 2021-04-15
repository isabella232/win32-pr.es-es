---
description: 'El método SetDefaultTransitionB establece la transición predeterminada. Este método es equivalente a IAMTimeline:: SetDefaultTransition, pero toma un valor BSTR, en lugar de un puntero a un GUID.'
ms.assetid: 1998fd31-2ab8-477e-89ee-93ca92dc10ec
title: 'IAMTimeline:: SetDefaultTransitionB (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultTransitionB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 221491dd0be97f1808e469d956c189bf61458278
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690046"
---
# <a name="iamtimelinesetdefaulttransitionb-method"></a><span data-ttu-id="de3e9-104">IAMTimeline:: SetDefaultTransitionB (método)</span><span class="sxs-lookup"><span data-stu-id="de3e9-104">IAMTimeline::SetDefaultTransitionB method</span></span>

> [!Note]  
> <span data-ttu-id="de3e9-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="de3e9-105">\[Deprecated.</span></span> <span data-ttu-id="de3e9-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="de3e9-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="de3e9-107">El `SetDefaultTransitionB` método establece la transición predeterminada.</span><span class="sxs-lookup"><span data-stu-id="de3e9-107">The `SetDefaultTransitionB` method sets the default transition.</span></span> <span data-ttu-id="de3e9-108">Este método es equivalente a [**IAMTimeline:: SetDefaultTransition**](iamtimeline-setdefaulttransition.md), pero toma un valor BSTR, en lugar de un puntero a un GUID.</span><span class="sxs-lookup"><span data-stu-id="de3e9-108">This method is equivalent to [**IAMTimeline::SetDefaultTransition**](iamtimeline-setdefaulttransition.md), but takes a BSTR value, rather than a pointer to a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="de3e9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de3e9-109">Syntax</span></span>


```C++
HRESULT SetDefaultTransitionB(
   BSTR pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="de3e9-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de3e9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de3e9-111">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="de3e9-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="de3e9-112">Valor BSTR que representa el GUID de la transición predeterminada.</span><span class="sxs-lookup"><span data-stu-id="de3e9-112">BSTR value representing the GUID of the default transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de3e9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de3e9-113">Return value</span></span>

<span data-ttu-id="de3e9-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="de3e9-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="de3e9-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="de3e9-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="de3e9-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de3e9-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="de3e9-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="de3e9-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="de3e9-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="de3e9-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="de3e9-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="de3e9-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="de3e9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de3e9-120">Requirements</span></span>



| <span data-ttu-id="de3e9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="de3e9-121">Requirement</span></span> | <span data-ttu-id="de3e9-122">Value</span><span class="sxs-lookup"><span data-stu-id="de3e9-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de3e9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de3e9-123">Header</span></span><br/>  | <dl> <span data-ttu-id="de3e9-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="de3e9-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="de3e9-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="de3e9-125">Library</span></span><br/> | <dl> <span data-ttu-id="de3e9-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de3e9-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de3e9-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="de3e9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de3e9-128">**Interfaz IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="de3e9-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="de3e9-129">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="de3e9-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





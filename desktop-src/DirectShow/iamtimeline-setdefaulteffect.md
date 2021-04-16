---
description: El método SetDefaultEffect establece el efecto predeterminado. Si el motor de representación no puede representar un efecto, sustituye el efecto predeterminado.
ms.assetid: 6ee94d86-c27f-4378-9a10-f3993a3ae657
title: 'IAMTimeline:: SetDefaultEffect (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 33e23070a7bb10dd040d08c145bfe1e0111026d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690253"
---
# <a name="iamtimelinesetdefaulteffect-method"></a><span data-ttu-id="c0390-104">IAMTimeline:: SetDefaultEffect (método)</span><span class="sxs-lookup"><span data-stu-id="c0390-104">IAMTimeline::SetDefaultEffect method</span></span>

> [!Note]  
> <span data-ttu-id="c0390-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="c0390-105">\[Deprecated.</span></span> <span data-ttu-id="c0390-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c0390-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c0390-107">El `SetDefaultEffect` método establece el efecto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c0390-107">The `SetDefaultEffect` method sets the default effect.</span></span> <span data-ttu-id="c0390-108">Si el motor de representación no puede representar un efecto, sustituye el efecto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c0390-108">If the render engine cannot render an effect, it substitutes the default effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0390-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0390-109">Syntax</span></span>


```C++
HRESULT SetDefaultEffect(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="c0390-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c0390-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0390-111">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="c0390-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="c0390-112">Puntero al GUID del efecto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c0390-112">Pointer to the GUID of the default effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0390-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0390-113">Return value</span></span>

<span data-ttu-id="c0390-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c0390-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c0390-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c0390-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0390-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c0390-116">Remarks</span></span>

<span data-ttu-id="c0390-117">Si no establece un efecto predeterminado, o si el efecto que se especifica como predeterminado produce un error, DES utiliza su propio efecto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c0390-117">If you do not set a default effect, or if the effect that you specify as a default causes an error, DES uses its own default effect.</span></span>

> [!Note]  
> <span data-ttu-id="c0390-118">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="c0390-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c0390-119">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c0390-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c0390-120">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c0390-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c0390-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0390-121">Requirements</span></span>



| <span data-ttu-id="c0390-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0390-122">Requirement</span></span> | <span data-ttu-id="c0390-123">Value</span><span class="sxs-lookup"><span data-stu-id="c0390-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0390-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c0390-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c0390-125"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0390-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c0390-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c0390-126">Library</span></span><br/> | <dl> <span data-ttu-id="c0390-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0390-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0390-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0390-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0390-129">**Interfaz IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="c0390-129">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="c0390-130">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="c0390-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





---
description: El método IsNormalRate indica si el clip se reproducirá a la velocidad de reproducción normal; es decir, la velocidad de reproducción del archivo original.
ms.assetid: 4a8fe415-f9eb-450d-9a75-e528577050d9
title: 'IAMTimelineSrc:: IsNormalRate (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.IsNormalRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e368efcf29d836cc23fa60ed34dae1a172978f77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690939"
---
# <a name="iamtimelinesrcisnormalrate-method"></a><span data-ttu-id="bb5ef-103">IAMTimelineSrc:: IsNormalRate (método)</span><span class="sxs-lookup"><span data-stu-id="bb5ef-103">IAMTimelineSrc::IsNormalRate method</span></span>

> [!Note]  
> <span data-ttu-id="bb5ef-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="bb5ef-104">\[Deprecated.</span></span> <span data-ttu-id="bb5ef-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bb5ef-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bb5ef-106">El `IsNormalRate` método indica si el clip se reproducirá con la velocidad de reproducción normal; es decir, la velocidad de reproducción del archivo original.</span><span class="sxs-lookup"><span data-stu-id="bb5ef-106">The `IsNormalRate` method indicates whether the clip will play at the normal playback rate; that is, the playback rate of the original file.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb5ef-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb5ef-107">Syntax</span></span>


```C++
HRESULT IsNormalRate(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="bb5ef-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb5ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb5ef-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="bb5ef-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="bb5ef-110">Recibe un valor booleano que indica cómo se representará el clip.</span><span class="sxs-lookup"><span data-stu-id="bb5ef-110">Receives a Boolean value indicating how the clip will render.</span></span> <span data-ttu-id="bb5ef-111">Si el valor es **true**, el clip se reproducirá a la tarifa normal.</span><span class="sxs-lookup"><span data-stu-id="bb5ef-111">If the value is **TRUE**, the clip will play at the normal rate.</span></span> <span data-ttu-id="bb5ef-112">De lo contrario, se reproducirá más rápido o más lento de lo normal.</span><span class="sxs-lookup"><span data-stu-id="bb5ef-112">Otherwise, it will play faster or slower than normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb5ef-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb5ef-113">Return value</span></span>

<span data-ttu-id="bb5ef-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="bb5ef-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bb5ef-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bb5ef-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb5ef-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb5ef-116">Remarks</span></span>

<span data-ttu-id="bb5ef-117">La velocidad de reproducción de un clip viene determinada por las horas de inicio y detención del medio, en relación con las horas de la escala de tiempo:</span><span class="sxs-lookup"><span data-stu-id="bb5ef-117">A clip's playback rate is determined by its media start and stop times, relative to its timeline times:</span></span>


```C++
Playback rate = (Media Stop <entity type="mdash"/> Media Start) / (Timeline Stop <entity type="mdash"/> Timeline Start)
```



<span data-ttu-id="bb5ef-118">Si esta relación es igual a 1, el clip se reproduce a la velocidad creada.</span><span class="sxs-lookup"><span data-stu-id="bb5ef-118">If this ratio is equal to 1, the clip plays at the authored speed.</span></span> <span data-ttu-id="bb5ef-119">De lo contrario, se reproducirá más rápido o más lento.</span><span class="sxs-lookup"><span data-stu-id="bb5ef-119">Otherwise, it plays faster or slower.</span></span> <span data-ttu-id="bb5ef-120">Para obtener más información, vea [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="bb5ef-120">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="bb5ef-121">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="bb5ef-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bb5ef-122">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bb5ef-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bb5ef-123">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="bb5ef-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bb5ef-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb5ef-124">Requirements</span></span>



| <span data-ttu-id="bb5ef-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb5ef-125">Requirement</span></span> | <span data-ttu-id="bb5ef-126">Value</span><span class="sxs-lookup"><span data-stu-id="bb5ef-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb5ef-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb5ef-127">Header</span></span><br/>  | <dl> <span data-ttu-id="bb5ef-128"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb5ef-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bb5ef-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bb5ef-129">Library</span></span><br/> | <dl> <span data-ttu-id="bb5ef-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb5ef-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb5ef-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb5ef-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb5ef-132">**Interfaz IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="bb5ef-132">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="bb5ef-133">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="bb5ef-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





---
description: El método EffectsEnabled determina si se habilitan los efectos. Si los efectos están deshabilitados, permanecen en la escala de tiempo pero no se representan.
ms.assetid: fd8bb2aa-9c10-4a85-9e9d-1b342fbce03b
title: 'IAMTimeline:: EffectsEnabled (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EffectsEnabled
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d988e8a4c10dc6dba52269c6729b8d7fea1f090e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653517"
---
# <a name="iamtimelineeffectsenabled-method"></a><span data-ttu-id="13bd1-104">IAMTimeline:: EffectsEnabled (método)</span><span class="sxs-lookup"><span data-stu-id="13bd1-104">IAMTimeline::EffectsEnabled method</span></span>

> [!Note]  
> <span data-ttu-id="13bd1-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="13bd1-105">\[Deprecated.</span></span> <span data-ttu-id="13bd1-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="13bd1-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="13bd1-107">El `EffectsEnabled` método determina si se habilitan los efectos.</span><span class="sxs-lookup"><span data-stu-id="13bd1-107">The `EffectsEnabled` method determines whether effects are enabled.</span></span> <span data-ttu-id="13bd1-108">Si los efectos están deshabilitados, permanecen en la escala de tiempo pero no se representan.</span><span class="sxs-lookup"><span data-stu-id="13bd1-108">If effects are disabled, they remain in the timeline but are not rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="13bd1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13bd1-109">Syntax</span></span>


```C++
HRESULT EffectsEnabled(
   BOOL *pfEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="13bd1-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13bd1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13bd1-111">*pfEnabled*</span><span class="sxs-lookup"><span data-stu-id="13bd1-111">*pfEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="13bd1-112">Recibe un valor booleano que indica si se habilitan los efectos.</span><span class="sxs-lookup"><span data-stu-id="13bd1-112">Receives a Boolean value indicating whether effects are enabled.</span></span> <span data-ttu-id="13bd1-113">Si **es true**, se habilitan los efectos.</span><span class="sxs-lookup"><span data-stu-id="13bd1-113">If **TRUE**, effects are enabled.</span></span> <span data-ttu-id="13bd1-114">Si **es false**, los efectos están deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="13bd1-114">If **FALSE**, effects are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13bd1-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13bd1-115">Return value</span></span>

<span data-ttu-id="13bd1-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="13bd1-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="13bd1-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="13bd1-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="13bd1-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13bd1-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="13bd1-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="13bd1-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="13bd1-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="13bd1-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="13bd1-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="13bd1-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="13bd1-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13bd1-122">Requirements</span></span>



| <span data-ttu-id="13bd1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="13bd1-123">Requirement</span></span> | <span data-ttu-id="13bd1-124">Value</span><span class="sxs-lookup"><span data-stu-id="13bd1-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13bd1-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13bd1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="13bd1-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="13bd1-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="13bd1-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="13bd1-127">Library</span></span><br/> | <dl> <span data-ttu-id="13bd1-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13bd1-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13bd1-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="13bd1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13bd1-130">**Interfaz IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="13bd1-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="13bd1-131">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="13bd1-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





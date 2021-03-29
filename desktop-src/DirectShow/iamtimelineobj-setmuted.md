---
description: El método SetMuted establece el estado silenciado del objeto. Un objeto silenciado no se representa, pero permanece en la escala de tiempo.
ms.assetid: 5dcd8533-8e58-4553-ac01-928723485f5d
title: 'IAMTimelineObj:: SetMuted (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetMuted
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac3f5b798ef56251fa64b55a92ae1e94e2fd61b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680727"
---
# <a name="iamtimelineobjsetmuted-method"></a><span data-ttu-id="b089f-104">IAMTimelineObj:: SetMuted (método)</span><span class="sxs-lookup"><span data-stu-id="b089f-104">IAMTimelineObj::SetMuted method</span></span>

> [!Note]  
> <span data-ttu-id="b089f-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="b089f-105">\[Deprecated.</span></span> <span data-ttu-id="b089f-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b089f-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b089f-107">El `SetMuted` método establece el estado silenciado del objeto.</span><span class="sxs-lookup"><span data-stu-id="b089f-107">The `SetMuted` method sets the object's muted state.</span></span> <span data-ttu-id="b089f-108">Un objeto silenciado no se representa, pero permanece en la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="b089f-108">A muted object is not rendered, but it remains in the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="b089f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b089f-109">Syntax</span></span>


```C++
HRESULT SetMuted(
   BOOL newVal
);
```



## <a name="parameters"></a><span data-ttu-id="b089f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b089f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b089f-111">*newVal*</span><span class="sxs-lookup"><span data-stu-id="b089f-111">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="b089f-112">Marca que especifica el estado silenciado.</span><span class="sxs-lookup"><span data-stu-id="b089f-112">Flag that specifies the muted state.</span></span> <span data-ttu-id="b089f-113">Si **es true**, se silencia el objeto y todos sus elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="b089f-113">If **TRUE**, the object and all of its children are muted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b089f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b089f-114">Return value</span></span>

<span data-ttu-id="b089f-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="b089f-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b089f-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b089f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b089f-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b089f-117">Remarks</span></span>

<span data-ttu-id="b089f-118">Silenciar un objeto también silencia los elementos secundarios contenidos en el objeto.</span><span class="sxs-lookup"><span data-stu-id="b089f-118">Muting an object also mutes any children contained in the object.</span></span> <span data-ttu-id="b089f-119">Por ejemplo, si silencia una pista, las transiciones, los orígenes y los efectos de esa pista también se silencian.</span><span class="sxs-lookup"><span data-stu-id="b089f-119">For example, if you mute a track, the transitions, sources, and effects in that track are also muted.</span></span> <span data-ttu-id="b089f-120">Una vez que el objeto deja de estar silenciado, sus elementos secundarios se revierten a su estado anterior, lo que podría estar silenciado o desactivado.</span><span class="sxs-lookup"><span data-stu-id="b089f-120">Once the object is no longer muted, its children revert to their previous state, which might be muted or unmuted.</span></span>

> [!Note]  
> <span data-ttu-id="b089f-121">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="b089f-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b089f-122">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b089f-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b089f-123">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b089f-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b089f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b089f-124">Requirements</span></span>



| <span data-ttu-id="b089f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b089f-125">Requirement</span></span> | <span data-ttu-id="b089f-126">Value</span><span class="sxs-lookup"><span data-stu-id="b089f-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b089f-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b089f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b089f-128"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="b089f-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b089f-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b089f-129">Library</span></span><br/> | <dl> <span data-ttu-id="b089f-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b089f-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b089f-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="b089f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b089f-132">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="b089f-132">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="b089f-133">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="b089f-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





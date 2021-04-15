---
description: El método GetDefaultEffect recupera el efecto predeterminado. Si el motor de representación no puede representar un efecto, sustituye el efecto predeterminado.
ms.assetid: 27eec6e8-702f-4e56-8d81-aa0633b8ec68
title: 'IAMTimeline:: GetDefaultEffect (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a0b1cf356a9c067ccae246814d2e1f381d7f78e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653852"
---
# <a name="iamtimelinegetdefaulteffect-method"></a><span data-ttu-id="80890-104">IAMTimeline:: GetDefaultEffect (método)</span><span class="sxs-lookup"><span data-stu-id="80890-104">IAMTimeline::GetDefaultEffect method</span></span>

> [!Note]  
> <span data-ttu-id="80890-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="80890-105">\[Deprecated.</span></span> <span data-ttu-id="80890-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="80890-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="80890-107">El `GetDefaultEffect` método recupera el efecto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="80890-107">The `GetDefaultEffect` method retrieves the default effect.</span></span> <span data-ttu-id="80890-108">Si el motor de representación no puede representar un efecto, sustituye el efecto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="80890-108">If the render engine cannot render an effect, it substitutes the default effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="80890-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80890-109">Syntax</span></span>


```C++
HRESULT GetDefaultEffect(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="80890-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="80890-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80890-111">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="80890-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="80890-112">Recibe el identificador único global (GUID) del efecto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="80890-112">Receives the globally unique identifier (GUID) of the default effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80890-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80890-113">Return value</span></span>

<span data-ttu-id="80890-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="80890-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="80890-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="80890-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="80890-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="80890-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="80890-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="80890-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="80890-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="80890-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="80890-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="80890-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="80890-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80890-120">Requirements</span></span>



| <span data-ttu-id="80890-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="80890-121">Requirement</span></span> | <span data-ttu-id="80890-122">Value</span><span class="sxs-lookup"><span data-stu-id="80890-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80890-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80890-123">Header</span></span><br/>  | <dl> <span data-ttu-id="80890-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="80890-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="80890-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="80890-125">Library</span></span><br/> | <dl> <span data-ttu-id="80890-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80890-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80890-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="80890-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80890-128">**Interfaz IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="80890-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="80890-129">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="80890-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





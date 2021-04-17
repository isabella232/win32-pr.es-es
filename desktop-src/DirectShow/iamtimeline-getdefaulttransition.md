---
description: El método GetDefaultTransition recupera la transición predeterminada. Si el motor de representación no puede representar una transición, sustituye la transición predeterminada.
ms.assetid: 3fe5d984-480b-4b35-970f-2f571e0fde7d
title: 'IAMTimeline:: GetDefaultTransition (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultTransition
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f594c0c0be10f93d0e90997df53074a9e69aec6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653849"
---
# <a name="iamtimelinegetdefaulttransition-method"></a><span data-ttu-id="1ded8-104">IAMTimeline:: GetDefaultTransition (método)</span><span class="sxs-lookup"><span data-stu-id="1ded8-104">IAMTimeline::GetDefaultTransition method</span></span>

> [!Note]  
> <span data-ttu-id="1ded8-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="1ded8-105">\[Deprecated.</span></span> <span data-ttu-id="1ded8-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1ded8-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1ded8-107">El `GetDefaultTransition` método recupera la transición predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1ded8-107">The `GetDefaultTransition` method retrieves the default transition.</span></span> <span data-ttu-id="1ded8-108">Si el motor de representación no puede representar una transición, sustituye la transición predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1ded8-108">If the render engine cannot render a transition, it substitutes the default transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ded8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ded8-109">Syntax</span></span>


```C++
HRESULT GetDefaultTransition(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="1ded8-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ded8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ded8-111">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="1ded8-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="1ded8-112">Recibe el GUID de la transición predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1ded8-112">Receives the GUID of the default transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ded8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ded8-113">Return value</span></span>

<span data-ttu-id="1ded8-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="1ded8-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1ded8-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1ded8-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ded8-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ded8-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1ded8-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="1ded8-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1ded8-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1ded8-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1ded8-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1ded8-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1ded8-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ded8-120">Requirements</span></span>



| <span data-ttu-id="1ded8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ded8-121">Requirement</span></span> | <span data-ttu-id="1ded8-122">Value</span><span class="sxs-lookup"><span data-stu-id="1ded8-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ded8-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ded8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1ded8-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ded8-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1ded8-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1ded8-125">Library</span></span><br/> | <dl> <span data-ttu-id="1ded8-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ded8-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ded8-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ded8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ded8-128">**Interfaz IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="1ded8-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="1ded8-129">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="1ded8-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





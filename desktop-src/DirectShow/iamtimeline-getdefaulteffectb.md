---
description: 'El método GetDefaultEffectB recupera el efecto predeterminado. Este método es equivalente a IAMTimeline:: GetDefaultEffect, pero recibe un valor BSTR en lugar de un GUID.'
ms.assetid: 62c37a61-9875-4140-8552-83d82c060715
title: 'IAMTimeline:: GetDefaultEffectB (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultEffectB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 01b82c42c34e3146bbad5560d516aef55225a3d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653851"
---
# <a name="iamtimelinegetdefaulteffectb-method"></a><span data-ttu-id="8aea8-104">IAMTimeline:: GetDefaultEffectB (método)</span><span class="sxs-lookup"><span data-stu-id="8aea8-104">IAMTimeline::GetDefaultEffectB method</span></span>

> [!Note]  
> <span data-ttu-id="8aea8-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="8aea8-105">\[Deprecated.</span></span> <span data-ttu-id="8aea8-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8aea8-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8aea8-107">El `GetDefaultEffectB` método recupera el efecto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8aea8-107">The `GetDefaultEffectB` method retrieves the default effect.</span></span> <span data-ttu-id="8aea8-108">Este método es equivalente a [**IAMTimeline:: GetDefaultEffect**](iamtimeline-getdefaulteffect.md), pero recibe un valor **BSTR** en lugar de un GUID.</span><span class="sxs-lookup"><span data-stu-id="8aea8-108">This method is equivalent to [**IAMTimeline::GetDefaultEffect**](iamtimeline-getdefaulteffect.md), but receives a **BSTR** value rather than a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="8aea8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8aea8-109">Syntax</span></span>


```C++
HRESULT GetDefaultEffectB(
  [out, retval] BSTR *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="8aea8-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8aea8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8aea8-111">*pGuid* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8aea8-111">*pGuid* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8aea8-112">Recibe un valor **BSTR** que representa el GUID del efecto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8aea8-112">Receives a **BSTR** value representing the GUID of the default effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8aea8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8aea8-113">Return value</span></span>

<span data-ttu-id="8aea8-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="8aea8-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8aea8-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8aea8-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8aea8-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8aea8-116">Remarks</span></span>

<span data-ttu-id="8aea8-117">El método asigna memoria para la cadena.</span><span class="sxs-lookup"><span data-stu-id="8aea8-117">The method allocates memory for the string.</span></span> <span data-ttu-id="8aea8-118">La aplicación debe llamar a **SysFreeString** para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="8aea8-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="8aea8-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="8aea8-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8aea8-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8aea8-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8aea8-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8aea8-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8aea8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8aea8-122">Requirements</span></span>



| <span data-ttu-id="8aea8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8aea8-123">Requirement</span></span> | <span data-ttu-id="8aea8-124">Value</span><span class="sxs-lookup"><span data-stu-id="8aea8-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8aea8-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8aea8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8aea8-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="8aea8-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8aea8-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8aea8-127">Library</span></span><br/> | <dl> <span data-ttu-id="8aea8-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8aea8-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8aea8-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="8aea8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8aea8-130">**Interfaz IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="8aea8-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="8aea8-131">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="8aea8-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





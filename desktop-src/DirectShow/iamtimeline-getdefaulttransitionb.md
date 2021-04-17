---
description: 'El método GetDefaultTransitionB recupera la transición predeterminada. Este método es equivalente a IAMTimeline:: GetDefaultTransition, pero recibe un valor BSTR, en lugar de un GUID.'
ms.assetid: ed743766-e970-4bd9-a9a0-8b5d9fec2d80
title: 'IAMTimeline:: GetDefaultTransitionB (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultTransitionB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f150ca0fafff6b250776a38b7ec68beb470e9d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681054"
---
# <a name="iamtimelinegetdefaulttransitionb-method"></a><span data-ttu-id="ec477-104">IAMTimeline:: GetDefaultTransitionB (método)</span><span class="sxs-lookup"><span data-stu-id="ec477-104">IAMTimeline::GetDefaultTransitionB method</span></span>

> [!Note]  
> <span data-ttu-id="ec477-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="ec477-105">\[Deprecated.</span></span> <span data-ttu-id="ec477-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ec477-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ec477-107">El `GetDefaultTransitionB` método recupera la transición predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ec477-107">The `GetDefaultTransitionB` method retrieves the default transition.</span></span> <span data-ttu-id="ec477-108">Este método es equivalente a [**IAMTimeline:: GetDefaultTransition**](iamtimeline-getdefaulttransition.md), pero recibe un valor BSTR, en lugar de un GUID.</span><span class="sxs-lookup"><span data-stu-id="ec477-108">This method is equivalent to [**IAMTimeline::GetDefaultTransition**](iamtimeline-getdefaulttransition.md), but receives a BSTR value, rather than a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec477-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec477-109">Syntax</span></span>


```C++
HRESULT GetDefaultTransitionB(
  [out, retval] BSTR *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="ec477-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec477-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec477-111">*pGuid* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="ec477-111">*pGuid* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ec477-112">Recibe un valor **BSTR** que representa el GUID de la transición predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ec477-112">Receives a **BSTR** value representing the GUID of the default transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec477-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec477-113">Return value</span></span>

<span data-ttu-id="ec477-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="ec477-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ec477-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ec477-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec477-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ec477-116">Remarks</span></span>

<span data-ttu-id="ec477-117">El método asigna memoria para la cadena.</span><span class="sxs-lookup"><span data-stu-id="ec477-117">The method allocates memory for the string.</span></span> <span data-ttu-id="ec477-118">La aplicación debe llamar a **SysFreeString** para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="ec477-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="ec477-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="ec477-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ec477-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ec477-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ec477-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ec477-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ec477-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec477-122">Requirements</span></span>



| <span data-ttu-id="ec477-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec477-123">Requirement</span></span> | <span data-ttu-id="ec477-124">Value</span><span class="sxs-lookup"><span data-stu-id="ec477-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec477-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec477-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ec477-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec477-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ec477-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ec477-127">Library</span></span><br/> | <dl> <span data-ttu-id="ec477-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec477-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec477-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec477-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec477-130">**Interfaz IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="ec477-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="ec477-131">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="ec477-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





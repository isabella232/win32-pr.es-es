---
description: El método SetDefaultTransition establece la transición predeterminada. Si el motor de representación no puede representar una transición, sustituye la transición predeterminada.
ms.assetid: 5ee84a12-402f-4f1c-9f08-206431c7ecdb
title: 'IAMTimeline:: SetDefaultTransition (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultTransition
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eeea5563ca9a2548507d3b4333d857d7cc156dd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690948"
---
# <a name="iamtimelinesetdefaulttransition-method"></a><span data-ttu-id="d0535-104">IAMTimeline:: SetDefaultTransition (método)</span><span class="sxs-lookup"><span data-stu-id="d0535-104">IAMTimeline::SetDefaultTransition method</span></span>

> [!Note]  
> <span data-ttu-id="d0535-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="d0535-105">\[Deprecated.</span></span> <span data-ttu-id="d0535-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d0535-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d0535-107">El `SetDefaultTransition` método establece la transición predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d0535-107">The `SetDefaultTransition` method sets the default transition.</span></span> <span data-ttu-id="d0535-108">Si el motor de representación no puede representar una transición, sustituye la transición predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d0535-108">If the render engine cannot render a transition, it substitutes the default transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0535-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0535-109">Syntax</span></span>


```C++
HRESULT SetDefaultTransition(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="d0535-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0535-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0535-111">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="d0535-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="d0535-112">Puntero a una variable que contiene el GUID de la transición predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d0535-112">Pointer to a variable that contains the GUID of the default transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0535-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0535-113">Return value</span></span>

<span data-ttu-id="d0535-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d0535-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d0535-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d0535-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0535-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0535-116">Remarks</span></span>

<span data-ttu-id="d0535-117">Si no se establece una transición predeterminada, o si la transición que se especifica como valor predeterminado produce un error, DES utiliza su propia transición predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d0535-117">If you do not set a default transition, or if the transition that you specify as a default causes an error, DES uses its own default transition.</span></span>

> [!Note]  
> <span data-ttu-id="d0535-118">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="d0535-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d0535-119">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d0535-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d0535-120">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d0535-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d0535-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0535-121">Requirements</span></span>



| <span data-ttu-id="d0535-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0535-122">Requirement</span></span> | <span data-ttu-id="d0535-123">Value</span><span class="sxs-lookup"><span data-stu-id="d0535-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0535-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0535-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d0535-125"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0535-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d0535-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d0535-126">Library</span></span><br/> | <dl> <span data-ttu-id="d0535-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0535-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0535-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0535-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0535-129">**Interfaz IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="d0535-129">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="d0535-130">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="d0535-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





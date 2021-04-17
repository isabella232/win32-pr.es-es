---
description: El método GetMuted recupera el estado silenciado del objeto.
ms.assetid: e901af1f-1137-4708-a98b-c9f83edc5ab9
title: 'IAMTimelineObj:: GetMuted (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetMuted
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8883b03f9070a017b8fa4788a7cfd795f46c5f3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690760"
---
# <a name="iamtimelineobjgetmuted-method"></a><span data-ttu-id="9b50f-103">IAMTimelineObj:: GetMuted (método)</span><span class="sxs-lookup"><span data-stu-id="9b50f-103">IAMTimelineObj::GetMuted method</span></span>

> [!Note]  
> <span data-ttu-id="9b50f-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="9b50f-104">\[Deprecated.</span></span> <span data-ttu-id="9b50f-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9b50f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9b50f-106">El `GetMuted` método recupera el estado silenciado del objeto.</span><span class="sxs-lookup"><span data-stu-id="9b50f-106">The `GetMuted` method retrieves the object's muted state.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b50f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b50f-107">Syntax</span></span>


```C++
HRESULT GetMuted(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="9b50f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b50f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b50f-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="9b50f-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="9b50f-110">Recibe un valor que indica el estado silenciado.</span><span class="sxs-lookup"><span data-stu-id="9b50f-110">Receives a value indicating the muted state.</span></span> <span data-ttu-id="9b50f-111">Si el valor es **true**, se silencia el objeto y sus elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="9b50f-111">If the value is **TRUE**, the object and its children are muted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b50f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b50f-112">Return value</span></span>

<span data-ttu-id="9b50f-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9b50f-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9b50f-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9b50f-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b50f-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b50f-115">Remarks</span></span>

<span data-ttu-id="9b50f-116">Si el elemento primario de un objeto está silenciado, se silencia el objeto, independientemente de su estado silenciado.</span><span class="sxs-lookup"><span data-stu-id="9b50f-116">If an object's parent is muted, the object is muted regardless of its muted state.</span></span> <span data-ttu-id="9b50f-117">Cuando el elemento primario ya no está silenciado, se restaura el estado silenciado anterior del objeto.</span><span class="sxs-lookup"><span data-stu-id="9b50f-117">When the parent is no longer muted, the object's previous muted state is restored.</span></span>

> [!Note]  
> <span data-ttu-id="9b50f-118">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="9b50f-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9b50f-119">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9b50f-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9b50f-120">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9b50f-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9b50f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b50f-121">Requirements</span></span>



| <span data-ttu-id="9b50f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b50f-122">Requirement</span></span> | <span data-ttu-id="9b50f-123">Value</span><span class="sxs-lookup"><span data-stu-id="9b50f-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b50f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b50f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9b50f-125"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b50f-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9b50f-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b50f-126">Library</span></span><br/> | <dl> <span data-ttu-id="9b50f-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b50f-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b50f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b50f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b50f-129">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="9b50f-129">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="9b50f-130">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="9b50f-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





---
description: El método GetSubObjectGUID recupera el GUID del subobjeto asociado a este objeto Timeline.
ms.assetid: c2787e6b-ed72-4a6c-9e1e-c79c00020585
title: 'IAMTimelineObj:: GetSubObjectGUID (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1c787bdbca8bbd255ccc78c3756fd0071d22f30d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690416"
---
# <a name="iamtimelineobjgetsubobjectguid-method"></a><span data-ttu-id="719e0-103">IAMTimelineObj:: GetSubObjectGUID (método)</span><span class="sxs-lookup"><span data-stu-id="719e0-103">IAMTimelineObj::GetSubObjectGUID method</span></span>

> [!Note]  
> <span data-ttu-id="719e0-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="719e0-104">\[Deprecated.</span></span> <span data-ttu-id="719e0-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="719e0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="719e0-106">El `GetSubObjectGUID` método recupera el GUID del subobjeto asociado a este objeto Timeline.</span><span class="sxs-lookup"><span data-stu-id="719e0-106">The `GetSubObjectGUID` method retrieves the GUID of the subobject associated with this timeline object.</span></span>

## <a name="syntax"></a><span data-ttu-id="719e0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="719e0-107">Syntax</span></span>


```C++
HRESULT GetSubObjectGUID(
   GUID *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="719e0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="719e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="719e0-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="719e0-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="719e0-110">Recibe el GUID del subobjeto o GUID \_ null si el objeto no tiene un subobjeto.</span><span class="sxs-lookup"><span data-stu-id="719e0-110">Receives the GUID of the subobject, or GUID\_NULL if the object does not have a subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="719e0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="719e0-111">Return value</span></span>

<span data-ttu-id="719e0-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="719e0-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="719e0-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="719e0-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="719e0-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="719e0-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="719e0-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="719e0-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="719e0-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="719e0-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="719e0-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="719e0-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="719e0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="719e0-118">Requirements</span></span>



| <span data-ttu-id="719e0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="719e0-119">Requirement</span></span> | <span data-ttu-id="719e0-120">Value</span><span class="sxs-lookup"><span data-stu-id="719e0-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="719e0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="719e0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="719e0-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="719e0-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="719e0-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="719e0-123">Library</span></span><br/> | <dl> <span data-ttu-id="719e0-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="719e0-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="719e0-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="719e0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="719e0-126">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="719e0-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="719e0-127">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="719e0-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





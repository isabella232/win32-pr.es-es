---
description: El método GetGenID recupera el identificador generado por el objeto. El identificador es un número reservado; las aplicaciones no deben utilizarla.
ms.assetid: b71b9b52-589b-4f80-915f-4805b1b8e295
title: 'IAMTimelineObj:: GetGenID (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetGenID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e3497777d25c9a81d4334f1979ce33f351111ed4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680851"
---
# <a name="iamtimelineobjgetgenid-method"></a><span data-ttu-id="c1f5b-104">IAMTimelineObj:: GetGenID (método)</span><span class="sxs-lookup"><span data-stu-id="c1f5b-104">IAMTimelineObj::GetGenID method</span></span>

> [!Note]  
> <span data-ttu-id="c1f5b-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="c1f5b-105">\[Deprecated.</span></span> <span data-ttu-id="c1f5b-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c1f5b-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c1f5b-107">El `GetGenID` método recupera el identificador generado del objeto.</span><span class="sxs-lookup"><span data-stu-id="c1f5b-107">The `GetGenID` method retrieves the object's generated identifier.</span></span> <span data-ttu-id="c1f5b-108">El identificador es un número reservado; las aplicaciones no deben utilizarla.</span><span class="sxs-lookup"><span data-stu-id="c1f5b-108">The identifier is a reserved number; applications should not use it.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1f5b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1f5b-109">Syntax</span></span>


```C++
HRESULT GetGenID(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="c1f5b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1f5b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1f5b-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="c1f5b-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="c1f5b-112">Recibe el identificador generado.</span><span class="sxs-lookup"><span data-stu-id="c1f5b-112">Receives the generated identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1f5b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1f5b-113">Return value</span></span>

<span data-ttu-id="c1f5b-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c1f5b-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c1f5b-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c1f5b-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1f5b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1f5b-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c1f5b-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="c1f5b-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c1f5b-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c1f5b-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c1f5b-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c1f5b-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c1f5b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1f5b-120">Requirements</span></span>



| <span data-ttu-id="c1f5b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1f5b-121">Requirement</span></span> | <span data-ttu-id="c1f5b-122">Value</span><span class="sxs-lookup"><span data-stu-id="c1f5b-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1f5b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c1f5b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c1f5b-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1f5b-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c1f5b-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c1f5b-125">Library</span></span><br/> | <dl> <span data-ttu-id="c1f5b-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1f5b-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1f5b-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1f5b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1f5b-128">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="c1f5b-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="c1f5b-129">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="c1f5b-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





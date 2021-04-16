---
description: El método GetUserID recupera el identificador definido por la aplicación del objeto.
ms.assetid: 68a20dfa-990e-47de-ae02-1d3182b7f13f
title: 'IAMTimelineObj:: GetUserID (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetUserID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f5d6c07fd826f2045ddc9f54445bc96feb5a7c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689932"
---
# <a name="iamtimelineobjgetuserid-method"></a><span data-ttu-id="e17a1-103">IAMTimelineObj:: GetUserID (método)</span><span class="sxs-lookup"><span data-stu-id="e17a1-103">IAMTimelineObj::GetUserID method</span></span>

> [!Note]  
> <span data-ttu-id="e17a1-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="e17a1-104">\[Deprecated.</span></span> <span data-ttu-id="e17a1-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e17a1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e17a1-106">El `GetUserID` método recupera el identificador definido por la aplicación del objeto.</span><span class="sxs-lookup"><span data-stu-id="e17a1-106">The `GetUserID` method retrieves the object's application-defined identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="e17a1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e17a1-107">Syntax</span></span>


```C++
HRESULT GetUserID(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="e17a1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e17a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e17a1-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="e17a1-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="e17a1-110">Recibe el identificador definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e17a1-110">Receives the application-defined identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e17a1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e17a1-111">Return value</span></span>

<span data-ttu-id="e17a1-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="e17a1-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e17a1-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e17a1-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e17a1-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e17a1-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e17a1-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="e17a1-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e17a1-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e17a1-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e17a1-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e17a1-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e17a1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e17a1-118">Requirements</span></span>



| <span data-ttu-id="e17a1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e17a1-119">Requirement</span></span> | <span data-ttu-id="e17a1-120">Value</span><span class="sxs-lookup"><span data-stu-id="e17a1-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e17a1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e17a1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e17a1-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="e17a1-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e17a1-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e17a1-123">Library</span></span><br/> | <dl> <span data-ttu-id="e17a1-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e17a1-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e17a1-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e17a1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e17a1-126">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="e17a1-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="e17a1-127">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="e17a1-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





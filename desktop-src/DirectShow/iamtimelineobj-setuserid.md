---
description: El método SetUserID establece un identificador definido por la aplicación para el objeto.
ms.assetid: 102fe29e-dc2c-4377-bce3-ba3c61dcb355
title: 'IAMTimelineObj:: SetUserID (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 31a0c59c6c93535be1200b2cd7678d4c355b5bc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690715"
---
# <a name="iamtimelineobjsetuserid-method"></a><span data-ttu-id="3950d-103">IAMTimelineObj:: SetUserID (método)</span><span class="sxs-lookup"><span data-stu-id="3950d-103">IAMTimelineObj::SetUserID method</span></span>

> [!Note]  
> <span data-ttu-id="3950d-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="3950d-104">\[Deprecated.</span></span> <span data-ttu-id="3950d-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3950d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3950d-106">El `SetUserID` método establece un identificador definido por la aplicación para el objeto.</span><span class="sxs-lookup"><span data-stu-id="3950d-106">The `SetUserID` method sets an application-defined identifier for the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3950d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3950d-107">Syntax</span></span>


```C++
HRESULT SetUserID(
   long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="3950d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3950d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3950d-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="3950d-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="3950d-110">Valor que especifica el identificador.</span><span class="sxs-lookup"><span data-stu-id="3950d-110">Value that specifies the identifier.</span></span> <span data-ttu-id="3950d-111">Este identificador solo lo usa la aplicación y puede ser cualquier valor.</span><span class="sxs-lookup"><span data-stu-id="3950d-111">This identifier is used only by the application and can be any value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3950d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3950d-112">Return value</span></span>

<span data-ttu-id="3950d-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="3950d-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3950d-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3950d-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3950d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3950d-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3950d-116">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="3950d-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3950d-117">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3950d-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3950d-118">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3950d-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3950d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3950d-119">Requirements</span></span>



| <span data-ttu-id="3950d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3950d-120">Requirement</span></span> | <span data-ttu-id="3950d-121">Value</span><span class="sxs-lookup"><span data-stu-id="3950d-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3950d-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3950d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3950d-123"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="3950d-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3950d-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3950d-124">Library</span></span><br/> | <dl> <span data-ttu-id="3950d-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3950d-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3950d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="3950d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3950d-127">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="3950d-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="3950d-128">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="3950d-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





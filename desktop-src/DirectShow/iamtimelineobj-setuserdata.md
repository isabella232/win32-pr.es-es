---
description: El método SetUserData establece datos persistentes definidos por la aplicación.
ms.assetid: 195d8e92-a25c-40ff-8cc7-c1f05bdd76ab
title: 'IAMTimelineObj:: SetUserData (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserData
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7e09aafd614234827a704d8b9997f27981eb7c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680722"
---
# <a name="iamtimelineobjsetuserdata-method"></a><span data-ttu-id="7c720-103">IAMTimelineObj:: SetUserData (método)</span><span class="sxs-lookup"><span data-stu-id="7c720-103">IAMTimelineObj::SetUserData method</span></span>

> [!Note]  
> <span data-ttu-id="7c720-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="7c720-104">\[Deprecated.</span></span> <span data-ttu-id="7c720-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7c720-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7c720-106">El `SetUserData` método establece los datos persistentes definidos por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7c720-106">The `SetUserData` method sets application-defined persistent data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c720-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c720-107">Syntax</span></span>


```C++
HRESULT SetUserData(
   BYTE *pData,
   long Size
);
```



## <a name="parameters"></a><span data-ttu-id="7c720-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c720-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c720-109">*pData*</span><span class="sxs-lookup"><span data-stu-id="7c720-109">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="7c720-110">Puntero a un búfer que contiene los datos.</span><span class="sxs-lookup"><span data-stu-id="7c720-110">Pointer to a buffer containing the data.</span></span>

</dd> <dt>

<span data-ttu-id="7c720-111">*Tamaño*</span><span class="sxs-lookup"><span data-stu-id="7c720-111">*Size*</span></span> 
</dt> <dd>

<span data-ttu-id="7c720-112">Tamaño de los datos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="7c720-112">Size of the data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c720-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c720-113">Return value</span></span>

<span data-ttu-id="7c720-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="7c720-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7c720-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7c720-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c720-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c720-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7c720-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="7c720-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7c720-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7c720-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7c720-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7c720-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7c720-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c720-120">Requirements</span></span>



| <span data-ttu-id="7c720-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c720-121">Requirement</span></span> | <span data-ttu-id="7c720-122">Value</span><span class="sxs-lookup"><span data-stu-id="7c720-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c720-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c720-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7c720-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c720-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7c720-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c720-125">Library</span></span><br/> | <dl> <span data-ttu-id="7c720-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c720-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c720-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c720-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c720-128">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="7c720-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="7c720-129">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="7c720-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





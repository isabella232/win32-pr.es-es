---
description: El método GetUserData recupera los datos persistentes definidos por la aplicación.
ms.assetid: dd2cdb37-9c4f-4356-a35f-2d42b7588da6
title: 'IAMTimelineObj:: GetUserData (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetUserData
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9dda74980dcdae9cd73e749d9cb4324b4c6357f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680903"
---
# <a name="iamtimelineobjgetuserdata-method"></a><span data-ttu-id="abe4d-103">IAMTimelineObj:: GetUserData (método)</span><span class="sxs-lookup"><span data-stu-id="abe4d-103">IAMTimelineObj::GetUserData method</span></span>

> [!Note]  
> <span data-ttu-id="abe4d-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="abe4d-104">\[Deprecated.</span></span> <span data-ttu-id="abe4d-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="abe4d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="abe4d-106">El `GetUserData` método recupera los datos persistentes definidos por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="abe4d-106">The `GetUserData` method retrieves the application-defined persistent data.</span></span>

## <a name="syntax"></a><span data-ttu-id="abe4d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="abe4d-107">Syntax</span></span>


```C++
HRESULT GetUserData(
   BYTE *pData,
   long *pSize
);
```



## <a name="parameters"></a><span data-ttu-id="abe4d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="abe4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abe4d-109">*pData*</span><span class="sxs-lookup"><span data-stu-id="abe4d-109">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="abe4d-110">Puntero a un búfer que recibe los datos.</span><span class="sxs-lookup"><span data-stu-id="abe4d-110">Pointer to a buffer that receives the data.</span></span> <span data-ttu-id="abe4d-111">Para determinar el tamaño del búfer que se va a asignar, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="abe4d-111">To determine the size of buffer to allocate, set this parameter to **NULL**.</span></span> <span data-ttu-id="abe4d-112">El tamaño necesario se devuelve en *pSize*.</span><span class="sxs-lookup"><span data-stu-id="abe4d-112">The required size is returned in *pSize*.</span></span>

</dd> <dt>

<span data-ttu-id="abe4d-113">*pSize*</span><span class="sxs-lookup"><span data-stu-id="abe4d-113">*pSize*</span></span> 
</dt> <dd>

<span data-ttu-id="abe4d-114">Recibe el tamaño de los datos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="abe4d-114">Receives the size of the data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abe4d-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="abe4d-115">Return value</span></span>

<span data-ttu-id="abe4d-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="abe4d-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="abe4d-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="abe4d-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="abe4d-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="abe4d-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="abe4d-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="abe4d-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="abe4d-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="abe4d-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="abe4d-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="abe4d-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="abe4d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abe4d-122">Requirements</span></span>



| <span data-ttu-id="abe4d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="abe4d-123">Requirement</span></span> | <span data-ttu-id="abe4d-124">Value</span><span class="sxs-lookup"><span data-stu-id="abe4d-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="abe4d-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="abe4d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="abe4d-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="abe4d-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="abe4d-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="abe4d-127">Library</span></span><br/> | <dl> <span data-ttu-id="abe4d-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="abe4d-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abe4d-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="abe4d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abe4d-130">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="abe4d-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="abe4d-131">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="abe4d-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





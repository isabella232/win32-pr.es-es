---
description: El método GetSubObjectLoaded determina si se ha establecido el puntero de subobjeto.
ms.assetid: 05b58435-eeca-4b52-9a53-ad7f81b5b35d
title: 'IAMTimelineObj:: GetSubObjectLoaded (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectLoaded
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 073810b6c02997d78e21a66976954d88e47ae82b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690219"
---
# <a name="iamtimelineobjgetsubobjectloaded-method"></a><span data-ttu-id="913dd-103">IAMTimelineObj:: GetSubObjectLoaded (método)</span><span class="sxs-lookup"><span data-stu-id="913dd-103">IAMTimelineObj::GetSubObjectLoaded method</span></span>

> [!Note]  
> <span data-ttu-id="913dd-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="913dd-104">\[Deprecated.</span></span> <span data-ttu-id="913dd-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="913dd-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="913dd-106">El `GetSubObjectLoaded` método determina si se ha establecido el puntero de subobjeto.</span><span class="sxs-lookup"><span data-stu-id="913dd-106">The `GetSubObjectLoaded` method determines whether the subobject pointer has been set.</span></span>

## <a name="syntax"></a><span data-ttu-id="913dd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="913dd-107">Syntax</span></span>


```C++
HRESULT GetSubObjectLoaded(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="913dd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="913dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="913dd-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="913dd-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="913dd-110">Recibe un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="913dd-110">Receives a Boolean value.</span></span> <span data-ttu-id="913dd-111">Si el valor es **true**, se ha establecido el puntero de subobjeto.</span><span class="sxs-lookup"><span data-stu-id="913dd-111">If the value is **TRUE**, the subobject pointer has been set.</span></span> <span data-ttu-id="913dd-112">Si **es false**, no se ha establecido el puntero.</span><span class="sxs-lookup"><span data-stu-id="913dd-112">If **FALSE**, the pointer has not been set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="913dd-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="913dd-113">Return value</span></span>

<span data-ttu-id="913dd-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="913dd-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="913dd-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="913dd-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="913dd-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="913dd-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="913dd-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="913dd-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="913dd-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="913dd-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="913dd-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="913dd-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="913dd-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="913dd-120">Requirements</span></span>



| <span data-ttu-id="913dd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="913dd-121">Requirement</span></span> | <span data-ttu-id="913dd-122">Value</span><span class="sxs-lookup"><span data-stu-id="913dd-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="913dd-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="913dd-123">Header</span></span><br/>  | <dl> <span data-ttu-id="913dd-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="913dd-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="913dd-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="913dd-125">Library</span></span><br/> | <dl> <span data-ttu-id="913dd-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="913dd-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="913dd-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="913dd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="913dd-128">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="913dd-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="913dd-129">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="913dd-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





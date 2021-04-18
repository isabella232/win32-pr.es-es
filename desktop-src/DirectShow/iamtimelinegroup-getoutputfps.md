---
description: El método GetOutputFPS recupera la velocidad de fotogramas de salida de este grupo.
ms.assetid: e6dfa4a9-4d44-4ce7-9aec-3564fd337ff6
title: 'IAMTimelineGroup:: GetOutputFPS (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetOutputFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f02e7db36e5ea61e3c738b4c2d92678674bfcec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681248"
---
# <a name="iamtimelinegroupgetoutputfps-method"></a><span data-ttu-id="83640-103">IAMTimelineGroup:: GetOutputFPS (método)</span><span class="sxs-lookup"><span data-stu-id="83640-103">IAMTimelineGroup::GetOutputFPS method</span></span>

> [!Note]  
> <span data-ttu-id="83640-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="83640-104">\[Deprecated.</span></span> <span data-ttu-id="83640-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="83640-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="83640-106">El `GetOutputFPS` método recupera la velocidad de fotogramas de salida de este grupo.</span><span class="sxs-lookup"><span data-stu-id="83640-106">The `GetOutputFPS` method retrieves the output frame rate of this group.</span></span>

## <a name="syntax"></a><span data-ttu-id="83640-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83640-107">Syntax</span></span>


```C++
HRESULT GetOutputFPS(
   double *pFPS
);
```



## <a name="parameters"></a><span data-ttu-id="83640-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83640-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83640-109">*pFPS*</span><span class="sxs-lookup"><span data-stu-id="83640-109">*pFPS*</span></span> 
</dt> <dd>

<span data-ttu-id="83640-110">Recibe la velocidad de fotogramas de salida, en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="83640-110">Receives the output frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83640-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83640-111">Return value</span></span>

<span data-ttu-id="83640-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="83640-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="83640-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="83640-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="83640-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83640-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="83640-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="83640-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="83640-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="83640-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="83640-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="83640-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="83640-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83640-118">Requirements</span></span>



| <span data-ttu-id="83640-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="83640-119">Requirement</span></span> | <span data-ttu-id="83640-120">Value</span><span class="sxs-lookup"><span data-stu-id="83640-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83640-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="83640-121">Header</span></span><br/>  | <dl> <span data-ttu-id="83640-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="83640-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="83640-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="83640-123">Library</span></span><br/> | <dl> <span data-ttu-id="83640-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83640-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83640-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="83640-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83640-126">**Interfaz IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="83640-126">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="83640-127">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="83640-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





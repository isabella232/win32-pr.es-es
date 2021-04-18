---
description: El método ApplyChanges aplica todas las propiedades que han cambiado.
ms.assetid: dece1e61-7fe1-40f1-8d1d-89b5a334d04e
title: 'IDxtJpeg:: ApplyChanges (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.ApplyChanges
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 522df2fc362b0332d4eb41e9a2f10201bfcdec9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679274"
---
# <a name="idxtjpegapplychanges-method"></a><span data-ttu-id="781cd-103">IDxtJpeg:: ApplyChanges (método)</span><span class="sxs-lookup"><span data-stu-id="781cd-103">IDxtJpeg::ApplyChanges method</span></span>

> [!Note]  
> <span data-ttu-id="781cd-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="781cd-104">\[Deprecated.</span></span> <span data-ttu-id="781cd-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="781cd-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="781cd-106">El `ApplyChanges` método aplica todas las propiedades que han cambiado.</span><span class="sxs-lookup"><span data-stu-id="781cd-106">The `ApplyChanges` method applies any properties that have changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="781cd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="781cd-107">Syntax</span></span>


```C++
HRESULT ApplyChanges();
```



## <a name="parameters"></a><span data-ttu-id="781cd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="781cd-108">Parameters</span></span>

<span data-ttu-id="781cd-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="781cd-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="781cd-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="781cd-110">Return value</span></span>

<span data-ttu-id="781cd-111">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="781cd-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="781cd-112">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="781cd-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="781cd-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="781cd-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="781cd-114">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="781cd-114">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="781cd-115">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="781cd-115">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="781cd-116">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="781cd-116">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="781cd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="781cd-117">Requirements</span></span>



| <span data-ttu-id="781cd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="781cd-118">Requirement</span></span> | <span data-ttu-id="781cd-119">Value</span><span class="sxs-lookup"><span data-stu-id="781cd-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="781cd-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="781cd-120">Header</span></span><br/>  | <dl> <span data-ttu-id="781cd-121"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="781cd-121"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="781cd-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="781cd-122">Library</span></span><br/> | <dl> <span data-ttu-id="781cd-123"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="781cd-123"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="781cd-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="781cd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="781cd-125">**Interfaz IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="781cd-125">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 





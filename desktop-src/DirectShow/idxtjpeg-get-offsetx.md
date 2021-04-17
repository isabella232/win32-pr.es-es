---
description: El \_ método get OffsetX recupera el desplazamiento horizontal del origen de borrado.
ms.assetid: 0ca97bb9-9359-4098-9e80-1847da4154ec
title: 'Método IDxtJpeg:: get_OffsetX (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_OffsetX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d18d8ede94700f2de2fe49e44031675c7c91c930
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680672"
---
# <a name="idxtjpegget_offsetx-method"></a><span data-ttu-id="9c031-103">IDxtJpeg:: get \_ offsetX (método)</span><span class="sxs-lookup"><span data-stu-id="9c031-103">IDxtJpeg::get\_OffsetX method</span></span>

> [!Note]  
> <span data-ttu-id="9c031-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="9c031-104">\[Deprecated.</span></span> <span data-ttu-id="9c031-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9c031-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9c031-106">El `get_OffsetX` método recupera el desplazamiento horizontal del origen de borrado.</span><span class="sxs-lookup"><span data-stu-id="9c031-106">The `get_OffsetX` method retrieves the horizontal offset of the wipe origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c031-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c031-107">Syntax</span></span>


```C++
HRESULT get_OffsetX(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="9c031-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c031-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c031-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="9c031-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="9c031-110">Recibe el desplazamiento horizontal del origen de borrado, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="9c031-110">Receives the horizontal offset of the wipe origin, in pixels.</span></span> <span data-ttu-id="9c031-111">El centro del borrado se desplaza por esta cantidad.</span><span class="sxs-lookup"><span data-stu-id="9c031-111">The center of the wipe is offset by this amount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c031-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c031-112">Return value</span></span>

<span data-ttu-id="9c031-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9c031-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9c031-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9c031-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c031-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c031-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9c031-116">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="9c031-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9c031-117">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9c031-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9c031-118">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9c031-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9c031-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c031-119">Requirements</span></span>



| <span data-ttu-id="9c031-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c031-120">Requirement</span></span> | <span data-ttu-id="9c031-121">Value</span><span class="sxs-lookup"><span data-stu-id="9c031-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c031-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c031-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9c031-123"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c031-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9c031-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9c031-124">Library</span></span><br/> | <dl> <span data-ttu-id="9c031-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c031-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c031-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c031-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c031-127">**Interfaz IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="9c031-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 





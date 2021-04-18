---
description: El \_ método put BorderWidth especifica el ancho del borde sólido a lo largo de los bordes del patrón de barrido.
ms.assetid: a618926a-efa4-47a2-9ce9-ae298ed41083
title: 'IDxtJpeg: método de ut_BorderWidth de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_BorderWidth
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: df7435b8a516b818b6d7c86e907ba75cce86f6c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680984"
---
# <a name="idxtjpegput_borderwidth-method"></a><span data-ttu-id="23039-103">IDxtJpeg::p \_ método BorderWidth</span><span class="sxs-lookup"><span data-stu-id="23039-103">IDxtJpeg::put\_BorderWidth method</span></span>

> [!Note]  
> <span data-ttu-id="23039-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="23039-104">\[Deprecated.</span></span> <span data-ttu-id="23039-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="23039-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="23039-106">El `put_BorderWidth` método especifica el ancho del borde sólido a lo largo de los bordes del patrón de barrido.</span><span class="sxs-lookup"><span data-stu-id="23039-106">The `put_BorderWidth` method specifies the width of the solid border along the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="23039-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23039-107">Syntax</span></span>


```C++
HRESULT put_BorderWidth(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="23039-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23039-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23039-109">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="23039-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23039-110">Ancho del borde, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="23039-110">The width of the border, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23039-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23039-111">Return value</span></span>

<span data-ttu-id="23039-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="23039-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="23039-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="23039-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="23039-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23039-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="23039-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="23039-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="23039-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="23039-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="23039-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="23039-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="23039-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23039-118">Requirements</span></span>



| <span data-ttu-id="23039-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="23039-119">Requirement</span></span> | <span data-ttu-id="23039-120">Value</span><span class="sxs-lookup"><span data-stu-id="23039-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23039-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23039-121">Header</span></span><br/>  | <dl> <span data-ttu-id="23039-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="23039-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="23039-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23039-123">Library</span></span><br/> | <dl> <span data-ttu-id="23039-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23039-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23039-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="23039-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23039-126">**Interfaz IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="23039-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 





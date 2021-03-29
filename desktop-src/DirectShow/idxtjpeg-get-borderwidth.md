---
description: El \_ método get BorderWidth recupera el ancho del borde sólido a lo largo de los bordes del patrón de barrido.
ms.assetid: 85c62524-5936-475e-a73b-7a3c926bb5f0
title: 'Método IDxtJpeg:: get_BorderWidth (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_BorderWidth
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 28405c08d5666c8f182e0ffdb6ed1aa7bac599d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680673"
---
# <a name="idxtjpegget_borderwidth-method"></a><span data-ttu-id="2d577-103">IDxtJpeg:: get \_ BorderWidth (método)</span><span class="sxs-lookup"><span data-stu-id="2d577-103">IDxtJpeg::get\_BorderWidth method</span></span>

> [!Note]  
> <span data-ttu-id="2d577-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="2d577-104">\[Deprecated.</span></span> <span data-ttu-id="2d577-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2d577-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2d577-106">El `get_BorderWidth` método recupera el ancho del borde sólido a lo largo de los bordes del patrón de barrido.</span><span class="sxs-lookup"><span data-stu-id="2d577-106">The `get_BorderWidth` method retrieves the width of the solid border along the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d577-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d577-107">Syntax</span></span>


```C++
HRESULT get_BorderWidth(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="2d577-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2d577-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d577-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2d577-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2d577-110">Recibe el ancho del borde, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="2d577-110">Receives the width of the border, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d577-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2d577-111">Return value</span></span>

<span data-ttu-id="2d577-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="2d577-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2d577-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2d577-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d577-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2d577-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2d577-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="2d577-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2d577-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2d577-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2d577-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="2d577-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2d577-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d577-118">Requirements</span></span>



| <span data-ttu-id="2d577-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d577-119">Requirement</span></span> | <span data-ttu-id="2d577-120">Value</span><span class="sxs-lookup"><span data-stu-id="2d577-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d577-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d577-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2d577-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d577-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2d577-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d577-123">Library</span></span><br/> | <dl> <span data-ttu-id="2d577-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d577-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d577-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d577-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d577-126">**Interfaz IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="2d577-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 





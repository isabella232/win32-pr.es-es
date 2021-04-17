---
description: El \_ método get BorderColor recupera el color del borde alrededor de los bordes del patrón de barrido.
ms.assetid: 9d36cc49-c174-4b93-a030-ca8d2890c624
title: 'Método IDxtJpeg:: get_BorderColor (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_BorderColor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7f37c37865caf76839733ada376ec637747977ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680897"
---
# <a name="idxtjpegget_bordercolor-method"></a><span data-ttu-id="5d212-103">IDxtJpeg:: get \_ BorderColor (método)</span><span class="sxs-lookup"><span data-stu-id="5d212-103">IDxtJpeg::get\_BorderColor method</span></span>

> [!Note]  
> <span data-ttu-id="5d212-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="5d212-104">\[Deprecated.</span></span> <span data-ttu-id="5d212-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5d212-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5d212-106">El `get_BorderColor` método recupera el color del borde alrededor de los bordes del patrón de barrido.</span><span class="sxs-lookup"><span data-stu-id="5d212-106">The `get_BorderColor` method retrieves the color of the border around the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d212-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d212-107">Syntax</span></span>


```C++
HRESULT get_BorderColor(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="5d212-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d212-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d212-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5d212-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5d212-110">Recibe el color.</span><span class="sxs-lookup"><span data-stu-id="5d212-110">Receives the color.</span></span> <span data-ttu-id="5d212-111">El valor devuelto es un número hexadecimal con el formato 0xRRGGBB, donde RR es el valor rojo, GG es el valor verde y BB es el valor azul.</span><span class="sxs-lookup"><span data-stu-id="5d212-111">The returned value is a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d212-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d212-112">Return value</span></span>

<span data-ttu-id="5d212-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="5d212-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5d212-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5d212-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d212-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d212-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5d212-116">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="5d212-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5d212-117">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5d212-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5d212-118">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5d212-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5d212-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d212-119">Requirements</span></span>



| <span data-ttu-id="5d212-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d212-120">Requirement</span></span> | <span data-ttu-id="5d212-121">Value</span><span class="sxs-lookup"><span data-stu-id="5d212-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d212-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d212-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5d212-123"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d212-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5d212-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5d212-124">Library</span></span><br/> | <dl> <span data-ttu-id="5d212-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d212-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d212-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d212-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d212-127">**Interfaz IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="5d212-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 





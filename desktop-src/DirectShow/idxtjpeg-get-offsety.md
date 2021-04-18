---
description: El \_ método get offsetY recupera el desplazamiento vertical del origen de borrado.
ms.assetid: 0d8b8df2-b916-4143-b1f1-7912ef3fa025
title: 'Método IDxtJpeg:: get_OffsetY (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_OffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 76c0d60ac5150fcec1bde63ccb4e03d820c38ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679379"
---
# <a name="idxtjpegget_offsety-method"></a><span data-ttu-id="02639-103">IDxtJpeg:: get ( \_ método de desplazamiento)</span><span class="sxs-lookup"><span data-stu-id="02639-103">IDxtJpeg::get\_OffsetY method</span></span>

> [!Note]  
> <span data-ttu-id="02639-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="02639-104">\[Deprecated.</span></span> <span data-ttu-id="02639-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="02639-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="02639-106">El `get_OffsetY` método recupera el desplazamiento vertical del origen de borrado.</span><span class="sxs-lookup"><span data-stu-id="02639-106">The `get_OffsetY` method retrieves the vertical offset of the wipe origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="02639-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02639-107">Syntax</span></span>


```C++
HRESULT get_OffsetY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="02639-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02639-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02639-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="02639-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="02639-110">Recibe el desplazamiento vertical del origen de borrado, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="02639-110">Receives the vertical offset of the wipe origin, in pixels.</span></span> <span data-ttu-id="02639-111">El centro del borrado se desplaza por esta cantidad.</span><span class="sxs-lookup"><span data-stu-id="02639-111">The center of the wipe is offset by this amount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02639-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02639-112">Return value</span></span>

<span data-ttu-id="02639-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="02639-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="02639-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="02639-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="02639-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02639-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="02639-116">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="02639-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="02639-117">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="02639-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="02639-118">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="02639-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="02639-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02639-119">Requirements</span></span>



| <span data-ttu-id="02639-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="02639-120">Requirement</span></span> | <span data-ttu-id="02639-121">Value</span><span class="sxs-lookup"><span data-stu-id="02639-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02639-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02639-122">Header</span></span><br/>  | <dl> <span data-ttu-id="02639-123"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="02639-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="02639-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="02639-124">Library</span></span><br/> | <dl> <span data-ttu-id="02639-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02639-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02639-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="02639-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02639-127">**Interfaz IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="02639-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 





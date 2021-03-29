---
description: El \_ método get scaleY recupera la cantidad por la que se ajusta verticalmente el borrado.
ms.assetid: d8b80f19-2ec5-4d66-bd13-d6f7b5144345
title: 'Método IDxtJpeg:: get_ScaleY (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ScaleY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f4ca3feb0177ad1c9172721ca312e810fdb105b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680670"
---
# <a name="idxtjpegget_scaley-method"></a><span data-ttu-id="68b21-103">IDxtJpeg:: get \_ scaleY (método)</span><span class="sxs-lookup"><span data-stu-id="68b21-103">IDxtJpeg::get\_ScaleY method</span></span>

> [!Note]  
> <span data-ttu-id="68b21-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="68b21-104">\[Deprecated.</span></span> <span data-ttu-id="68b21-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="68b21-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="68b21-106">El `get_ScaleY` método recupera la cantidad por la que se ajusta verticalmente el borrado.</span><span class="sxs-lookup"><span data-stu-id="68b21-106">The `get_ScaleY` method retrieves the amount by which the wipe is stretched vertically.</span></span>

## <a name="syntax"></a><span data-ttu-id="68b21-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68b21-107">Syntax</span></span>


```C++
HRESULT get_ScaleY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="68b21-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68b21-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68b21-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="68b21-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="68b21-110">Recibe la cantidad por la que se estira verticalmente el borrado, como un porcentaje de la definición de borrado original.</span><span class="sxs-lookup"><span data-stu-id="68b21-110">Receives the amount by which the wipe is stretched vertically, as a percentage of the original wipe definition.</span></span> <span data-ttu-id="68b21-111">Por ejemplo, el valor 1,0 significa que no hay expansión y 2,0 significa que el 200% se ajusta.</span><span class="sxs-lookup"><span data-stu-id="68b21-111">For example, the value 1.0 means no stretching, and 2.0 means 200% stretching.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68b21-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68b21-112">Return value</span></span>

<span data-ttu-id="68b21-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="68b21-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="68b21-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="68b21-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="68b21-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68b21-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="68b21-116">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="68b21-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="68b21-117">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="68b21-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="68b21-118">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="68b21-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="68b21-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68b21-119">Requirements</span></span>



| <span data-ttu-id="68b21-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="68b21-120">Requirement</span></span> | <span data-ttu-id="68b21-121">Value</span><span class="sxs-lookup"><span data-stu-id="68b21-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68b21-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68b21-122">Header</span></span><br/>  | <dl> <span data-ttu-id="68b21-123"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="68b21-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="68b21-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68b21-124">Library</span></span><br/> | <dl> <span data-ttu-id="68b21-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68b21-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68b21-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="68b21-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68b21-127">**Interfaz IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="68b21-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 





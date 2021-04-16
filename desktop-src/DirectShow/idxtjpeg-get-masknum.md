---
description: El \_ método get MaskNum recupera el código de borrado de SMPTE de la eliminación.
ms.assetid: 49710d40-acc0-453e-ac9c-882794a0b82d
title: 'Método IDxtJpeg:: get_MaskNum (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_MaskNum
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 869809fdea6e1c329088abca50a1670239554327
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679380"
---
# <a name="idxtjpegget_masknum-method"></a><span data-ttu-id="04749-103">IDxtJpeg:: get \_ MaskNum (método)</span><span class="sxs-lookup"><span data-stu-id="04749-103">IDxtJpeg::get\_MaskNum method</span></span>

> [!Note]  
> <span data-ttu-id="04749-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="04749-104">\[Deprecated.</span></span> <span data-ttu-id="04749-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="04749-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="04749-106">El `get_MaskNum` método recupera el código de borrado de SMPTE del borrado.</span><span class="sxs-lookup"><span data-stu-id="04749-106">The `get_MaskNum` method retrieves the SMPTE wipe code of the wipe.</span></span>

## <a name="syntax"></a><span data-ttu-id="04749-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04749-107">Syntax</span></span>


```C++
HRESULT get_MaskNum(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="04749-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04749-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04749-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="04749-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="04749-110">Recibe el código de borrado de SMPTE.</span><span class="sxs-lookup"><span data-stu-id="04749-110">Receives the SMPTE wipe code.</span></span> <span data-ttu-id="04749-111">Para obtener una lista de barridos SMPTE admitidos, consulte [transición de borrado de SMPTE](smpte-wipe-transition.md).</span><span class="sxs-lookup"><span data-stu-id="04749-111">For a list of supported SMPTE wipes, see [SMPTE Wipe Transition](smpte-wipe-transition.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04749-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04749-112">Return value</span></span>

<span data-ttu-id="04749-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="04749-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="04749-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="04749-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="04749-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04749-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="04749-116">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="04749-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="04749-117">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="04749-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="04749-118">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="04749-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="04749-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04749-119">Requirements</span></span>



| <span data-ttu-id="04749-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="04749-120">Requirement</span></span> | <span data-ttu-id="04749-121">Value</span><span class="sxs-lookup"><span data-stu-id="04749-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04749-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04749-122">Header</span></span><br/>  | <dl> <span data-ttu-id="04749-123"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="04749-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="04749-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="04749-124">Library</span></span><br/> | <dl> <span data-ttu-id="04749-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04749-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04749-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="04749-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04749-127">**Interfaz IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="04749-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 





---
description: El \_ método put RGB especifica el color RGB en el que se va a incluir la tecla. Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ RGB.
ms.assetid: 7a0b794e-bea6-4061-98a0-3f70521e89a3
title: 'IDxtKey: método de ut_RGB de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0b7d282ceb4a693d5a390b8df9b935f0e415d150
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680497"
---
# <a name="idxtkeyput_rgb-method"></a><span data-ttu-id="d8698-104">IDxtKey: \_ método RGB:p UT</span><span class="sxs-lookup"><span data-stu-id="d8698-104">IDxtKey::put\_RGB method</span></span>

> [!Note]  
> <span data-ttu-id="d8698-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="d8698-105">\[Deprecated.</span></span> <span data-ttu-id="d8698-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d8698-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d8698-107">El `put_RGB` método especifica el color RGB en el que se va a hacer la tecla.</span><span class="sxs-lookup"><span data-stu-id="d8698-107">The `put_RGB` method specifies the RGB color on which to key.</span></span> <span data-ttu-id="d8698-108">Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ RGB.</span><span class="sxs-lookup"><span data-stu-id="d8698-108">This property applies only when the key type is DXTKEY\_RGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8698-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8698-109">Syntax</span></span>


```C++
HRESULT put_RGB(
  [in] DWORD newVal
);
```



## <a name="parameters"></a><span data-ttu-id="d8698-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8698-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8698-111">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d8698-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8698-112">Especifica el color como un número hexadecimal con el formato 0xRRGGBB, donde RR es el valor rojo, GG es el valor verde y BB es el valor azul.</span><span class="sxs-lookup"><span data-stu-id="d8698-112">Specifies the color as a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8698-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8698-113">Return value</span></span>

<span data-ttu-id="d8698-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d8698-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d8698-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d8698-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8698-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8698-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d8698-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="d8698-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d8698-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d8698-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d8698-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d8698-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d8698-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8698-120">Requirements</span></span>



| <span data-ttu-id="d8698-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8698-121">Requirement</span></span> | <span data-ttu-id="d8698-122">Value</span><span class="sxs-lookup"><span data-stu-id="d8698-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8698-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8698-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d8698-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8698-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d8698-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d8698-125">Library</span></span><br/> | <dl> <span data-ttu-id="d8698-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8698-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8698-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8698-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8698-128">**Interfaz IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="d8698-128">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="d8698-129">**IDxtKey::p \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="d8698-129">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 





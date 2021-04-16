---
description: El \_ método put Hue especifica el valor de matiz que se va a incluir en la clave. Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ Hue.
ms.assetid: 90c8c610-7ceb-479b-bb0e-d8753d0d7dac
title: 'IDxtKey: método de ut_Hue de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Hue
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9d2b08f3e805edc8b8860495fc105f0cfdf6768f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679415"
---
# <a name="idxtkeyput_hue-method"></a><span data-ttu-id="f13e4-104">IDxtKey::p \_ método Hue</span><span class="sxs-lookup"><span data-stu-id="f13e4-104">IDxtKey::put\_Hue method</span></span>

> [!Note]  
> <span data-ttu-id="f13e4-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="f13e4-105">\[Deprecated.</span></span> <span data-ttu-id="f13e4-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f13e4-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f13e4-107">El `put_Hue` método especifica el valor de matiz en el que se va a especificar la tecla.</span><span class="sxs-lookup"><span data-stu-id="f13e4-107">The `put_Hue` method specifies the hue value on which to key.</span></span> <span data-ttu-id="f13e4-108">Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ Hue.</span><span class="sxs-lookup"><span data-stu-id="f13e4-108">This property applies only when the key type is DXTKEY\_HUE.</span></span>

## <a name="syntax"></a><span data-ttu-id="f13e4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f13e4-109">Syntax</span></span>


```C++
HRESULT put_Hue(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="f13e4-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f13e4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f13e4-111">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f13e4-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f13e4-112">Valor de matiz en el que se va a hacer la tecla.</span><span class="sxs-lookup"><span data-stu-id="f13e4-112">The hue value on which to key.</span></span> <span data-ttu-id="f13e4-113">El intervalo válido es de 0 a 360.</span><span class="sxs-lookup"><span data-stu-id="f13e4-113">The valid range is from 0 to 360.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f13e4-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f13e4-114">Return value</span></span>

<span data-ttu-id="f13e4-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f13e4-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f13e4-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f13e4-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f13e4-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f13e4-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f13e4-118">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="f13e4-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f13e4-119">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f13e4-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f13e4-120">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f13e4-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f13e4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f13e4-121">Requirements</span></span>



| <span data-ttu-id="f13e4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f13e4-122">Requirement</span></span> | <span data-ttu-id="f13e4-123">Value</span><span class="sxs-lookup"><span data-stu-id="f13e4-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f13e4-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f13e4-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f13e4-125"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="f13e4-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f13e4-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f13e4-126">Library</span></span><br/> | <dl> <span data-ttu-id="f13e4-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f13e4-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f13e4-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f13e4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f13e4-129">**Interfaz IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="f13e4-129">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="f13e4-130">**IDxtKey::p \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="f13e4-130">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 





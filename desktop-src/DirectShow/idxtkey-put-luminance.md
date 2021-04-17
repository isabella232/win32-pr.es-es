---
description: El \_ método de luminancia Put especifica el valor de luminancia en el que se va a especificar la clave. Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ luminancia.
ms.assetid: 3e255423-1724-49fe-b1a1-49bc1d5fa6ae
title: 'IDxtKey: método de ut_Luminance de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Luminance
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 100f2352b88e9aae2f31ce969302f4bee0905f27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680618"
---
# <a name="idxtkeyput_luminance-method"></a><span data-ttu-id="4ff74-104">IDxtKey: método de luminancia de:p UT \_</span><span class="sxs-lookup"><span data-stu-id="4ff74-104">IDxtKey::put\_Luminance method</span></span>

> [!Note]  
> <span data-ttu-id="4ff74-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="4ff74-105">\[Deprecated.</span></span> <span data-ttu-id="4ff74-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4ff74-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4ff74-107">El `put_Luminance` método especifica el valor de luminancia en el que se va a hacer la tecla.</span><span class="sxs-lookup"><span data-stu-id="4ff74-107">The `put_Luminance` method specifies the luminance value on which to key.</span></span> <span data-ttu-id="4ff74-108">Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ luminancia.</span><span class="sxs-lookup"><span data-stu-id="4ff74-108">This property applies only when the key type is DXTKEY\_LUMINANCE.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ff74-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ff74-109">Syntax</span></span>


```C++
HRESULT put_Luminance(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="4ff74-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ff74-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ff74-111">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4ff74-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ff74-112">Valor de luminancia en el que se va a hacer la tecla.</span><span class="sxs-lookup"><span data-stu-id="4ff74-112">The luminance value on which to key.</span></span> <span data-ttu-id="4ff74-113">El intervalo válido es de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="4ff74-113">The valid range is from 0 to 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ff74-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ff74-114">Return value</span></span>

<span data-ttu-id="4ff74-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4ff74-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4ff74-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4ff74-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ff74-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ff74-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4ff74-118">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="4ff74-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4ff74-119">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4ff74-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4ff74-120">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4ff74-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4ff74-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ff74-121">Requirements</span></span>



| <span data-ttu-id="4ff74-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ff74-122">Requirement</span></span> | <span data-ttu-id="4ff74-123">Value</span><span class="sxs-lookup"><span data-stu-id="4ff74-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ff74-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ff74-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4ff74-125"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ff74-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4ff74-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4ff74-126">Library</span></span><br/> | <dl> <span data-ttu-id="4ff74-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ff74-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ff74-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ff74-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ff74-129">**Interfaz IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="4ff74-129">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="4ff74-130">**IDxtKey::p \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="4ff74-130">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 





---
description: El \_ método get RGB recupera el color RGB en el que se va a incluir la tecla. Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ RGB.
ms.assetid: 7b1b22ff-457a-48c8-9221-ca38601874a9
title: 'Método IDxtKey:: get_RGB (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ef521b28c232f8247ef38858931ae56be6bf2d25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679418"
---
# <a name="idxtkeyget_rgb-method"></a><span data-ttu-id="96201-104">IDxtKey:: get \_ RGB (método)</span><span class="sxs-lookup"><span data-stu-id="96201-104">IDxtKey::get\_RGB method</span></span>

> [!Note]  
> <span data-ttu-id="96201-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="96201-105">\[Deprecated.</span></span> <span data-ttu-id="96201-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="96201-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="96201-107">El `get_RGB` método recupera el color RGB en el que se va a hacer la tecla.</span><span class="sxs-lookup"><span data-stu-id="96201-107">The `get_RGB` method retrieves the RGB color on which to key.</span></span> <span data-ttu-id="96201-108">Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ RGB.</span><span class="sxs-lookup"><span data-stu-id="96201-108">This property applies only when the key type is DXTKEY\_RGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="96201-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96201-109">Syntax</span></span>


```C++
HRESULT get_RGB(
  [out, retval] DWORD *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="96201-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96201-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96201-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="96201-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="96201-112">Recibe el color.</span><span class="sxs-lookup"><span data-stu-id="96201-112">Receives the color.</span></span> <span data-ttu-id="96201-113">El valor devuelto es un número hexadecimal con el formato 0xRRGGBB, donde RR es el valor rojo, GG es el valor verde y BB es el valor azul.</span><span class="sxs-lookup"><span data-stu-id="96201-113">The returned value is a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96201-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96201-114">Return value</span></span>

<span data-ttu-id="96201-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="96201-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="96201-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="96201-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="96201-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96201-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="96201-118">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="96201-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="96201-119">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="96201-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="96201-120">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="96201-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="96201-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96201-121">Requirements</span></span>



| <span data-ttu-id="96201-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="96201-122">Requirement</span></span> | <span data-ttu-id="96201-123">Value</span><span class="sxs-lookup"><span data-stu-id="96201-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96201-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96201-124">Header</span></span><br/>  | <dl> <span data-ttu-id="96201-125"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="96201-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="96201-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="96201-126">Library</span></span><br/> | <dl> <span data-ttu-id="96201-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96201-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96201-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="96201-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96201-129">**Interfaz IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="96201-129">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="96201-130">**IDxtKey:: get \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="96201-130">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 





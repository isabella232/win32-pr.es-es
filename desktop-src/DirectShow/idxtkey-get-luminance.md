---
description: El \_ método get luminancia recupera el valor de luminancia en el que se va a hacer la tecla. Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ luminancia.
ms.assetid: 92113331-a7b7-4618-81b2-ea02e7bcc923
title: 'Método IDxtKey:: get_Luminance (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Luminance
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 85dcba3720e007d0f3de890c085b0b223e3df350
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679420"
---
# <a name="idxtkeyget_luminance-method"></a><span data-ttu-id="3379d-104">IDxtKey:: get \_ luminancia (método)</span><span class="sxs-lookup"><span data-stu-id="3379d-104">IDxtKey::get\_Luminance method</span></span>

> [!Note]  
> <span data-ttu-id="3379d-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="3379d-105">\[Deprecated.</span></span> <span data-ttu-id="3379d-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3379d-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3379d-107">El `get_Luminance` método recupera el valor de luminancia en el que se va a hacer la tecla.</span><span class="sxs-lookup"><span data-stu-id="3379d-107">The `get_Luminance` method retrieves the luminance value on which to key.</span></span> <span data-ttu-id="3379d-108">Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ luminancia.</span><span class="sxs-lookup"><span data-stu-id="3379d-108">This property applies only when the key type is DXTKEY\_LUMINANCE.</span></span>

## <a name="syntax"></a><span data-ttu-id="3379d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3379d-109">Syntax</span></span>


```C++
HRESULT get_Luminance(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="3379d-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3379d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3379d-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3379d-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3379d-112">Recibe el valor de luminancia en el que se va a hacer la tecla.</span><span class="sxs-lookup"><span data-stu-id="3379d-112">Receives the luminance value on which to key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3379d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3379d-113">Return value</span></span>

<span data-ttu-id="3379d-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="3379d-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3379d-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3379d-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3379d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3379d-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3379d-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="3379d-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3379d-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3379d-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3379d-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3379d-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3379d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3379d-120">Requirements</span></span>



| <span data-ttu-id="3379d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3379d-121">Requirement</span></span> | <span data-ttu-id="3379d-122">Value</span><span class="sxs-lookup"><span data-stu-id="3379d-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3379d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3379d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="3379d-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="3379d-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3379d-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3379d-125">Library</span></span><br/> | <dl> <span data-ttu-id="3379d-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3379d-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3379d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3379d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3379d-128">**Interfaz IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="3379d-128">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="3379d-129">**IDxtKey:: get \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="3379d-129">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 





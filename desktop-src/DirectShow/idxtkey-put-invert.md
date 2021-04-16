---
description: El \_ método put Invert especifica si se invierte la operación de clave. Esta propiedad se aplica a todos los tipos de clave excepto DXTKEY \_ Alpha.
ms.assetid: 06acdd9f-eb3a-49bd-961d-00966df2ccb4
title: 'IDxtKey: método de ut_Invert de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3e4b807770d0eeb985c982b61b8390695cc42327
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679413"
---
# <a name="idxtkeyput_invert-method"></a><span data-ttu-id="6801e-104">IDxtKey: método de \_ inversión:p UT</span><span class="sxs-lookup"><span data-stu-id="6801e-104">IDxtKey::put\_Invert method</span></span>

> [!Note]  
> <span data-ttu-id="6801e-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="6801e-105">\[Deprecated.</span></span> <span data-ttu-id="6801e-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6801e-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6801e-107">El `put_Invert` método especifica si se invierte la operación de clave.</span><span class="sxs-lookup"><span data-stu-id="6801e-107">The `put_Invert` method specifies whether the key operation is inverted.</span></span> <span data-ttu-id="6801e-108">Esta propiedad se aplica a todos los tipos de clave excepto DXTKEY \_ Alpha.</span><span class="sxs-lookup"><span data-stu-id="6801e-108">This property applies to all key types except DXTKEY\_ALPHA.</span></span>

## <a name="syntax"></a><span data-ttu-id="6801e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6801e-109">Syntax</span></span>


```C++
HRESULT put_Invert(
  [in] BOOL newVal
);
```



## <a name="parameters"></a><span data-ttu-id="6801e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6801e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6801e-111">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6801e-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6801e-112">Especifica un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="6801e-112">Specifies a Boolean value.</span></span> <span data-ttu-id="6801e-113">Si **es true**, los píxeles de la imagen superpuesta se invierten con respecto a la operación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6801e-113">If **TRUE**, pixels in the overlying image are inverted with respect to the default operation.</span></span> <span data-ttu-id="6801e-114">Si **es false**, los píxeles de la imagen superpuestas se convierten en transparentes de la manera predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6801e-114">If **FALSE**, pixels in the overlying image are made transparent in the default manner.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6801e-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6801e-115">Return value</span></span>

<span data-ttu-id="6801e-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="6801e-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6801e-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6801e-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6801e-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6801e-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6801e-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="6801e-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6801e-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6801e-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6801e-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6801e-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6801e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6801e-122">Requirements</span></span>



| <span data-ttu-id="6801e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6801e-123">Requirement</span></span> | <span data-ttu-id="6801e-124">Value</span><span class="sxs-lookup"><span data-stu-id="6801e-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6801e-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6801e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6801e-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="6801e-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6801e-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6801e-127">Library</span></span><br/> | <dl> <span data-ttu-id="6801e-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6801e-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6801e-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="6801e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6801e-130">**Interfaz IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="6801e-130">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="6801e-131">**IDxtKey::p \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="6801e-131">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 





---
description: El \_ método get Invert recupera un valor booleano que indica si se invierte la operación de clave. Esta propiedad se aplica a todos los tipos de clave excepto DXTKEY \_ Alpha.
ms.assetid: 2ccf2066-3d9c-493b-bc54-a03e7d075531
title: 'Método IDxtKey:: get_Invert (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 51b95758adf6690f6d4fa479ac1cc2c585fa9352
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679423"
---
# <a name="idxtkeyget_invert-method"></a><span data-ttu-id="f6319-104">IDxtKey:: get \_ Invert (método)</span><span class="sxs-lookup"><span data-stu-id="f6319-104">IDxtKey::get\_Invert method</span></span>

> [!Note]  
> <span data-ttu-id="f6319-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="f6319-105">\[Deprecated.</span></span> <span data-ttu-id="f6319-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f6319-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f6319-107">El `get_Invert` método recupera un valor booleano que indica si se invierte la operación de clave.</span><span class="sxs-lookup"><span data-stu-id="f6319-107">The `get_Invert` method retrieves a Boolean value indicating whether the key operation is inverted.</span></span> <span data-ttu-id="f6319-108">Esta propiedad se aplica a todos los tipos de clave excepto DXTKEY \_ Alpha.</span><span class="sxs-lookup"><span data-stu-id="f6319-108">This property applies to all key types except DXTKEY\_ALPHA.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6319-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6319-109">Syntax</span></span>


```C++
HRESULT get_Invert(
  [out, retval] BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="f6319-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6319-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6319-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f6319-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f6319-112">Recibe uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f6319-112">Receives one of the following values.</span></span>



| <span data-ttu-id="f6319-113">Value</span><span class="sxs-lookup"><span data-stu-id="f6319-113">Value</span></span>     | <span data-ttu-id="f6319-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6319-114">Description</span></span>                                                                       |
|-----------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f6319-115">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="f6319-115">**TRUE**</span></span>  | <span data-ttu-id="f6319-116">Los píxeles de la imagen superpuesta se invierten con respecto a la operación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f6319-116">Pixels in the overlying image are inverted with respect to the default operation.</span></span> |
| <span data-ttu-id="f6319-117">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="f6319-117">**FALSE**</span></span> | <span data-ttu-id="f6319-118">Los píxeles de la imagen superpuestas se convierten en transparentes de la manera predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f6319-118">Pixels in the overlying image are made transparent in the default manner.</span></span>         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6319-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6319-119">Return value</span></span>

<span data-ttu-id="f6319-120">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f6319-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f6319-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f6319-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6319-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6319-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f6319-123">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="f6319-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f6319-124">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f6319-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f6319-125">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f6319-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f6319-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6319-126">Requirements</span></span>



| <span data-ttu-id="f6319-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6319-127">Requirement</span></span> | <span data-ttu-id="f6319-128">Value</span><span class="sxs-lookup"><span data-stu-id="f6319-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6319-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6319-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f6319-130"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6319-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f6319-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f6319-131">Library</span></span><br/> | <dl> <span data-ttu-id="f6319-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6319-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6319-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6319-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6319-134">**Interfaz IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="f6319-134">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="f6319-135">**IDxtKey:: get \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="f6319-135">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 





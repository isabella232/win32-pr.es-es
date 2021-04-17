---
description: Función de proxy para el método GetType.
ms.assetid: 04e71352-4f07-4026-bc32-f6926a58c707
title: IWICPalette_GetType_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetType_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: faa027a6366965b232a988daeab063fd902f7805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716447"
---
# <a name="iwicpalette_gettype_proxy-function"></a><span data-ttu-id="dbfbd-103">IWICPalette \_ \_ función de proxy GetType</span><span class="sxs-lookup"><span data-stu-id="dbfbd-103">IWICPalette\_GetType\_Proxy function</span></span>

<span data-ttu-id="dbfbd-104">Función de proxy para el método [**GetType**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-gettype) .</span><span class="sxs-lookup"><span data-stu-id="dbfbd-104">Proxy function for the [**GetType**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-gettype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbfbd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dbfbd-105">Syntax</span></span>


```C++
HRESULT IWICPalette_GetType_Proxy(
  _In_  IWICPalette          *THIS_PTR,
  _Out_ WICBitmapPaletteType *pePaletteType
);
```



## <a name="parameters"></a><span data-ttu-id="dbfbd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dbfbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbfbd-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="dbfbd-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbfbd-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="dbfbd-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="dbfbd-109">Puntero a este objeto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="dbfbd-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="dbfbd-110">*pePaletteType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="dbfbd-110">*pePaletteType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbfbd-111">Tipo: \**[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype) \** _</span><span class="sxs-lookup"><span data-stu-id="dbfbd-111">Type: \**[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)\** _</span></span>

<span data-ttu-id="dbfbd-112">Puntero que recibe el tipo de paleta de bimtap.</span><span class="sxs-lookup"><span data-stu-id="dbfbd-112">Pointer that receives the palette type of the bimtap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbfbd-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dbfbd-113">Return value</span></span>

<span data-ttu-id="dbfbd-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="dbfbd-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="dbfbd-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="dbfbd-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dbfbd-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dbfbd-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbfbd-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dbfbd-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="dbfbd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbfbd-118">Requirements</span></span>



| <span data-ttu-id="dbfbd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbfbd-119">Requirement</span></span> | <span data-ttu-id="dbfbd-120">Value</span><span class="sxs-lookup"><span data-stu-id="dbfbd-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbfbd-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dbfbd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dbfbd-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dbfbd-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="dbfbd-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dbfbd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dbfbd-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="dbfbd-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="dbfbd-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dbfbd-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbfbd-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dbfbd-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 





---
description: Lee un valor textura y devuelve el resultado al host asynchrnously.
MS-HAID: vspixengine.IPixEngine5\_ReadTexelValueAsync\_UINT\_PixEngineTextureSliceIndex\_int\_int\_int\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5:: ReadTexelValueAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 28C44D12-383D-4E91-8BB1-12869782533C
api_name:
- IPixEngine5.ReadTexelValueAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ca3510b01038df3b07b3033364902f76f2e05b4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705243"
---
# <a name="span-idvspixengineipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dwordspanipixengine5readtexelvalueasync-method"></a><span data-ttu-id="d90a4-103"><span id="vspixengine.ipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5:: ReadTexelValueAsync (método)</span><span class="sxs-lookup"><span data-stu-id="d90a4-103"><span id="vspixengine.ipixengine5_readtexelvalueasync_uint_pixenginetexturesliceindex_int_int_int_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::ReadTexelValueAsync method</span></span>

<span data-ttu-id="d90a4-104">Lee un valor textura y devuelve el resultado al host asynchrnously.</span><span class="sxs-lookup"><span data-stu-id="d90a4-104">Reads a texel value and returns the result to the host asynchrnously.</span></span>

## <a name="syntax"></a><span data-ttu-id="d90a4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d90a4-105">Syntax</span></span>


```C++
HRESULT ReadTexelValueAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        x,
   int                        y,
   int                        formatOverride,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="d90a4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d90a4-106">Parameters</span></span>

<span data-ttu-id="d90a4-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="d90a4-107">*textureId* </span></span>  
<span data-ttu-id="d90a4-108">IDENTIFICADOR de la textura de la que se va a leer el valor de textura.</span><span class="sxs-lookup"><span data-stu-id="d90a4-108">The ID of the texture to read the texel value from.</span></span>

<span data-ttu-id="d90a4-109">*sliceIndex* </span><span class="sxs-lookup"><span data-stu-id="d90a4-109">*sliceIndex* </span></span>  
<span data-ttu-id="d90a4-110">Índice del segmento en la textura en el que se va a leer el valor de textura.</span><span class="sxs-lookup"><span data-stu-id="d90a4-110">The index of the slice within the texture to read the texel value from.</span></span>

<span data-ttu-id="d90a4-111">*x1* </span><span class="sxs-lookup"><span data-stu-id="d90a4-111">*x* </span></span>  
<span data-ttu-id="d90a4-112">Coordenada x textura que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="d90a4-112">The x texel coordinate to read.</span></span>

<span data-ttu-id="d90a4-113">*sí* </span><span class="sxs-lookup"><span data-stu-id="d90a4-113">*y* </span></span>  
<span data-ttu-id="d90a4-114">Coordenada y de textura que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="d90a4-114">The y texel coordinate to read.</span></span>

<span data-ttu-id="d90a4-115">*formatOverride* </span><span class="sxs-lookup"><span data-stu-id="d90a4-115">*formatOverride* </span></span>  
<span data-ttu-id="d90a4-116">Invalidación del formato de color.</span><span class="sxs-lookup"><span data-stu-id="d90a4-116">The color format override.</span></span>

<span data-ttu-id="d90a4-117">*devoluciones* </span><span class="sxs-lookup"><span data-stu-id="d90a4-117">*callbacks* </span></span>  
<span data-ttu-id="d90a4-118">La dirección de un objeto que proporciona la interfaz de devoluciones de llamada IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="d90a4-118">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="d90a4-119">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="d90a4-119">*requestCookie* </span></span>  
<span data-ttu-id="d90a4-120">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="d90a4-120">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="d90a4-121">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="d90a4-121">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="d90a4-122">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d90a4-122">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="d90a4-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d90a4-123">Return value</span></span>

<span data-ttu-id="d90a4-124">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d90a4-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d90a4-125">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d90a4-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d90a4-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d90a4-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d90a4-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d90a4-127">Header</span></span></p></td><td><span data-ttu-id="d90a4-128">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="d90a4-128">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="d90a4-129"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="d90a4-129"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="d90a4-130">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="d90a4-130">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 

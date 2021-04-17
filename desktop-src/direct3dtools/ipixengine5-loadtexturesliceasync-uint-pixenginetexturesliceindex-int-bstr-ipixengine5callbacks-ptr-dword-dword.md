---
description: Carga un segmento de textura y notifica al host asynchrnously cuando se completa.
MS-HAID: vspixengine.IPixEngine5\_LoadTextureSliceAsync\_UINT\_PixEngineTextureSliceIndex\_int\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5:: LoadTextureSliceAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 520DBB6D-D8F3-451F-942C-BE8428B9ADFF
api_name:
- IPixEngine5.LoadTextureSliceAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 505ccfd6668cbe08b4f62878b5f51e9c20185b41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705223"
---
# <a name="span-idvspixengineipixengine5_loadtexturesliceasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadtexturesliceasync-method"></a><span data-ttu-id="553a2-103"><span id="vspixengine.ipixengine5_loadtexturesliceasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5:: LoadTextureSliceAsync (método)</span><span class="sxs-lookup"><span data-stu-id="553a2-103"><span id="vspixengine.ipixengine5_loadtexturesliceasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::LoadTextureSliceAsync method</span></span>

<span data-ttu-id="553a2-104">Carga un segmento de textura y notifica al host asynchrnously cuando se completa.</span><span class="sxs-lookup"><span data-stu-id="553a2-104">Loads a texture slice and notifies the host asynchrnously when it completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="553a2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="553a2-105">Syntax</span></span>


```C++
HRESULT LoadTextureSliceAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   BSTR                       histogramDataFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="553a2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="553a2-106">Parameters</span></span>

<span data-ttu-id="553a2-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="553a2-107">*textureId* </span></span>  
<span data-ttu-id="553a2-108">IDENTIFICADOR de la textura para la que se va a cargar el segmento.</span><span class="sxs-lookup"><span data-stu-id="553a2-108">The ID of the texture to load the slice for.</span></span>

<span data-ttu-id="553a2-109">*sliceIndex* </span><span class="sxs-lookup"><span data-stu-id="553a2-109">*sliceIndex* </span></span>  
<span data-ttu-id="553a2-110">Índice del segmento que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="553a2-110">The index of the slice to load.</span></span>

<span data-ttu-id="553a2-111">*formatOverride* </span><span class="sxs-lookup"><span data-stu-id="553a2-111">*formatOverride* </span></span>  
<span data-ttu-id="553a2-112">Especifica la invalidación de formato.</span><span class="sxs-lookup"><span data-stu-id="553a2-112">Specifies the format override.</span></span>

<span data-ttu-id="553a2-113">*histogramDataFileName* </span><span class="sxs-lookup"><span data-stu-id="553a2-113">*histogramDataFileName* </span></span>  
<span data-ttu-id="553a2-114">Cadena COM que contiene el nombre del archivo de datos de histograma asociado al segmento de textura.</span><span class="sxs-lookup"><span data-stu-id="553a2-114">A COM string containing the name of the histogram data file associated with the texture slice.</span></span>

<span data-ttu-id="553a2-115">*devoluciones* </span><span class="sxs-lookup"><span data-stu-id="553a2-115">*callbacks* </span></span>  
<span data-ttu-id="553a2-116">La dirección de un objeto que proporciona la interfaz de devoluciones de llamada IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="553a2-116">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="553a2-117">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="553a2-117">*requestCookie* </span></span>  
<span data-ttu-id="553a2-118">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="553a2-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="553a2-119">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="553a2-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="553a2-120">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="553a2-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="553a2-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="553a2-121">Return value</span></span>

<span data-ttu-id="553a2-122">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="553a2-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="553a2-123">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="553a2-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="553a2-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="553a2-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="553a2-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="553a2-125">Header</span></span></p></td><td><span data-ttu-id="553a2-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="553a2-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="553a2-127"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="553a2-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="553a2-128">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="553a2-128">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 

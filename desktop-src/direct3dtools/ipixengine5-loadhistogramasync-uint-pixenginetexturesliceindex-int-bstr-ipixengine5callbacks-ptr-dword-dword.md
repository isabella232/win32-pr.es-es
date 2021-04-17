---
description: Una solicitud asincrónica para cargar datos de histograma.
MS-HAID: vspixengine.IPixEngine5\_LoadHistogramAsync\_UINT\_PixEngineTextureSliceIndex\_int\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5:: LoadHistogramAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A23CB3E0-B299-40FD-899E-9FE6E9177551
api_name:
- IPixEngine5.LoadHistogramAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7c7128743c2086c0ddc2875c493dac98617986a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705244"
---
# <a name="span-idvspixengineipixengine5_loadhistogramasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadhistogramasync-method"></a><span data-ttu-id="a315d-103"><span id="vspixengine.ipixengine5_loadhistogramasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5:: LoadHistogramAsync (método)</span><span class="sxs-lookup"><span data-stu-id="a315d-103"><span id="vspixengine.ipixengine5_loadhistogramasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::LoadHistogramAsync method</span></span>

<span data-ttu-id="a315d-104">Una solicitud asincrónica para cargar datos de histograma.</span><span class="sxs-lookup"><span data-stu-id="a315d-104">An asynchronous request to load histogram data.</span></span>

## <a name="syntax"></a><span data-ttu-id="a315d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a315d-105">Syntax</span></span>


```C++
HRESULT LoadHistogramAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   BSTR                       histogramDataFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="a315d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a315d-106">Parameters</span></span>

<span data-ttu-id="a315d-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="a315d-107">*textureId* </span></span>  
<span data-ttu-id="a315d-108">IDENTIFICADOR de la textura para la que se van a cargar los datos del histograma.</span><span class="sxs-lookup"><span data-stu-id="a315d-108">The ID of the texture to load histogram data for.</span></span>

<span data-ttu-id="a315d-109">*sliceIndex* </span><span class="sxs-lookup"><span data-stu-id="a315d-109">*sliceIndex* </span></span>  
<span data-ttu-id="a315d-110">Índice del segmento para el que se van a cargar datos de histograma.</span><span class="sxs-lookup"><span data-stu-id="a315d-110">The index of the slice to load histogram data for.</span></span>

<span data-ttu-id="a315d-111">*formatOverride* </span><span class="sxs-lookup"><span data-stu-id="a315d-111">*formatOverride* </span></span>  
<span data-ttu-id="a315d-112">Especifica la invalidación de formato.</span><span class="sxs-lookup"><span data-stu-id="a315d-112">Specifies the format override.</span></span>

<span data-ttu-id="a315d-113">*histogramDataFileName* </span><span class="sxs-lookup"><span data-stu-id="a315d-113">*histogramDataFileName* </span></span>  
<span data-ttu-id="a315d-114">Cadena COM que contiene el nombre del archivo de datos del histograma.</span><span class="sxs-lookup"><span data-stu-id="a315d-114">A COM string containing the name of the histogram data file.</span></span>

<span data-ttu-id="a315d-115">*devoluciones* </span><span class="sxs-lookup"><span data-stu-id="a315d-115">*callbacks* </span></span>  
<span data-ttu-id="a315d-116">La dirección de un objeto que proporciona la interfaz de devoluciones de llamada IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="a315d-116">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="a315d-117">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="a315d-117">*requestCookie* </span></span>  
<span data-ttu-id="a315d-118">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="a315d-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="a315d-119">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="a315d-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="a315d-120">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="a315d-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="a315d-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a315d-121">Return value</span></span>

<span data-ttu-id="a315d-122">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a315d-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a315d-123">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a315d-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a315d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a315d-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a315d-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a315d-125">Header</span></span></p></td><td><span data-ttu-id="a315d-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a315d-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a315d-127"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="a315d-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a315d-128">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="a315d-128">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 

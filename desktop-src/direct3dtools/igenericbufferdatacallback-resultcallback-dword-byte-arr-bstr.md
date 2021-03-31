---
description: Devolución de llamada que notifica al host la información de búfer genérico devuelta por la solicitud asociada.
MS-HAID: vspixengine.IGenericBufferDataCallback\_ResultCallback\_DWORD\_BYTE\_arr\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IGenericBufferDataCallback:: ResultCallback (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5627A93E-8BE8-4413-BFB4-724AF2DDFEB6
api_name:
- IGenericBufferDataCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: be2d6aa7cd5e844cd5d1297c16de2ebb21c939a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806512"
---
# <a name="span-idvspixengineigenericbufferdatacallback_resultcallback_dword_byte_arr_bstrspanigenericbufferdatacallbackresultcallback-method"></a><span data-ttu-id="c398d-103"><span id="vspixengine.igenericbufferdatacallback_resultcallback_dword_byte_arr_bstr"></span>IGenericBufferDataCallback:: ResultCallback (método)</span><span class="sxs-lookup"><span data-stu-id="c398d-103"><span id="vspixengine.igenericbufferdatacallback_resultcallback_dword_byte_arr_bstr"></span>IGenericBufferDataCallback::ResultCallback method</span></span>

<span data-ttu-id="c398d-104">Devolución de llamada que notifica al host la información de búfer genérico devuelta por la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="c398d-104">A callback that notifies the host of generic buffer information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="c398d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c398d-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD   size,
   BYTE [] count0_buffer,
   BSTR    type
);
```

## <a name="parameters"></a><span data-ttu-id="c398d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c398d-106">Parameters</span></span>

<span data-ttu-id="c398d-107">*ajusta* </span><span class="sxs-lookup"><span data-stu-id="c398d-107">*size* </span></span>  
<span data-ttu-id="c398d-108">Tamaño del contenido del búfer en bytes.</span><span class="sxs-lookup"><span data-stu-id="c398d-108">The size of the buffer contents in bytes.</span></span>

<span data-ttu-id="c398d-109">*\_búfer count0* </span><span class="sxs-lookup"><span data-stu-id="c398d-109">*count0\_buffer* </span></span>  
<span data-ttu-id="c398d-110">Contenido del búfer.</span><span class="sxs-lookup"><span data-stu-id="c398d-110">The buffer contents.</span></span> <span data-ttu-id="c398d-111">En la mayoría de los casos, se trata de datos XML.</span><span class="sxs-lookup"><span data-stu-id="c398d-111">In most cases this is XML data.</span></span>

<span data-ttu-id="c398d-112">*type* </span><span class="sxs-lookup"><span data-stu-id="c398d-112">*type* </span></span>  
<span data-ttu-id="c398d-113">Cadena COM que indica el tipo de contenido devuelto en el búfer.</span><span class="sxs-lookup"><span data-stu-id="c398d-113">A COM string that indicates the type of content returned in the buffer.</span></span>

## <a name="return-value"></a><span data-ttu-id="c398d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c398d-114">Return value</span></span>

<span data-ttu-id="c398d-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c398d-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c398d-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c398d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c398d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c398d-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c398d-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c398d-118">Header</span></span></p></td><td><span data-ttu-id="c398d-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c398d-119">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c398d-120"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="c398d-120"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c398d-121">**IGenericBufferDataCallback**</span><span class="sxs-lookup"><span data-stu-id="c398d-121">**IGenericBufferDataCallback**</span></span>](/windows/desktop/direct3dtools/igenericbufferdatacallback)

 

 

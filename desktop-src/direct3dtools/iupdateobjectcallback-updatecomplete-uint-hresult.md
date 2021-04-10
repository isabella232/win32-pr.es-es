---
description: Devolución de llamada que se usa para notificar al host que se ha actualizado un objeto.
MS-HAID: vspixengine.IUpdateObjectCallback\_UpdateComplete\_UINT\_HRESULT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IUpdateObjectCallback:: UpdateComplete (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7F54DDEC-E595-4615-B9B7-B1213A58B362
api_name:
- IUpdateObjectCallback.UpdateComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b601d8ac785f65c4400821741b83e76bd6987481
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152394"
---
# <a name="span-idvspixengineiupdateobjectcallback_updatecomplete_uint_hresultspaniupdateobjectcallbackupdatecomplete-method"></a><span data-ttu-id="c9e95-103"><span id="vspixengine.iupdateobjectcallback_updatecomplete_uint_hresult"></span>IUpdateObjectCallback:: UpdateComplete (método)</span><span class="sxs-lookup"><span data-stu-id="c9e95-103"><span id="vspixengine.iupdateobjectcallback_updatecomplete_uint_hresult"></span>IUpdateObjectCallback::UpdateComplete method</span></span>

<span data-ttu-id="c9e95-104">Devolución de llamada que se usa para notificar al host que se ha actualizado un objeto.</span><span class="sxs-lookup"><span data-stu-id="c9e95-104">A callback used to notify the host that an object was updated.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9e95-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9e95-105">Syntax</span></span>


```C++
HRESULT UpdateComplete(
   UINT    objectAddress,
   HRESULT result
);
```

## <a name="parameters"></a><span data-ttu-id="c9e95-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9e95-106">Parameters</span></span>

<span data-ttu-id="c9e95-107">*objectAddress* </span><span class="sxs-lookup"><span data-stu-id="c9e95-107">*objectAddress* </span></span>  
<span data-ttu-id="c9e95-108">IDENTIFICADOR del objeto que se actualizó.</span><span class="sxs-lookup"><span data-stu-id="c9e95-108">The ID of the object that was updated.</span></span>

<span data-ttu-id="c9e95-109">*da* </span><span class="sxs-lookup"><span data-stu-id="c9e95-109">*result* </span></span>  
<span data-ttu-id="c9e95-110">Indica si la actualización se realizó correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="c9e95-110">Indicates whether or not the update succeeded.</span></span>

## <a name="return-value"></a><span data-ttu-id="c9e95-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9e95-111">Return value</span></span>

<span data-ttu-id="c9e95-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c9e95-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c9e95-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c9e95-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9e95-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9e95-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c9e95-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9e95-115">Header</span></span></p></td><td><span data-ttu-id="c9e95-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c9e95-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c9e95-117"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="c9e95-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c9e95-118">**IUpdateObjectCallback**</span><span class="sxs-lookup"><span data-stu-id="c9e95-118">**IUpdateObjectCallback**</span></span>](/windows/desktop/direct3dtools/iupdateobjectcallback)

 

 

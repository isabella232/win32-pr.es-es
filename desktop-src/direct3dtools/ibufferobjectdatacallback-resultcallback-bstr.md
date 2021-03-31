---
description: Devolución de llamada que notifica al host la información del búfer escrita en un archivo mediante la solicitud asociada.
MS-HAID: vspixengine.IBufferObjectDataCallback\_ResultCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IBufferObjectDataCallback:: ResultCallback (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C8083FDF-0A56-4777-8EFD-66F77AD195EA
api_name:
- IBufferObjectDataCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 41a5017171fee8476033e3c38d050bc38b1642a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423143"
---
# <a name="span-idvspixengineibufferobjectdatacallback_resultcallback_bstrspanibufferobjectdatacallbackresultcallback-method"></a><span data-ttu-id="18bca-103"><span id="vspixengine.ibufferobjectdatacallback_resultcallback_bstr"></span>IBufferObjectDataCallback:: ResultCallback (método)</span><span class="sxs-lookup"><span data-stu-id="18bca-103"><span id="vspixengine.ibufferobjectdatacallback_resultcallback_bstr"></span>IBufferObjectDataCallback::ResultCallback method</span></span>

<span data-ttu-id="18bca-104">Devolución de llamada que notifica al host la información del búfer escrita en un archivo mediante la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="18bca-104">A callback that notifies the host of buffer information written to a file by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="18bca-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18bca-105">Syntax</span></span>

```C++
HRESULT ResultCallback(
   BSTR File
);
```

## <a name="parameters"></a><span data-ttu-id="18bca-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18bca-106">Parameters</span></span>

<span data-ttu-id="18bca-107">*Archivo* de Cadena COM que contiene la ruta de acceso del archivo donde se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="18bca-107">*File* A COM string that contains the pathname of the file where results are written.</span></span>

## <a name="return-value"></a><span data-ttu-id="18bca-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18bca-108">Return value</span></span>

<span data-ttu-id="18bca-109">Si este método se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="18bca-109">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="18bca-110">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="18bca-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="18bca-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18bca-111">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="18bca-112">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18bca-112">Header</span></span></p></td><td><span data-ttu-id="18bca-113">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="18bca-113">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="18bca-114"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="18bca-114"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="18bca-115">**IBufferObjectDataCallback**</span><span class="sxs-lookup"><span data-stu-id="18bca-115">**IBufferObjectDataCallback**</span></span>](/windows/desktop/direct3dtools/ibufferobjectdatacallback)

 

 

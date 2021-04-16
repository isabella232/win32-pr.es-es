---
description: Solicita obtener información sobre las columnas (campos) que admite este tipo de solicitud de tabla de objetos.
MS-HAID: vspixengine.IObjectTableRequest\_RequestSupportedColumnsAsync\_IObjectTableCallback\_ptr\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IObjectTableRequest:: RequestSupportedColumnsAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0931C81A-65D5-493E-9F54-C7E98FA2FA6F
api_name:
- IObjectTableRequest.RequestSupportedColumnsAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6773a69061e7a17d2271e1a53f89f6f2def1a6c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538212"
---
# <a name="span-idvspixengineiobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dwordspaniobjecttablerequestrequestsupportedcolumnsasync-method"></a><span data-ttu-id="130ec-103"><span id="vspixengine.iobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dword"></span>IObjectTableRequest:: RequestSupportedColumnsAsync (método)</span><span class="sxs-lookup"><span data-stu-id="130ec-103"><span id="vspixengine.iobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dword"></span>IObjectTableRequest::RequestSupportedColumnsAsync method</span></span>

<span data-ttu-id="130ec-104">Solicita obtener información sobre las columnas (campos) que admite este tipo de solicitud de tabla de objetos.</span><span class="sxs-lookup"><span data-stu-id="130ec-104">Requests to get information about what columns (fields) this object table request type supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="130ec-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="130ec-105">Syntax</span></span>


```C++
HRESULT RequestSupportedColumnsAsync(
   IObjectTableCallback * requestCallback,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="130ec-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="130ec-106">Parameters</span></span>

<span data-ttu-id="130ec-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="130ec-107">*requestCallback* </span></span>  
<span data-ttu-id="130ec-108">Dirección de devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="130ec-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="130ec-109">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="130ec-109">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="130ec-110">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="130ec-110">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="130ec-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="130ec-111">Return value</span></span>

<span data-ttu-id="130ec-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="130ec-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="130ec-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="130ec-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="130ec-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="130ec-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="130ec-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="130ec-115">Header</span></span></p></td><td><span data-ttu-id="130ec-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="130ec-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="130ec-117"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="130ec-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="130ec-118">**IObjectTableRequest**</span><span class="sxs-lookup"><span data-stu-id="130ec-118">**IObjectTableRequest**</span></span>](/windows/desktop/direct3dtools/iobjecttablerequest)

 

 

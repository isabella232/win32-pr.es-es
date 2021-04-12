---
description: Conéctese a otra instancia de un motor remoto en el equipo local.
MS-HAID: vspixengine.IServerConnectionCallback\_ConnectToEngine\_BOOL\_BSTR\_IPixEngine\_ptr\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IServerConnectionCallback:: ConnectToEngine (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 56D67449-EA8B-4AD0-94D7-B3CDB7F0ABC8
api_name:
- IServerConnectionCallback.ConnectToEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1506075066767cba95c7fec768fa27e858bd6a10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152615"
---
# <a name="span-idvspixengineiserverconnectioncallback_connecttoengine_bool_bstr_ipixengine_ptr_ptrspaniserverconnectioncallbackconnecttoengine-method"></a><span data-ttu-id="309e8-103"><span id="vspixengine.iserverconnectioncallback_connecttoengine_bool_bstr_ipixengine_ptr_ptr"></span>IServerConnectionCallback:: ConnectToEngine (método)</span><span class="sxs-lookup"><span data-stu-id="309e8-103"><span id="vspixengine.iserverconnectioncallback_connecttoengine_bool_bstr_ipixengine_ptr_ptr"></span>IServerConnectionCallback::ConnectToEngine method</span></span>

<span data-ttu-id="309e8-104">Conéctese a otra instancia de un motor remoto en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="309e8-104">Connect to another instance of a remote engine on the local machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="309e8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="309e8-105">Syntax</span></span>


```C++
HRESULT ConnectToEngine(
   BOOL          bLegacyConnection,
   BSTR          runAddress,
   IPixEngine ** ppEngineCreated
);
```

## <a name="parameters"></a><span data-ttu-id="309e8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="309e8-106">Parameters</span></span>

<span data-ttu-id="309e8-107">*bLegacyConnection* </span><span class="sxs-lookup"><span data-stu-id="309e8-107">*bLegacyConnection* </span></span>  
<span data-ttu-id="309e8-108">True si el motor utiliza es heredado; de lo contrario, false.</span><span class="sxs-lookup"><span data-stu-id="309e8-108">true if the engine uses is legacy, otherwise false.</span></span>

<span data-ttu-id="309e8-109">*runAddress* </span><span class="sxs-lookup"><span data-stu-id="309e8-109">*runAddress* </span></span>  
<span data-ttu-id="309e8-110">Cadena COM que contiene el nombre del equipo local.</span><span class="sxs-lookup"><span data-stu-id="309e8-110">A COM string containing the name of the local machine.</span></span>

<span data-ttu-id="309e8-111">*ppEngineCreated* </span><span class="sxs-lookup"><span data-stu-id="309e8-111">*ppEngineCreated* </span></span>  
<span data-ttu-id="309e8-112">En la devolución, la dirección de la instancia del motor.</span><span class="sxs-lookup"><span data-stu-id="309e8-112">On return, the address of the engine instance.</span></span>

## <a name="return-value"></a><span data-ttu-id="309e8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="309e8-113">Return value</span></span>

<span data-ttu-id="309e8-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="309e8-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="309e8-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="309e8-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="309e8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="309e8-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="309e8-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="309e8-117">Header</span></span></p></td><td><span data-ttu-id="309e8-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="309e8-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="309e8-119"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="309e8-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="309e8-120">**IServerConnectionCallback**</span><span class="sxs-lookup"><span data-stu-id="309e8-120">**IServerConnectionCallback**</span></span>](/windows/desktop/direct3dtools/iserverconnectioncallback)

 

 

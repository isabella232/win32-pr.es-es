---
description: Establece de forma asincrónica la dirección del punto de conexión utilizada para conectarse a un motor remoto.
MS-HAID: vspixengine.IPixEngine7\_SetPlaybackEndpointAsync\_BOOL\_BSTR\_BSTR\_RemotingVersion\_IVersionCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine7:: SetPlaybackEndpointAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4F76EFFF-F3CB-4BEA-999F-639876C7F792
api_name:
- IPixEngine7.SetPlaybackEndpointAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2e0970b1a2a786c828a24efef0ae9e4057dbe2cc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806691"
---
# <a name="span-idvspixengineipixengine7_setplaybackendpointasync_bool_bstr_bstr_remotingversion_iversioncallback_ptr_dword_dwordspanipixengine7setplaybackendpointasync-method"></a><span data-ttu-id="2924d-103"><span id="vspixengine.ipixengine7_setplaybackendpointasync_bool_bstr_bstr_remotingversion_iversioncallback_ptr_dword_dword"></span>IPixEngine7:: SetPlaybackEndpointAsync (método)</span><span class="sxs-lookup"><span data-stu-id="2924d-103"><span id="vspixengine.ipixengine7_setplaybackendpointasync_bool_bstr_bstr_remotingversion_iversioncallback_ptr_dword_dword"></span>IPixEngine7::SetPlaybackEndpointAsync method</span></span>

<span data-ttu-id="2924d-104">Establece de forma asincrónica la dirección del punto de conexión utilizada para conectarse a un motor remoto.</span><span class="sxs-lookup"><span data-stu-id="2924d-104">Asynchronously sets the endpoint address used to connect to a remote engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="2924d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2924d-105">Syntax</span></span>


```C++
HRESULT SetPlaybackEndpointAsync(
   BOOL              bUseAuthentication,
   BSTR              endpoint,
   BSTR              sessionKey,
   RemotingVersion   remoteVersion,
   IVersionCallback* versionCallback,
   DWORD             requestCookie,
   DWORD             progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="2924d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2924d-106">Parameters</span></span>

<span data-ttu-id="2924d-107">*bUseAuthentication* </span><span class="sxs-lookup"><span data-stu-id="2924d-107">*bUseAuthentication* </span></span>  
<span data-ttu-id="2924d-108">True para utilizar la autenticación; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="2924d-108">true to use authentication; otherwise, false.</span></span>

<span data-ttu-id="2924d-109">*finales* </span><span class="sxs-lookup"><span data-stu-id="2924d-109">*endpoint* </span></span>  
<span data-ttu-id="2924d-110">Cadena COM que contiene la dirección del extremo.</span><span class="sxs-lookup"><span data-stu-id="2924d-110">A COM string containing the endpoint address.</span></span>

<span data-ttu-id="2924d-111">*sessionKey* </span><span class="sxs-lookup"><span data-stu-id="2924d-111">*sessionKey* </span></span>  
<span data-ttu-id="2924d-112">Cadena COM que contiene la clave de sesión utilizada para el cifrado.</span><span class="sxs-lookup"><span data-stu-id="2924d-112">A COM string containing the session key used for encryption.</span></span>

<span data-ttu-id="2924d-113">*remoteVersion* </span><span class="sxs-lookup"><span data-stu-id="2924d-113">*remoteVersion* </span></span>  
<span data-ttu-id="2924d-114">Especifica la versión del motor remoto que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="2924d-114">Specifies the version of the remote engine to use.</span></span>

<span data-ttu-id="2924d-115">*versionCallback* </span><span class="sxs-lookup"><span data-stu-id="2924d-115">*versionCallback* </span></span>  
<span data-ttu-id="2924d-116">Dirección de devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="2924d-116">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="2924d-117">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="2924d-117">*requestCookie* </span></span>  
<span data-ttu-id="2924d-118">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="2924d-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="2924d-119">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="2924d-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="2924d-120">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="2924d-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="2924d-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2924d-121">Return value</span></span>

<span data-ttu-id="2924d-122">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="2924d-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2924d-123">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2924d-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2924d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2924d-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="2924d-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2924d-125">Header</span></span></p></td><td><span data-ttu-id="2924d-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="2924d-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="2924d-127"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="2924d-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="2924d-128">**IPixEngine7**</span><span class="sxs-lookup"><span data-stu-id="2924d-128">**IPixEngine7**</span></span>](/windows/desktop/direct3dtools/ipixengine7)

 

 

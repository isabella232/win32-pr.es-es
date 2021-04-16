---
description: Obtiene la dirección del extremo de un motor remoto.
MS-HAID: vspixengine.IPeerToPeerEngine\_GetPlaybackEndpoint\_BOOL\_BSTR\_ptr\_BSTR\_ptr\_RemotingVersion\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPeerToPeerEngine:: GetPlaybackEndpoint (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3B391048-E7F7-4DA7-96A3-05875B170DCA
api_name:
- IPeerToPeerEngine.GetPlaybackEndpoint
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f6ee25dbd456086227e88fcb8bf7708a39e26eb7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537011"
---
# <a name="span-idvspixengineipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptrspanipeertopeerenginegetplaybackendpoint-method"></a><span data-ttu-id="3b089-103"><span id="vspixengine.ipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptr"></span>IPeerToPeerEngine:: GetPlaybackEndpoint (método)</span><span class="sxs-lookup"><span data-stu-id="3b089-103"><span id="vspixengine.ipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptr"></span>IPeerToPeerEngine::GetPlaybackEndpoint method</span></span>

<span data-ttu-id="3b089-104">Obtiene la dirección del extremo de un motor remoto.</span><span class="sxs-lookup"><span data-stu-id="3b089-104">Gets the endpoint address of a remote engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b089-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b089-105">Syntax</span></span>


```C++
HRESULT GetPlaybackEndpoint(
   BOOL              bUseAuthentication,
   BSTR *            pEndpoint,
   BSTR *            sessionKey,
   RemotingVersion * pRemoteVersion
);
```

## <a name="parameters"></a><span data-ttu-id="3b089-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b089-106">Parameters</span></span>

<span data-ttu-id="3b089-107">*bUseAuthentication* </span><span class="sxs-lookup"><span data-stu-id="3b089-107">*bUseAuthentication* </span></span>  
<span data-ttu-id="3b089-108">True si el motor remoto utiliza la autenticación; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="3b089-108">true if the remote engine uses authentication; otherwise, false.</span></span>

<span data-ttu-id="3b089-109">*pEndpoint* </span><span class="sxs-lookup"><span data-stu-id="3b089-109">*pEndpoint* </span></span>  
<span data-ttu-id="3b089-110">En la devolución, cadena COM que contiene la dirección del extremo del equipo de reproducción remota.</span><span class="sxs-lookup"><span data-stu-id="3b089-110">On return, a COM string containing the endpoint address of the remote playback machine.</span></span>

<span data-ttu-id="3b089-111">*sessionKey* </span><span class="sxs-lookup"><span data-stu-id="3b089-111">*sessionKey* </span></span>  
<span data-ttu-id="3b089-112">En la devolución, cadena COM que contiene la clave de sesión utilizada para el cifrado.</span><span class="sxs-lookup"><span data-stu-id="3b089-112">On return, a COM string containing the session key used for encryption.</span></span>

<span data-ttu-id="3b089-113">*pRemoteVersion* </span><span class="sxs-lookup"><span data-stu-id="3b089-113">*pRemoteVersion* </span></span>  
<span data-ttu-id="3b089-114">En la devolución, la versión del motor remoto.</span><span class="sxs-lookup"><span data-stu-id="3b089-114">On return, the version of the remote engine.</span></span>

## <a name="return-value"></a><span data-ttu-id="3b089-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b089-115">Return value</span></span>

<span data-ttu-id="3b089-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="3b089-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3b089-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3b089-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b089-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b089-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3b089-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b089-119">Header</span></span></p></td><td><span data-ttu-id="3b089-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="3b089-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="3b089-121"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="3b089-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="3b089-122">**IPeerToPeerEngine**</span><span class="sxs-lookup"><span data-stu-id="3b089-122">**IPeerToPeerEngine**</span></span>](/windows/desktop/direct3dtools/ipeertopeerengine)

 

 

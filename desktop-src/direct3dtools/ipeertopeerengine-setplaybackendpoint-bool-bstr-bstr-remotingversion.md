---
description: Establece la dirección del extremo utilizada para conectarse a un motor remoto.
MS-HAID: vspixengine.IPeerToPeerEngine\_SetPlaybackEndpoint\_BOOL\_BSTR\_BSTR\_RemotingVersion
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPeerToPeerEngine:: SetPlaybackEndpoint (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D261D2EA-C930-406E-A5E1-CE5E98162399
api_name:
- IPeerToPeerEngine.SetPlaybackEndpoint
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bbec4826fb2659604a4b9f4388beed1829b42770
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495557"
---
# <a name="span-idvspixengineipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversionspanipeertopeerenginesetplaybackendpoint-method"></a><span data-ttu-id="2e3ab-103"><span id="vspixengine.ipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversion"></span>IPeerToPeerEngine:: SetPlaybackEndpoint (método)</span><span class="sxs-lookup"><span data-stu-id="2e3ab-103"><span id="vspixengine.ipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversion"></span>IPeerToPeerEngine::SetPlaybackEndpoint method</span></span>

<span data-ttu-id="2e3ab-104">Establece la dirección del extremo utilizada para conectarse a un motor remoto.</span><span class="sxs-lookup"><span data-stu-id="2e3ab-104">Sets the endpoint address used to connect to a remote engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e3ab-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e3ab-105">Syntax</span></span>


```C++
HRESULT SetPlaybackEndpoint(
   BOOL            bUseAuthentication,
   BSTR            endpoint,
   BSTR            sessionKey,
   RemotingVersion remoteVersion
);
```

## <a name="parameters"></a><span data-ttu-id="2e3ab-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e3ab-106">Parameters</span></span>

<span data-ttu-id="2e3ab-107">*bUseAuthentication* </span><span class="sxs-lookup"><span data-stu-id="2e3ab-107">*bUseAuthentication* </span></span>  
<span data-ttu-id="2e3ab-108">True para utilizar la autenticación; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="2e3ab-108">true to use authentication; otherwise, false.</span></span>

<span data-ttu-id="2e3ab-109">*finales* </span><span class="sxs-lookup"><span data-stu-id="2e3ab-109">*endpoint* </span></span>  
<span data-ttu-id="2e3ab-110">Cadena COM que contiene la dirección del extremo.</span><span class="sxs-lookup"><span data-stu-id="2e3ab-110">A COM string containing the endpoint address.</span></span>

<span data-ttu-id="2e3ab-111">*sessionKey* </span><span class="sxs-lookup"><span data-stu-id="2e3ab-111">*sessionKey* </span></span>  
<span data-ttu-id="2e3ab-112">Cadena COM que contiene la clave de sesión utilizada para el cifrado.</span><span class="sxs-lookup"><span data-stu-id="2e3ab-112">A COM string containing the session key used for encryption.</span></span>

<span data-ttu-id="2e3ab-113">*remoteVersion* </span><span class="sxs-lookup"><span data-stu-id="2e3ab-113">*remoteVersion* </span></span>  
<span data-ttu-id="2e3ab-114">Especifica la versión del motor remoto que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="2e3ab-114">Specifies the version of the remote engine to use.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e3ab-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e3ab-115">Return value</span></span>

<span data-ttu-id="2e3ab-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="2e3ab-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2e3ab-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2e3ab-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e3ab-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e3ab-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="2e3ab-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e3ab-119">Header</span></span></p></td><td><span data-ttu-id="2e3ab-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="2e3ab-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="2e3ab-121"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="2e3ab-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="2e3ab-122">**IPeerToPeerEngine**</span><span class="sxs-lookup"><span data-stu-id="2e3ab-122">**IPeerToPeerEngine**</span></span>](/windows/desktop/direct3dtools/ipeertopeerengine)

 

 

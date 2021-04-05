---
description: La estructura UpdateEndpointProxySettings define la configuración de proxy utilizada al solicitar un token.
ms.assetid: 24AA8843-D4EE-4F17-8B96-63ED25B365D2
title: Estructura UpdateEndpointProxySettings (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointProxySettings
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: aad6ad294baab37b7516152438dbc9fd05f7036a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082171"
---
# <a name="updateendpointproxysettings-structure"></a><span data-ttu-id="afa3a-103">Estructura UpdateEndpointProxySettings</span><span class="sxs-lookup"><span data-stu-id="afa3a-103">UpdateEndpointProxySettings structure</span></span>

<span data-ttu-id="afa3a-104">La estructura **UpdateEndpointProxySettings** define la configuración de proxy utilizada al solicitar un token.</span><span class="sxs-lookup"><span data-stu-id="afa3a-104">The **UpdateEndpointProxySettings** structure defines the proxy settings used when requesting a token.</span></span>

## <a name="syntax"></a><span data-ttu-id="afa3a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="afa3a-105">Syntax</span></span>


```C++
typedef struct tagUpdateEndpointProxySettings {
  BSTR szProxyAddr;
  BSTR szBypassList;
  BSTR szUserName;
  BSTR szPassword;
} UpdateEndpointProxySettings;
```



## <a name="members"></a><span data-ttu-id="afa3a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="afa3a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="afa3a-107">**szProxyAddr**</span><span class="sxs-lookup"><span data-stu-id="afa3a-107">**szProxyAddr**</span></span>
</dt> <dd>

<span data-ttu-id="afa3a-108">Nombre DNS o dirección IP del servidor proxy que se va a usar (por ejemplo, "proxy.somecorp.com" o "192.168.0.4") o una cadena vacía si no se debe utilizar ningún proxy.</span><span class="sxs-lookup"><span data-stu-id="afa3a-108">The DNS name or IP address of the proxy server to use (for example, "proxy.somecorp.com" or "192.168.0.4"), or an empty string if no proxy should be used.</span></span>

</dd> <dt>

<span data-ttu-id="afa3a-109">**szBypassList**</span><span class="sxs-lookup"><span data-stu-id="afa3a-109">**szBypassList**</span></span>
</dt> <dd>

<span data-ttu-id="afa3a-110">Una lista de direcciones de host que deben omitir el servidor proxy o una cadena vacía si todas las direcciones de host deben usar el servidor proxy</span><span class="sxs-lookup"><span data-stu-id="afa3a-110">A list of host addresses that should bypass the proxy server, or an empty string if all host addresses should use the proxy server</span></span>

<span data-ttu-id="afa3a-111">WUA no utiliza estos datos si **szProxyAddr** está vacío.</span><span class="sxs-lookup"><span data-stu-id="afa3a-111">WUA does not use this data if **szProxyAddr** is empty.</span></span>

</dd> <dt>

<span data-ttu-id="afa3a-112">**szUserName**</span><span class="sxs-lookup"><span data-stu-id="afa3a-112">**szUserName**</span></span>
</dt> <dd>

<span data-ttu-id="afa3a-113">El nombre de usuario que se usa para autenticarse con el servidor proxy, o la cadena vacía si no se necesita autenticación.</span><span class="sxs-lookup"><span data-stu-id="afa3a-113">The username that is used to authenticate with the proxy server, or the empty string if no authentication is needed.</span></span>

<span data-ttu-id="afa3a-114">WUA no utiliza estos datos si **szProxyAddr** está vacío.</span><span class="sxs-lookup"><span data-stu-id="afa3a-114">WUA does not use this data if **szProxyAddr** is empty.</span></span>

</dd> <dt>

<span data-ttu-id="afa3a-115">**szPassword**</span><span class="sxs-lookup"><span data-stu-id="afa3a-115">**szPassword**</span></span>
</dt> <dd>

<span data-ttu-id="afa3a-116">La contraseña que se usa para autenticarse con el servidor proxy, o la cadena vacía si no se necesita autenticación.</span><span class="sxs-lookup"><span data-stu-id="afa3a-116">The password that is used to authenticate with the proxy server, or the empty string if no authentication is needed.</span></span>

<span data-ttu-id="afa3a-117">WUA no utiliza estos datos si **szProxyAddr** está vacío.</span><span class="sxs-lookup"><span data-stu-id="afa3a-117">WUA does not use this data if **szProxyAddr** is empty.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="afa3a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afa3a-118">Requirements</span></span>



| <span data-ttu-id="afa3a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="afa3a-119">Requirement</span></span> | <span data-ttu-id="afa3a-120">Value</span><span class="sxs-lookup"><span data-stu-id="afa3a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afa3a-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="afa3a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="afa3a-122">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="afa3a-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="afa3a-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="afa3a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="afa3a-124">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="afa3a-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="afa3a-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="afa3a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="afa3a-126"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="afa3a-126"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="afa3a-127">IDL</span><span class="sxs-lookup"><span data-stu-id="afa3a-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="afa3a-128"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="afa3a-128"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afa3a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="afa3a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afa3a-130">**GetEndpointToken**</span><span class="sxs-lookup"><span data-stu-id="afa3a-130">**GetEndpointToken**</span></span>](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 





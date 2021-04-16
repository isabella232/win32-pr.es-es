---
title: Propiedad GatewayUserSelectedCredsSource de IMsRdpClientTransportSettings
description: Establece o recupera el origen de credenciales de puerta de enlace de escritorio remoto (puerta de enlace de RD) Escritorio remoto especificados por el usuario.
ms.assetid: 0c12ddf6-52c2-40a2-af2b-effd4e8bbdb6
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayUserSelectedCredsSource
- Propiedad GatewayUserSelectedCredsSource Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings, propiedad GatewayUserSelectedCredsSource
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.get_GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.put_GatewayUserSelectedCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1556088e62221df7ff91b4b0069bb1ec938ebf23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533874"
---
# <a name="imsrdpclienttransportsettingsgatewayuserselectedcredssource-property"></a><span data-ttu-id="5780c-106">IMsRdpClientTransportSettings:: GatewayUserSelectedCredsSource (propiedad)</span><span class="sxs-lookup"><span data-stu-id="5780c-106">IMsRdpClientTransportSettings::GatewayUserSelectedCredsSource property</span></span>

<span data-ttu-id="5780c-107">Establece o recupera el origen de credenciales de puerta de enlace de escritorio remoto (puerta de enlace de RD) Escritorio remoto especificados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="5780c-107">Sets or retrieves the user-specified Remote Desktop Gateway (RD Gateway) credential source.</span></span>

<span data-ttu-id="5780c-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5780c-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5780c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5780c-109">Syntax</span></span>


```C++
HRESULT put_GatewayUserSelectedCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayUserSelectedCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a><span data-ttu-id="5780c-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5780c-110">Property value</span></span>

<span data-ttu-id="5780c-111">Variable **ULong** que especifica el método de autenticación de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="5780c-111">A **ULONG** variable that specifies the RD Gateway authentication method.</span></span> <span data-ttu-id="5780c-112">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5780c-112">This parameter can be one of the following values.</span></span>

<dt>

<span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>

<span data-ttu-id="5780c-113"><span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>**TSC \_ \_Modo de credenciales de proxy \_ \_ USERPASS** (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="5780c-113"><span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>**TSC\_PROXY\_CREDS\_MODE\_USERPASS** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="5780c-114">Use una contraseña (NTLM) como método de autenticación para la puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="5780c-114">Use a password (NTLM) as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>

<span data-ttu-id="5780c-115"><span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>**TSC \_ \_ \_ \_ Tarjeta inteligente del modo de credenciales de proxy** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="5780c-115"><span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>**TSC\_PROXY\_CREDS\_MODE\_SMARTCARD** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="5780c-116">Usar una tarjeta inteligente como método de autenticación para la puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="5780c-116">Use a smart card as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>

<span data-ttu-id="5780c-117"><span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>**TSC \_ \_Modo de credenciales de proxy \_ \_ any** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="5780c-117"><span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>**TSC\_PROXY\_CREDS\_MODE\_ANY** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="5780c-118">Use cualquier método de autenticación para la puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="5780c-118">Use any authentication method for RD Gateway.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="5780c-119">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="5780c-119">Error codes</span></span>

<span data-ttu-id="5780c-120">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="5780c-120">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="5780c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5780c-121">Requirements</span></span>



| <span data-ttu-id="5780c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5780c-122">Requirement</span></span> | <span data-ttu-id="5780c-123">Value</span><span class="sxs-lookup"><span data-stu-id="5780c-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5780c-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5780c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5780c-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5780c-125">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="5780c-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5780c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5780c-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5780c-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="5780c-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5780c-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="5780c-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5780c-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="5780c-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5780c-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5780c-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5780c-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="5780c-132">IID</span><span class="sxs-lookup"><span data-stu-id="5780c-132">IID</span></span><br/>                      | <span data-ttu-id="5780c-133">IID \_ IMsRdpClientTransportSettings se define como 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="5780c-133">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5780c-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="5780c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5780c-135">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="5780c-135">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 






---
description: Solicite un token para el extremo del servicio con las credenciales especificadas.
ms.assetid: 2CA0F826-9A05-4385-AF1A-A8C05B3DAFE2
title: 'IUpdateEndpointAuthProvider:: GetEndpointToken (método) (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetEndpointToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 55efe38ce9782b691e1ad32f7a21f6124e1f0bf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810208"
---
# <a name="iupdateendpointauthprovidergetendpointtoken-method"></a><span data-ttu-id="88d37-103">IUpdateEndpointAuthProvider:: GetEndpointToken (método)</span><span class="sxs-lookup"><span data-stu-id="88d37-103">IUpdateEndpointAuthProvider::GetEndpointToken method</span></span>

<span data-ttu-id="88d37-104">Solicite un token para el extremo del servicio con las credenciales especificadas.</span><span class="sxs-lookup"><span data-stu-id="88d37-104">Request a token for the endpoint of the service using the specified credentials.</span></span>

## <a name="syntax"></a><span data-ttu-id="88d37-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88d37-105">Syntax</span></span>


```C++
HRESULT GetEndpointToken(
  [in]  GUID                        serviceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  UpdateEndpointAuthTokenType tokenType,
  [in]  BOOL                        fRefreshOnline,
  [out] IUnknown                    **ppEndpointToken
);
```



## <a name="parameters"></a><span data-ttu-id="88d37-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88d37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88d37-107">*serviceId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="88d37-107">*serviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88d37-108">Identifica el servicio que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="88d37-108">Identifies the service to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="88d37-109">*endpointType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="88d37-109">*endpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88d37-110">Identifica el tipo de extremo que implementa el servicio.</span><span class="sxs-lookup"><span data-stu-id="88d37-110">Identifies the type of endpoint that is implemented by the service.</span></span>

</dd> <dt>

<span data-ttu-id="88d37-111">*proxySettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="88d37-111">*proxySettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88d37-112">La configuración que se utilizará al conectarse a un servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="88d37-112">The settings to be used when connecting to a proxy server.</span></span> <span data-ttu-id="88d37-113">Para obtener más información, vea la estructura [**UpdateEndpointProxySettings**](updateendpointproxysettings.md) .</span><span class="sxs-lookup"><span data-stu-id="88d37-113">See the [**UpdateEndpointProxySettings**](updateendpointproxysettings.md) structure for more details.</span></span>

</dd> <dt>

<span data-ttu-id="88d37-114">*hUserToken* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="88d37-114">*hUserToken* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="88d37-115">*tokenType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="88d37-115">*tokenType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88d37-116">Identifica el tipo de token de autenticación que se utiliza para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="88d37-116">Identifies the type of authentication token that is used for authentication.</span></span>

</dd> <dt>

<span data-ttu-id="88d37-117">*fRefreshOnline* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="88d37-117">*fRefreshOnline* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88d37-118">Indica que el WUA meteorológico solicita un nuevo token.</span><span class="sxs-lookup"><span data-stu-id="88d37-118">Indicates weather WUA requests a new token.</span></span> <span data-ttu-id="88d37-119">True indica que se solicita un token nuevo.</span><span class="sxs-lookup"><span data-stu-id="88d37-119">True indicates that a new token is requested.</span></span> <span data-ttu-id="88d37-120">False indica que se solicita un token nuevo o almacenado en caché.</span><span class="sxs-lookup"><span data-stu-id="88d37-120">False indicates that a new or cached token is requested.</span></span> <span data-ttu-id="88d37-121">Vea Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="88d37-121">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="88d37-122">*ppEndpointToken* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="88d37-122">*ppEndpointToken* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88d37-123">Especifique el token del punto de conexión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="88d37-123">Specifiy the endpoint token to be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88d37-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88d37-124">Return value</span></span>

<span data-ttu-id="88d37-125">Devuelve S \_ correcto si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="88d37-125">Returns S\_OK if successful.</span></span> <span data-ttu-id="88d37-126">De lo contrario, devuelve un código de error COM o Windows.</span><span class="sxs-lookup"><span data-stu-id="88d37-126">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="88d37-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88d37-127">Remarks</span></span>

<span data-ttu-id="88d37-128">WUA normalmente establece el parámetro fRefreshOnline en false cuando se llama por primera vez a este método y, después, si se produce un error de conexión, WUA establece ese parámetro en true cuando se llama de nuevo al método.</span><span class="sxs-lookup"><span data-stu-id="88d37-128">WUA typically sets the fRefreshOnline parameter to false when this method is first called, then if a connection error occures WUA sets that parameter to true when the method is called again.</span></span> <span data-ttu-id="88d37-129">Sin embargo, la implementación de este método puede solicitar un nuevo token de un servicio de token de seguridad (STS) o proporcionar un token almacenado en caché en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="88d37-129">However, the implementation of this method can request a new token from a Security Token Service (STS) or provide a cached token at any time.</span></span>

## <a name="requirements"></a><span data-ttu-id="88d37-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88d37-130">Requirements</span></span>



| <span data-ttu-id="88d37-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="88d37-131">Requirement</span></span> | <span data-ttu-id="88d37-132">Value</span><span class="sxs-lookup"><span data-stu-id="88d37-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88d37-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88d37-133">Minimum supported client</span></span><br/> | <span data-ttu-id="88d37-134">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="88d37-134">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="88d37-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88d37-135">Minimum supported server</span></span><br/> | <span data-ttu-id="88d37-136">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="88d37-136">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="88d37-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88d37-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="88d37-138"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="88d37-138"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="88d37-139">IDL</span><span class="sxs-lookup"><span data-stu-id="88d37-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="88d37-140"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="88d37-140"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="88d37-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="88d37-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="88d37-142"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88d37-142"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="88d37-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="88d37-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88d37-144"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88d37-144"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88d37-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="88d37-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88d37-146">**IUpdateEndpointAuthProvider**</span><span class="sxs-lookup"><span data-stu-id="88d37-146">**IUpdateEndpointAuthProvider**</span></span>](iupdateendpointauthprovider.md)
</dt> </dl>

 

 





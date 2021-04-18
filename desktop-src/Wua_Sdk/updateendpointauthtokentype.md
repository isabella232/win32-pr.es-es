---
description: Define el tipo de tokens que se pueden utilizar para la autenticación con un punto de conexión.
ms.assetid: 2048BD09-056F-47C1-AD2F-998DE6C52EA6
title: Enumeración UpdateEndpointAuthTokenType (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointAuthTokenType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: c978841511b7cfff895a15936a41d169a8500927
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714991"
---
# <a name="updateendpointauthtokentype-enumeration"></a><span data-ttu-id="30cc0-103">Enumeración UpdateEndpointAuthTokenType</span><span class="sxs-lookup"><span data-stu-id="30cc0-103">UpdateEndpointAuthTokenType enumeration</span></span>

<span data-ttu-id="30cc0-104">Define el tipo de tokens que se pueden utilizar para la autenticación con un punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="30cc0-104">Defines the type of tokens that can be used for authenticating with an endpoint.</span></span>

## <a name="syntax"></a><span data-ttu-id="30cc0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30cc0-105">Syntax</span></span>


```C++
typedef enum tagUpdateEndpointAuthTokenType { 
  ueattInvalidTokenType  = 0x0,
  ueattSAML11Token       = 0X1
} UpdateEndpointAuthTokenType;
```



## <a name="constants"></a><span data-ttu-id="30cc0-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="30cc0-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="30cc0-107"><span id="ueattInvalidTokenType"></span><span id="ueattinvalidtokentype"></span><span id="UEATTINVALIDTOKENTYPE"></span>**ueattInvalidTokenType**</span><span class="sxs-lookup"><span data-stu-id="30cc0-107"><span id="ueattInvalidTokenType"></span><span id="ueattinvalidtokentype"></span><span id="UEATTINVALIDTOKENTYPE"></span>**ueattInvalidTokenType**</span></span>
</dt> <dd>

<span data-ttu-id="30cc0-108">No se necesita ningún token de autenticación.</span><span class="sxs-lookup"><span data-stu-id="30cc0-108">No authentication token is needed.</span></span>

</dd> <dt>

<span data-ttu-id="30cc0-109"><span id="ueattSAML11Token"></span><span id="ueattsaml11token"></span><span id="UEATTSAML11TOKEN"></span>**ueattSAML11Token**</span><span class="sxs-lookup"><span data-stu-id="30cc0-109"><span id="ueattSAML11Token"></span><span id="ueattsaml11token"></span><span id="UEATTSAML11TOKEN"></span>**ueattSAML11Token**</span></span>
</dt> <dd>

<span data-ttu-id="30cc0-110">El token de autenticación para el punto de conexión es un token WS-Security SAML (Lenguaje de marcado de aserción de seguridad) 1,1.</span><span class="sxs-lookup"><span data-stu-id="30cc0-110">The authentication token for the endpoint is a WS-Security SAML (Security Assertion Markup Language) 1.1 token.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30cc0-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30cc0-111">Requirements</span></span>



| <span data-ttu-id="30cc0-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="30cc0-112">Requirement</span></span> | <span data-ttu-id="30cc0-113">Value</span><span class="sxs-lookup"><span data-stu-id="30cc0-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30cc0-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30cc0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="30cc0-115">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="30cc0-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="30cc0-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30cc0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="30cc0-117">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="30cc0-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="30cc0-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30cc0-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="30cc0-119"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="30cc0-119"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="30cc0-120">IDL</span><span class="sxs-lookup"><span data-stu-id="30cc0-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="30cc0-121"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="30cc0-121"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |



 

 





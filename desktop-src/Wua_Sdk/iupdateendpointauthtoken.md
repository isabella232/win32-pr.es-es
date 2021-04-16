---
description: Proporciona los métodos que WUA puede usar para recopilar información sobre el token del extremo.
ms.assetid: 52D22909-B926-426F-98C7-643C4469D021
title: Interfaz IUpdateEndpointAuthToken (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: a5902b3c91b3ab12b311121bd7dcd8c415a68d6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497608"
---
# <a name="iupdateendpointauthtoken-interface"></a><span data-ttu-id="88104-103">Interfaz IUpdateEndpointAuthToken</span><span class="sxs-lookup"><span data-stu-id="88104-103">IUpdateEndpointAuthToken interface</span></span>

<span data-ttu-id="88104-104">Proporciona los métodos que WUA puede usar para recopilar información sobre el token del extremo.</span><span class="sxs-lookup"><span data-stu-id="88104-104">Provides the methods that WUA can use to gather information about the endpoint token.</span></span>

## <a name="members"></a><span data-ttu-id="88104-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="88104-105">Members</span></span>

<span data-ttu-id="88104-106">La interfaz **IUpdateEndpointAuthToken** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="88104-106">The **IUpdateEndpointAuthToken** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="88104-107">**IUpdateEndpointAuthToken** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="88104-107">**IUpdateEndpointAuthToken** also has these types of members:</span></span>

-   [<span data-ttu-id="88104-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="88104-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="88104-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="88104-109">Methods</span></span>

<span data-ttu-id="88104-110">La interfaz **IUpdateEndpointAuthToken** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="88104-110">The **IUpdateEndpointAuthToken** interface has these methods.</span></span>



| <span data-ttu-id="88104-111">Método</span><span class="sxs-lookup"><span data-stu-id="88104-111">Method</span></span>                                                                                | <span data-ttu-id="88104-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="88104-112">Description</span></span>                                                                                                                 |
|:--------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88104-113">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="88104-113">**ServiceID**</span></span>](iupdateendpointauthtoken-serviceid.md)                               | <span data-ttu-id="88104-114">Obtiene el identificador del servicio que se va a autenticar.</span><span class="sxs-lookup"><span data-stu-id="88104-114">Gets the identifier of the service to be authenticated.</span></span><br/>                                                          |
| [<span data-ttu-id="88104-115">**SigningKey**</span><span class="sxs-lookup"><span data-stu-id="88104-115">**SigningKey**</span></span>](iupdateendpointauthtoken-signingkey.md)                             | <span data-ttu-id="88104-116">Obtiene la clave utilizada para firmar los mensajes salientes entre el equipo cliente y el sercvice.</span><span class="sxs-lookup"><span data-stu-id="88104-116">Gets the key used to sign outgoing messages between the client computer and the sercvice.</span></span><br/>                        |
| [<span data-ttu-id="88104-117">**TokenData**</span><span class="sxs-lookup"><span data-stu-id="88104-117">**TokenData**</span></span>](iupdateendpointauthtoken-tokendata.md)                               | <span data-ttu-id="88104-118">Obtiene los datos XML (enviados a través de la conexión) que representa el token.</span><span class="sxs-lookup"><span data-stu-id="88104-118">Gets the XML data (sent over the wire) that represents the token.</span></span> <br/>                                               |
| [<span data-ttu-id="88104-119">**TokenReferenceAttached**</span><span class="sxs-lookup"><span data-stu-id="88104-119">**TokenReferenceAttached**</span></span>](iupdateendpointauthtoken-tokenreferenceattached.md)     | <span data-ttu-id="88104-120">Obtiene el formato XML de una referencia adjunta al token.</span><span class="sxs-lookup"><span data-stu-id="88104-120">Gets the XML format of an attached reference to the token.</span></span><br/>                                                       |
| [<span data-ttu-id="88104-121">**TokenReferenceUnattached**</span><span class="sxs-lookup"><span data-stu-id="88104-121">**TokenReferenceUnattached**</span></span>](iupdateendpointauthtoken-tokenreferenceunattached.md) | <span data-ttu-id="88104-122">Obtiene el formato XML de una referencia no adjunta al token.</span><span class="sxs-lookup"><span data-stu-id="88104-122">Gets the XML format of an unattached reference to the token.</span></span><br/>                                                     |
| [<span data-ttu-id="88104-123">**TokenType**</span><span class="sxs-lookup"><span data-stu-id="88104-123">**TokenType**</span></span>](iupdateendpointauthtoken-tokentype.md)                               | <span data-ttu-id="88104-124">Obtiene el tipo del token del punto de conexión, como un token WS-Security SAML (Lenguaje de marcado de aserción de seguridad) 1,1.</span><span class="sxs-lookup"><span data-stu-id="88104-124">Gets the type of the endpoint token, such as a WS-Security SAML (Security Assertion Markup Language) 1.1 token.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="88104-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88104-125">Requirements</span></span>



| <span data-ttu-id="88104-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="88104-126">Requirement</span></span> | <span data-ttu-id="88104-127">Value</span><span class="sxs-lookup"><span data-stu-id="88104-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88104-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88104-128">Minimum supported client</span></span><br/> | <span data-ttu-id="88104-129">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="88104-129">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="88104-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88104-130">Minimum supported server</span></span><br/> | <span data-ttu-id="88104-131">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="88104-131">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="88104-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88104-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="88104-133"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="88104-133"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="88104-134">IDL</span><span class="sxs-lookup"><span data-stu-id="88104-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="88104-135"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="88104-135"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="88104-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="88104-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="88104-137"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88104-137"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="88104-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="88104-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88104-139"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88104-139"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



 

 

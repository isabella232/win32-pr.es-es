---
description: Contiene los métodos que se usan para negociar el tipo de token que se utiliza para autenticar el extremo de un servicio.
ms.assetid: F6177B24-C166-4BEC-83D6-3AD5B5B3CF08
title: Interfaz IUpdateEndpointAuthProvider (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 071bc23bdf9d67412fef561c71e17fe81485984f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542270"
---
# <a name="iupdateendpointauthprovider-interface"></a><span data-ttu-id="60c04-103">Interfaz IUpdateEndpointAuthProvider</span><span class="sxs-lookup"><span data-stu-id="60c04-103">IUpdateEndpointAuthProvider interface</span></span>

<span data-ttu-id="60c04-104">La interfaz **IUpdateEndpointAuthProvider** contiene los métodos que se usan para negociar el tipo de token que se utiliza para autenticar el extremo de un servicio.</span><span class="sxs-lookup"><span data-stu-id="60c04-104">The **IUpdateEndpointAuthProvider** interface contains the methods used for negotiating which type of token is used for authenticating the endpoint of a service.</span></span>

## <a name="members"></a><span data-ttu-id="60c04-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="60c04-105">Members</span></span>

<span data-ttu-id="60c04-106">La interfaz **IUpdateEndpointAuthProvider** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="60c04-106">The **IUpdateEndpointAuthProvider** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="60c04-107">**IUpdateEndpointAuthProvider** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="60c04-107">**IUpdateEndpointAuthProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="60c04-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="60c04-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="60c04-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="60c04-109">Methods</span></span>

<span data-ttu-id="60c04-110">La interfaz **IUpdateEndpointAuthProvider** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="60c04-110">The **IUpdateEndpointAuthProvider** interface has these methods.</span></span>



| <span data-ttu-id="60c04-111">Método</span><span class="sxs-lookup"><span data-stu-id="60c04-111">Method</span></span>                                                                                             | <span data-ttu-id="60c04-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="60c04-112">Description</span></span>                                                                                    |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="60c04-113">**GetEndpointToken**</span><span class="sxs-lookup"><span data-stu-id="60c04-113">**GetEndpointToken**</span></span>](iupdateendpointauthprovider-getendpointtoken.md)                           | <span data-ttu-id="60c04-114">Solicite un token para el extremo del servicio con las credenciales especificadas.</span><span class="sxs-lookup"><span data-stu-id="60c04-114">Request a token for the endpoint of the service using the specified credentials.</span></span><br/>    |
| [<span data-ttu-id="60c04-115">**GetPreferredEndpointTokenType**</span><span class="sxs-lookup"><span data-stu-id="60c04-115">**GetPreferredEndpointTokenType**</span></span>](iupdateendpointauthprovider-getpreferredendpointtokentype.md) | <span data-ttu-id="60c04-116">Devuelve el tipo de token de autenticación preferido para el extremo del servicio.</span><span class="sxs-lookup"><span data-stu-id="60c04-116">Returns the preferred type of authentication token for the endpoint of the service.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="60c04-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60c04-117">Remarks</span></span>

<span data-ttu-id="60c04-118">WUA llama al método [**GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) de esta interfaz para iniciar el proceso de negociación.</span><span class="sxs-lookup"><span data-stu-id="60c04-118">WUA calls the [**GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) method of this interface to start the negotiation process.</span></span> <span data-ttu-id="60c04-119">Cuando se realiza la llamada, se pasa WUA en el identificador de servicio, el tipo de extremo implementado por el servicio y los tipos de token que están disponibles.</span><span class="sxs-lookup"><span data-stu-id="60c04-119">When the call is made WUA passes in the service identifier, the type of endpoint implemented by the service, and the token types that are available.</span></span> <span data-ttu-id="60c04-120">A continuación, la implementación de esta interfaz devuelve los tipos de token que prefiere usar.</span><span class="sxs-lookup"><span data-stu-id="60c04-120">The implementation of this interface then returns the token types that it preferes to use.</span></span>

## <a name="requirements"></a><span data-ttu-id="60c04-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60c04-121">Requirements</span></span>



| <span data-ttu-id="60c04-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="60c04-122">Requirement</span></span> | <span data-ttu-id="60c04-123">Value</span><span class="sxs-lookup"><span data-stu-id="60c04-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60c04-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60c04-124">Minimum supported client</span></span><br/> | <span data-ttu-id="60c04-125">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="60c04-125">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="60c04-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60c04-126">Minimum supported server</span></span><br/> | <span data-ttu-id="60c04-127">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="60c04-127">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="60c04-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60c04-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="60c04-129"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="60c04-129"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="60c04-130">IDL</span><span class="sxs-lookup"><span data-stu-id="60c04-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="60c04-131"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="60c04-131"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="60c04-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="60c04-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="60c04-133"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60c04-133"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="60c04-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="60c04-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60c04-135"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60c04-135"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



 

 

---
title: Constantes de nivel de autenticación (Rpcdce. h)
description: Estos valores especifican un nivel de autenticación, que indica la cantidad de autenticación proporcionada para ayudar a proteger la integridad de los datos. Cada nivel incluye la protección proporcionada por los niveles anteriores.
ms.assetid: 06c409e4-3772-45cf-8c31-c64f99aca244
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_LEVEL_DEFAULT
- RPC_C_AUTHN_LEVEL_NONE
- RPC_C_AUTHN_LEVEL_CONNECT
- RPC_C_AUTHN_LEVEL_CALL
- RPC_C_AUTHN_LEVEL_PKT
- RPC_C_AUTHN_LEVEL_PKT_INTEGRITY
- RPC_C_AUTHN_LEVEL_PKT_PRIVACY
api_location:
- rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdf922118a1b332bfe1fe8e744114a6d1d6bf4cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535446"
---
# <a name="authentication-level-constants"></a><span data-ttu-id="a9799-104">Constantes de nivel de autenticación</span><span class="sxs-lookup"><span data-stu-id="a9799-104">Authentication Level Constants</span></span>

<span data-ttu-id="a9799-105">Estos valores especifican un nivel de autenticación, que indica la cantidad de autenticación proporcionada para ayudar a proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="a9799-105">These values specify an authentication level, which indicates the amount of authentication provided to help protect the integrity of the data.</span></span> <span data-ttu-id="a9799-106">Cada nivel incluye la protección proporcionada por los niveles anteriores.</span><span class="sxs-lookup"><span data-stu-id="a9799-106">Each level includes the protection provided by the previous levels.</span></span>



| <span data-ttu-id="a9799-107">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="a9799-107">Constant/value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="a9799-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9799-108">Description</span></span>                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <span data-ttu-id="a9799-109"><dt>**RPC \_ \_ \_ \_ Valor predeterminado de nivel de autenticación de C**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a9799-109"><dt>**RPC\_C\_AUTHN\_LEVEL\_DEFAULT**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="a9799-110">Indica a DCOM que elija el nivel de autenticación mediante su algoritmo de negociación global de seguridad normal.</span><span class="sxs-lookup"><span data-stu-id="a9799-110">Tells DCOM to choose the authentication level using its normal security blanket negotiation algorithm.</span></span> <span data-ttu-id="a9799-111">Para obtener más información, vea negociación de la [capa de seguridad](security-blanket-negotiation.md).</span><span class="sxs-lookup"><span data-stu-id="a9799-111">For more information, see [Security Blanket Negotiation](security-blanket-negotiation.md).</span></span> <br/> |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <span data-ttu-id="a9799-112"><dt>**RPC \_ C \_ authn \_ nivel \_ ninguno**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a9799-112"><dt>**RPC\_C\_AUTHN\_LEVEL\_NONE**</dt> <dt>1</dt></span></span> </dl>                             | <span data-ttu-id="a9799-113">No realiza ninguna autenticación.</span><span class="sxs-lookup"><span data-stu-id="a9799-113">Performs no authentication.</span></span><br/>                                                                                                                                                                         |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <span data-ttu-id="a9799-114"><dt>**RPC \_ C \_ authn \_ LEVEL \_ Connect**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a9799-114"><dt>**RPC\_C\_AUTHN\_LEVEL\_CONNECT**</dt> <dt>2</dt></span></span> </dl>                    | <span data-ttu-id="a9799-115">Autentica las credenciales del cliente solo cuando el cliente establece una relación con el servidor.</span><span class="sxs-lookup"><span data-stu-id="a9799-115">Authenticates the credentials of the client only when the client establishes a relationship with the server.</span></span> <span data-ttu-id="a9799-116">Los transportes de datagramas siempre utilizan el nivel de introducción de autenticación de RPC \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a9799-116">Datagram transports always use RPC\_AUTHN\_LEVEL\_PKT instead.</span></span> <br/>                        |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <span data-ttu-id="a9799-117"><dt>**RPC \_ \_ \_ \_ Llamada de nivel**</dt> <dt>3</dt> de autenticación de C</span><span class="sxs-lookup"><span data-stu-id="a9799-117"><dt>**RPC\_C\_AUTHN\_LEVEL\_CALL**</dt> <dt>3</dt></span></span> </dl>                             | <span data-ttu-id="a9799-118">Solo se autentica al principio de cada llamada a procedimiento remoto cuando el servidor recibe la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a9799-118">Authenticates only at the beginning of each remote procedure call when the server receives the request.</span></span> <span data-ttu-id="a9799-119">Los transportes de datagramas usan \_ PKT de nivel de autenticación de RPC C \_ \_ \_ en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a9799-119">Datagram transports use RPC\_C\_AUTHN\_LEVEL\_PKT instead.</span></span><br/>                                  |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <span data-ttu-id="a9799-120"><dt>**RPC \_ \_Nivel de autenticación \_ \_ de C**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="a9799-120"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT**</dt> <dt>4</dt></span></span> </dl>                                | <span data-ttu-id="a9799-121">Autentica que todos los datos recibidos provienen del cliente esperado.</span><span class="sxs-lookup"><span data-stu-id="a9799-121">Authenticates that all data received is from the expected client.</span></span><br/>                                                                                                                                   |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <span data-ttu-id="a9799-122"><dt>**RPC \_ \_Integridad de la \_ \_ PKT \_ de nivel de autenticación de C**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="a9799-122"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY**</dt> <dt>5</dt></span></span> </dl> | <span data-ttu-id="a9799-123">Autentica y comprueba que no se ha modificado ninguno de los datos transferidos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="a9799-123">Authenticates and verifies that none of the data transferred between client and server has been modified.</span></span><br/>                                                                                           |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <span data-ttu-id="a9799-124"><dt>**RPC \_ \_ \_ \_ \_ Privacidad de nivel de autenticación de C**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a9799-124"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**</dt> <dt>6</dt></span></span> </dl>       | <span data-ttu-id="a9799-125">Autentica todos los niveles anteriores y cifra el valor del argumento de cada llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="a9799-125">Authenticates all previous levels and encrypts the argument value of each remote procedure call.</span></span><br/>                                                                                                    |



## <a name="requirements"></a><span data-ttu-id="a9799-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9799-126">Requirements</span></span>



| <span data-ttu-id="a9799-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9799-127">Requirement</span></span> | <span data-ttu-id="a9799-128">Value</span><span class="sxs-lookup"><span data-stu-id="a9799-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a9799-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9799-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a9799-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a9799-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a9799-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9799-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a9799-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a9799-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a9799-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9799-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9799-134"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9799-134"><dt>Rpcdce.h</dt></span></span> </dl> |



 

 






---
title: modificador/protocolo
description: El modificador/protocolo especifica qué protocolo de conexión es compatible con el código auxiliar generado.
ms.assetid: b565b30c-72e5-442b-9588-324b9041524b
keywords:
- /Protocolo modificador MIDL
topic_type:
- apiref
api_name:
- /protocol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9770fa94d010e21dcbd2a5574a0cffe29273a23
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358268"
---
# <a name="protocol-switch"></a><span data-ttu-id="2e52c-104">modificador/protocolo</span><span class="sxs-lookup"><span data-stu-id="2e52c-104">/protocol switch</span></span>

<span data-ttu-id="2e52c-105">El modificador **/Protocolo** especifica qué protocolo de conexión es compatible con el código auxiliar generado.</span><span class="sxs-lookup"><span data-stu-id="2e52c-105">The **/protocol** switch specifies which wire protocol is supported by the generated stub.</span></span>

``` syntax
midl /protocol (dce | ndr64 | all)
```

## <a name="switch-options"></a><span data-ttu-id="2e52c-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="2e52c-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="dce"></span><span id="DCE"></span>

<span data-ttu-id="2e52c-107"><span id="dce"></span><span id="DCE"></span>DCE \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="2e52c-107"><span id="dce"></span><span id="DCE"></span>\*\*\*\*dce\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="2e52c-108">El código auxiliar generado solo es compatible con el protocolo DCE.</span><span class="sxs-lookup"><span data-stu-id="2e52c-108">The generated stub supports DCE protocol only.</span></span>

</dd> <dt>

<span id="ndr64"></span><span id="NDR64"></span>

<span data-ttu-id="2e52c-109"><span id="ndr64"></span><span id="NDR64"></span>ndr64\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2e52c-109"><span id="ndr64"></span><span id="NDR64"></span>\*\*\*\*ndr64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="2e52c-110">El código auxiliar generado solo es compatible con el protocolo NDR64 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2e52c-110">The generated stub supports Microsoft NDR64 protocol only.</span></span>

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span data-ttu-id="2e52c-111"><span id="all"></span><span id="ALL"></span>todo \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="2e52c-111"><span id="all"></span><span id="ALL"></span>\*\*\*\*all\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="2e52c-112">El código auxiliar generado es compatible con todos los protocolos disponibles para un entorno determinado.</span><span class="sxs-lookup"><span data-stu-id="2e52c-112">The generated stub supports all available protocols for a given environment.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e52c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e52c-113">Remarks</span></span>

<span data-ttu-id="2e52c-114">RPC calcula las referencias y las calcula las referencias de los datos de acuerdo con un protocolo de conexión estricto, también denominado sintaxis de transferencia, que define la representación del cable de datos, como el orden en que se calculan las referencias a los miembros de datos, la alineación de los datos en la conexión, la información adicional incluida con los datos, entre otros.</span><span class="sxs-lookup"><span data-stu-id="2e52c-114">RPC marshals and unmarshals data according to a strict wire protocol, also called transfer syntax, that defines data wire representation such as the order in which data members are marshaled, the alignment of data on the wire, additional information included with the data, among others.</span></span> <span data-ttu-id="2e52c-115">Microsoft RPC es compatible con el protocolo NDR (representación de datos de red) de OSF DCE.</span><span class="sxs-lookup"><span data-stu-id="2e52c-115">Microsoft RPC is compatible with OSF DCE's NDR (network data representation) protocol.</span></span> <span data-ttu-id="2e52c-116">En la versión de 64 bits de Windows XP, Microsoft presenta una NDR64 de protocolo experimental que está optimizada para transferir datos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="2e52c-116">In the 64-bit release of Windows XP, Microsoft introduces an experimental protocol NDR64 that is optimized for transferring 64-bit data.</span></span> <span data-ttu-id="2e52c-117">NDR64 no es compatible con el protocolo DCE.</span><span class="sxs-lookup"><span data-stu-id="2e52c-117">NDR64 is not backward compatible with the DCE protocol.</span></span>

<span data-ttu-id="2e52c-118">El protocolo **DCE** es compatible con la sintaxis de transferencia de NDR de OSF DCE.</span><span class="sxs-lookup"><span data-stu-id="2e52c-118">The **dce** protocol is compatible with OSF DCE's NDR transfer syntax.</span></span> <span data-ttu-id="2e52c-119">Este protocolo está optimizado para transferir datos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2e52c-119">This protocol is optimized for transferring 32-bit data.</span></span>

<span data-ttu-id="2e52c-120">Actualmente, el protocolo **ndr64** solo se admite cuando se usa junto con el modificador [**/Win64**](-win64.md)</span><span class="sxs-lookup"><span data-stu-id="2e52c-120">The **ndr64** protocol is currently supported only when used in conjunction with the [**/win64**](-win64.md) switch.</span></span> <span data-ttu-id="2e52c-121">Si un cliente de ndr64 solo intenta conectarse a un servidor de solo DCE, o viceversa, se rechaza la llamada con \_ \_ Trans S no compatible con RPC \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2e52c-121">If a ndr64 only client tries to connect to a dce-only server, or vice versa, the call is rejected with RPC\_S\_UNSUPPORTED\_TRANS\_SYN.</span></span>

<span data-ttu-id="2e52c-122">La opción **All** crea un código auxiliar que puede usar cualquier protocolo disponible.</span><span class="sxs-lookup"><span data-stu-id="2e52c-122">The **all** option creates a stub that may use any available protocol.</span></span> <span data-ttu-id="2e52c-123">En el caso de los códigos auxiliares de 32 bits, el único protocolo disponible actualmente es DCE.</span><span class="sxs-lookup"><span data-stu-id="2e52c-123">For 32-bit stubs, the only protocol currently available is DCE.</span></span> <span data-ttu-id="2e52c-124">En el caso de los códigos auxiliares de 64 bits creados mediante el modificador [**/Win64**](-win64.md) , tanto DCE como NDR64 están disponibles.</span><span class="sxs-lookup"><span data-stu-id="2e52c-124">For 64-bit stubs, created using the [**/win64**](-win64.md) switch, both DCE and NDR64 are available.</span></span>

## <a name="examples"></a><span data-ttu-id="2e52c-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2e52c-125">Examples</span></span>

<span data-ttu-id="2e52c-126">**MIDL/protocolo All/Win64 FILENAME. idl**</span><span class="sxs-lookup"><span data-stu-id="2e52c-126">**midl /protocol all /win64 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="2e52c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e52c-127">See also</span></span>

<dl> <dt>

[**/<system>**](-system-.md)
</dt> </dl>

 

 





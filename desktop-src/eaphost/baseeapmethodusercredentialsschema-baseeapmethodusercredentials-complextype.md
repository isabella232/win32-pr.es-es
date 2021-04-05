---
title: Tipo complejo de BaseEapMethodUserCredentials
description: Obtenga información sobre el tipo complejo de BaseEapMethodUserCredentials. Este tipo es un elemento de marcador de posición para los datos de credenciales de método.
ms.assetid: ebbf813d-657a-4ff2-acf2-c18ce694b564
keywords:
- Tipo complejo BaseEapMethodUserCredentials EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37bc7a91a5d90cde6cba1af12bb0a4784ee21c7f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793785"
---
# <a name="baseeapmethodusercredentials-complex-type"></a><span data-ttu-id="822df-105">Tipo complejo de BaseEapMethodUserCredentials</span><span class="sxs-lookup"><span data-stu-id="822df-105">BaseEapMethodUserCredentials Complex Type</span></span>

<span data-ttu-id="822df-106">El tipo complejo de **BaseEapMethodUserCredentials** es un elemento de marcador de posición para los datos de credenciales de método.</span><span class="sxs-lookup"><span data-stu-id="822df-106">The **BaseEapMethodUserCredentials** complex type is a placeholder element for method credential data.</span></span>

``` syntax
<xs:complexType name="BaseEapMethodUserCredentials">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a><span data-ttu-id="822df-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="822df-107">Remarks</span></span>

<span data-ttu-id="822df-108">El método EAP realiza la validación del esquema en el contenido de **BaseEapMethodUserCredentials**.</span><span class="sxs-lookup"><span data-stu-id="822df-108">The EAP method performs schema validation on the contents of **BaseEapMethodUserCredentials**.</span></span>

## <a name="requirements"></a><span data-ttu-id="822df-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="822df-109">Requirements</span></span>



| <span data-ttu-id="822df-110">Role</span><span class="sxs-lookup"><span data-stu-id="822df-110">Role</span></span> | <span data-ttu-id="822df-111">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="822df-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="822df-112">Remoto</span><span class="sxs-lookup"><span data-stu-id="822df-112">Client</span></span><br/> | <span data-ttu-id="822df-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="822df-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="822df-114">Servidor</span><span class="sxs-lookup"><span data-stu-id="822df-114">Server</span></span><br/> | <span data-ttu-id="822df-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="822df-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="822df-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="822df-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="822df-117">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="822df-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="822df-118">Esquema baseeapmethodusercredentials</span><span class="sxs-lookup"><span data-stu-id="822df-118">baseeapmethodusercredentials Schema</span></span>](baseeapmethodusercredentialsschema-schema.md)
</dt> </dl>

 

 






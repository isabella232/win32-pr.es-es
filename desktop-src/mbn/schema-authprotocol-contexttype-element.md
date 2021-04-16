---
description: Especifica el protocolo de autenticación que se va a utilizar para activar un contexto del Protocolo de datos de paquetes (PDP).
ms.assetid: cd3c28d9-8663-4672-94ba-0a53861086cb
title: Elemento AuthProtocol (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthProtocol
api_type:
- Schema
ms.openlocfilehash: 8626d17a234784491c5f186f800943a6ab208bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686754"
---
# <a name="authprotocol-contexttype-element"></a><span data-ttu-id="78cad-103">Elemento AuthProtocol (contextType)</span><span class="sxs-lookup"><span data-stu-id="78cad-103">AuthProtocol (contextType) Element</span></span>

<span data-ttu-id="78cad-104">El elemento **AuthProtocol (contextType)** especifica el protocolo de autenticación que se va a utilizar para activar un contexto del Protocolo de datos de paquetes (PDP).</span><span class="sxs-lookup"><span data-stu-id="78cad-104">The **AuthProtocol (contextType)** element specifies the authentication protocol to be used for activating a Packet Data Protocol (PDP) context.</span></span>

<span data-ttu-id="78cad-105">El elemento puede tener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="78cad-105">The element can have one of the following values.</span></span>

| <span data-ttu-id="78cad-106">Value</span><span class="sxs-lookup"><span data-stu-id="78cad-106">Value</span></span>      | <span data-ttu-id="78cad-107">Significado</span><span class="sxs-lookup"><span data-stu-id="78cad-107">Meaning</span></span>                                                                 |
|------------|-------------------------------------------------------------------------|
| <span data-ttu-id="78cad-108">NINGUNA</span><span class="sxs-lookup"><span data-stu-id="78cad-108">"NONE"</span></span>     | <span data-ttu-id="78cad-109">No hay ningún protocolo de autenticación.</span><span class="sxs-lookup"><span data-stu-id="78cad-109">No authentication protocol.</span></span>                                             |
| <span data-ttu-id="78cad-110">Papanicolau</span><span class="sxs-lookup"><span data-stu-id="78cad-110">"PAP"</span></span>      | <span data-ttu-id="78cad-111">Autenticación de contraseña no cifrada.</span><span class="sxs-lookup"><span data-stu-id="78cad-111">Unencrypted password authentication.</span></span>                                    |
| <span data-ttu-id="78cad-112">CHAPV2</span><span class="sxs-lookup"><span data-stu-id="78cad-112">"CHAP"</span></span>     | <span data-ttu-id="78cad-113">Protocolo de autenticación por desafío mutuo (CHAP).</span><span class="sxs-lookup"><span data-stu-id="78cad-113">Challenge Handshake Authentication Protocol(CHAP).</span></span>                      |
|  <span data-ttu-id="78cad-114">MsCHAPV2</span><span class="sxs-lookup"><span data-stu-id="78cad-114">MsCHAPV2"</span></span> | <span data-ttu-id="78cad-115">Use el protocolo de autenticación por desafío mutuo (CHAP) v 2.0 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="78cad-115">Use Microsoft s Challenge Handshake Authentication Protocol(CHAP) v2.0.</span></span> |



 

<span data-ttu-id="78cad-116">Este elemento es opcional y solo se usa para los perfiles de GSM.</span><span class="sxs-lookup"><span data-stu-id="78cad-116">This element is optional and is used only for GSM profiles.</span></span> <span data-ttu-id="78cad-117">Si no se especifica el elemento y el perfil es para un dispositivo GSM, el servicio de banda ancha móvil usará **"none"**.</span><span class="sxs-lookup"><span data-stu-id="78cad-117">If the element is not specified and the profile is for a GSM device, then the Mobile Broadband service will use **"NONE"**.</span></span>

``` syntax
<xs:element name="AuthProtocol">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="NONE"
             />
            <xs:enumeration
                value="PAP"
             />
            <xs:enumeration
                value="CHAP"
             />
            <xs:enumeration
                value="MsCHAPv2"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="78cad-118">El elemento **AuthProtocol** se define mediante el tipo complejo de [**contextType**](schema-contexttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="78cad-118">The **AuthProtocol** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="78cad-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78cad-119">Requirements</span></span>



| <span data-ttu-id="78cad-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="78cad-120">Requirement</span></span> | <span data-ttu-id="78cad-121">Value</span><span class="sxs-lookup"><span data-stu-id="78cad-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="78cad-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78cad-122">Minimum supported client</span></span><br/> | <span data-ttu-id="78cad-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="78cad-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="78cad-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78cad-124">Minimum supported server</span></span><br/> | <span data-ttu-id="78cad-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="78cad-125">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="78cad-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="78cad-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="78cad-127">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="78cad-127">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="78cad-128">**contextType**</span><span class="sxs-lookup"><span data-stu-id="78cad-128">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="78cad-129">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="78cad-129">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="78cad-130">**Contexto (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="78cad-130">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 





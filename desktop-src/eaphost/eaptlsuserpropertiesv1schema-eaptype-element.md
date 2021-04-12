---
title: Elemento EapType
description: Es un tipo derivado del elemento EapType del esquema baseeapuserpropertiesv1. | Elemento EapType
ms.assetid: c9117803-dbf0-498d-8f86-f44ac2e6b2dc
keywords:
- Elemento EapType EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be2fd00cde752cae1ae8af0fa0305cbed2cdfe7c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279960"
---
# <a name="eaptype-element"></a><span data-ttu-id="e1ec7-105">Elemento EapType</span><span class="sxs-lookup"><span data-stu-id="e1ec7-105">EapType Element</span></span>

<span data-ttu-id="e1ec7-106">El elemento **EapType** es un tipo derivado del elemento [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) del esquema [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="e1ec7-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element
                        ref="Username"
                     />
                    <xs:element name="UserCert"
                        type="hexBinary"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="e1ec7-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e1ec7-107">Child elements</span></span>



| <span data-ttu-id="e1ec7-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="e1ec7-108">Element</span></span>                                                                   | <span data-ttu-id="e1ec7-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e1ec7-109">Type</span></span>      | <span data-ttu-id="e1ec7-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1ec7-110">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1ec7-111">**Nombre de usuario**</span><span class="sxs-lookup"><span data-stu-id="e1ec7-111">**Username**</span></span>](eaptlsuserpropertiesv1schema-username-element.md)         |           | <span data-ttu-id="e1ec7-112">Captura el nombre de usuario que se va a enviar en la EAP-Identity respuesta.</span><span class="sxs-lookup"><span data-stu-id="e1ec7-112">Captures the user name to be sent in the EAP-Identity response.</span></span> <span data-ttu-id="e1ec7-113">Si falta el elemento [**username**](eaptlsuserpropertiesv1schema-username-element.md) , EAP-TLS usa el nombre del certificado al que se hace referencia en el elemento [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e1ec7-113">If the [**Username**](eaptlsuserpropertiesv1schema-username-element.md) element is absent, then EAP-TLS uses the name in the certificate referred to in the [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) element.</span></span><br/> |
| [<span data-ttu-id="e1ec7-114">**UserCert**</span><span class="sxs-lookup"><span data-stu-id="e1ec7-114">**UserCert**</span></span>](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) | <span data-ttu-id="e1ec7-115">hexBinary</span><span class="sxs-lookup"><span data-stu-id="e1ec7-115">hexBinary</span></span> | <span data-ttu-id="e1ec7-116">Hace referencia al hash SHA-1 del certificado que se debe usar para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="e1ec7-116">Refers to the SHA-1 hash of the certificate that should be used for authentication.</span></span><br/>                                                                                                                                                                                                                             |



## <a name="remarks"></a><span data-ttu-id="e1ec7-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1ec7-117">Remarks</span></span>

<span data-ttu-id="e1ec7-118">El elemento **processContents** permite futuras mejoras en el esquema.</span><span class="sxs-lookup"><span data-stu-id="e1ec7-118">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="e1ec7-119">El elemento **processContents** es opcional.</span><span class="sxs-lookup"><span data-stu-id="e1ec7-119">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1ec7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1ec7-120">Requirements</span></span>



| <span data-ttu-id="e1ec7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1ec7-121">Requirement</span></span> | <span data-ttu-id="e1ec7-122">Value</span><span class="sxs-lookup"><span data-stu-id="e1ec7-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e1ec7-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1ec7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e1ec7-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e1ec7-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e1ec7-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1ec7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e1ec7-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e1ec7-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e1ec7-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1ec7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1ec7-128">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="e1ec7-128">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="e1ec7-129">Esquema eaptlsuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="e1ec7-129">eaptlsuserpropertiesv1 Schema</span></span>](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 






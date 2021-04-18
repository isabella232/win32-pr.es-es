---
title: Elemento EapType (eaptlsuserpropertiesv1schema)
description: Este elemento es un tipo derivado del elemento EapType del esquema baseeapuserpropertiesv1. Para eaptlsuserpropertiesv1schema.
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
ms.openlocfilehash: 53e5c1404c70542f3604b94aa6cae9c8fc39fd21
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187758"
---
# <a name="eaptype-element-eaptlsuserpropertiesv1schema"></a><span data-ttu-id="c3d7b-105">Elemento EapType (eaptlsuserpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="c3d7b-105">EapType element (eaptlsuserpropertiesv1schema)</span></span>

<span data-ttu-id="c3d7b-106">El elemento **EapType** es un tipo derivado del elemento [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) del esquema [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="c3d7b-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="c3d7b-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c3d7b-107">Child elements</span></span>



| <span data-ttu-id="c3d7b-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c3d7b-108">Element</span></span>                                                                   | <span data-ttu-id="c3d7b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="c3d7b-109">Type</span></span>      | <span data-ttu-id="c3d7b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3d7b-110">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3d7b-111">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c3d7b-111">**Username**</span></span>](eaptlsuserpropertiesv1schema-username-element.md)         |           | <span data-ttu-id="c3d7b-112">Captura el nombre de usuario que se va a enviar en la EAP-Identity respuesta.</span><span class="sxs-lookup"><span data-stu-id="c3d7b-112">Captures the user name to be sent in the EAP-Identity response.</span></span> <span data-ttu-id="c3d7b-113">Si falta el elemento [**username**](eaptlsuserpropertiesv1schema-username-element.md) , EAP-TLS usa el nombre del certificado al que se hace referencia en el elemento [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c3d7b-113">If the [**Username**](eaptlsuserpropertiesv1schema-username-element.md) element is absent, then EAP-TLS uses the name in the certificate referred to in the [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) element.</span></span><br/> |
| [<span data-ttu-id="c3d7b-114">**UserCert**</span><span class="sxs-lookup"><span data-stu-id="c3d7b-114">**UserCert**</span></span>](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) | <span data-ttu-id="c3d7b-115">hexBinary</span><span class="sxs-lookup"><span data-stu-id="c3d7b-115">hexBinary</span></span> | <span data-ttu-id="c3d7b-116">Hace referencia al hash SHA-1 del certificado que se debe usar para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="c3d7b-116">Refers to the SHA-1 hash of the certificate that should be used for authentication.</span></span><br/>                                                                                                                                                                                                                             |



## <a name="remarks"></a><span data-ttu-id="c3d7b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c3d7b-117">Remarks</span></span>

<span data-ttu-id="c3d7b-118">El elemento **processContents** permite futuras mejoras en el esquema.</span><span class="sxs-lookup"><span data-stu-id="c3d7b-118">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="c3d7b-119">El elemento **processContents** es opcional.</span><span class="sxs-lookup"><span data-stu-id="c3d7b-119">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3d7b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3d7b-120">Requirements</span></span>



| <span data-ttu-id="c3d7b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3d7b-121">Requirement</span></span> | <span data-ttu-id="c3d7b-122">Value</span><span class="sxs-lookup"><span data-stu-id="c3d7b-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c3d7b-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3d7b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c3d7b-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c3d7b-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c3d7b-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3d7b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c3d7b-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c3d7b-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c3d7b-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c3d7b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3d7b-128">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="c3d7b-128">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="c3d7b-129">Esquema eaptlsuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="c3d7b-129">eaptlsuserpropertiesv1 Schema</span></span>](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 






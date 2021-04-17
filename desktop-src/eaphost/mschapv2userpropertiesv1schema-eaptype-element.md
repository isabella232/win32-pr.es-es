---
title: Elemento EapType (mschapv2userpropertiesv1schema)
description: Este elemento es un tipo derivado del elemento EapType del esquema baseeapuserpropertiesv1. Para mschapv2userpropertiesv1schema.
ms.assetid: 7bd8fb5b-ceff-4d82-a979-b01229f8863a
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
ms.openlocfilehash: d5985123a4679fe9b2524f9338b9181daa11282d
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187750"
---
# <a name="eaptype-element-mschapv2userpropertiesv1schema"></a><span data-ttu-id="98705-105">Elemento EapType (mschapv2userpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="98705-105">EapType element (mschapv2userpropertiesv1schema)</span></span>

<span data-ttu-id="98705-106">El elemento **EapType** es un tipo derivado del elemento [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) del esquema [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="98705-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

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
                        minOccurs="0"
                        ref="Username"
                     />
                    <xs:element name="Password"
                        type="string"
                        minOccurs="0"
                     />
                    <xs:element name="LogonDomain"
                        type="string"
                        minOccurs="0"
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

## <a name="child-elements"></a><span data-ttu-id="98705-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="98705-107">Child elements</span></span>



| <span data-ttu-id="98705-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="98705-108">Element</span></span>                                                                           | <span data-ttu-id="98705-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="98705-109">Type</span></span>   | <span data-ttu-id="98705-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="98705-110">Description</span></span>                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98705-111">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="98705-111">**Username**</span></span>](mschapv2userpropertiesv1schema-username-element.md)               |        | <span data-ttu-id="98705-112">Identifica el usuario que se va a autenticar.</span><span class="sxs-lookup"><span data-stu-id="98705-112">Identifies the user being authenticated.</span></span> <span data-ttu-id="98705-113">Si este elemento no está presente, el nombre de usuario se obtiene de Winlogon.</span><span class="sxs-lookup"><span data-stu-id="98705-113">If this element is not present, the user name is obtained from winlogon.</span></span> <span data-ttu-id="98705-114">El elemento [**username**](mschapv2userpropertiesv1schema-username-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="98705-114">The [**Username**](mschapv2userpropertiesv1schema-username-element.md) element is optional.</span></span><br/>                                        |
| [<span data-ttu-id="98705-115">**LogonDomain**</span><span class="sxs-lookup"><span data-stu-id="98705-115">**LogonDomain**</span></span>](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) | <span data-ttu-id="98705-116">string</span><span class="sxs-lookup"><span data-stu-id="98705-116">string</span></span> | <span data-ttu-id="98705-117">Identifica el dominio del usuario o equipo que se va a autenticar.</span><span class="sxs-lookup"><span data-stu-id="98705-117">Identifies the domain of the user or machine being authenticated.</span></span> <span data-ttu-id="98705-118">Si este elemento no está presente, se utiliza el dominio de Winlogon.</span><span class="sxs-lookup"><span data-stu-id="98705-118">If this element is not present, the domain from winlogon is used.</span></span> <span data-ttu-id="98705-119">El elemento [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="98705-119">The [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) element is optional.</span></span><br/>        |
| [<span data-ttu-id="98705-120">**Contraseña**</span><span class="sxs-lookup"><span data-stu-id="98705-120">**Password**</span></span>](mschapv2userpropertiesv1schema-password-eaptype-element.md)       | <span data-ttu-id="98705-121">string</span><span class="sxs-lookup"><span data-stu-id="98705-121">string</span></span> | <span data-ttu-id="98705-122">Identifica la contraseña del usuario o equipo que se va a autenticar.</span><span class="sxs-lookup"><span data-stu-id="98705-122">Identifies the password of the user or machine being authenticated.</span></span> <span data-ttu-id="98705-123">Si este elemento no está presente, el hash de contraseña se obtiene de Winlogon.</span><span class="sxs-lookup"><span data-stu-id="98705-123">If this element is not present, the password hash is obtained from winlogon.</span></span> <span data-ttu-id="98705-124">El elemento [**password**](mschapv2userpropertiesv1schema-password-eaptype-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="98705-124">The [**Password**](mschapv2userpropertiesv1schema-password-eaptype-element.md) element is optional.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="98705-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98705-125">Remarks</span></span>

<span data-ttu-id="98705-126">El elemento **processContents** permite futuras mejoras en el esquema.</span><span class="sxs-lookup"><span data-stu-id="98705-126">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="98705-127">El elemento **processContents** es opcional.</span><span class="sxs-lookup"><span data-stu-id="98705-127">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="98705-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98705-128">Requirements</span></span>



| <span data-ttu-id="98705-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="98705-129">Requirement</span></span> | <span data-ttu-id="98705-130">Value</span><span class="sxs-lookup"><span data-stu-id="98705-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="98705-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98705-131">Minimum supported client</span></span><br/> | <span data-ttu-id="98705-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="98705-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="98705-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98705-133">Minimum supported server</span></span><br/> | <span data-ttu-id="98705-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="98705-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="98705-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="98705-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98705-136">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="98705-136">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="98705-137">Esquema mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="98705-137">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 






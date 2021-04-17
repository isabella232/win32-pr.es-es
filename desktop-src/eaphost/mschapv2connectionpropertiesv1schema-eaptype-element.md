---
title: Elemento EapType (mschapv2connectionpropertiesv1schema)
description: Es un tipo derivado del elemento EapType del esquema baseeapconnectionpropertiesv1. Este es el elemento superior que aparece dentro del elemento de configuración del esquema EapHostConfig.
ms.assetid: dbd63387-f8ed-4308-903f-7a555f3410f7
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
ms.openlocfilehash: 3e9b7db3d3e3ab1ba90427a65a5544b87939ca88
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187762"
---
# <a name="eaptype-element-mschapv2connectionpropertiesv1schema"></a><span data-ttu-id="4efad-105">Elemento EapType (mschapv2connectionpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="4efad-105">EapType Element (mschapv2connectionpropertiesv1schema)</span></span>

<span data-ttu-id="4efad-106">El elemento **EapType** es un tipo derivado del elemento [EapType](baseeapconnectionpropertiesv1schema-eaptype-element.md) del esquema [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="4efad-106">The **EapType** element is a derived type of the [EapType](baseeapconnectionpropertiesv1schema-eaptype-element.md) element from the [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md) schema.</span></span> <span data-ttu-id="4efad-107">Este es el elemento superior que aparece dentro del elemento de configuración del esquema [EapHostConfig](eaphostconfigschema-elements.md)</span><span class="sxs-lookup"><span data-stu-id="4efad-107">This is the top element that appears inside the Config element of the [EapHostConfig](eaphostconfigschema-elements.md) schema</span></span>

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
                    <xs:element name="UseWinLogonCredentials"
                        type="boolean"
                        default="true"
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

## <a name="child-elements"></a><span data-ttu-id="4efad-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4efad-108">Child elements</span></span>



| <span data-ttu-id="4efad-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="4efad-109">Element</span></span>                                                                                                       | <span data-ttu-id="4efad-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="4efad-110">Type</span></span>    | <span data-ttu-id="4efad-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4efad-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4efad-112">**UseWinLogonCredentials**</span><span class="sxs-lookup"><span data-stu-id="4efad-112">**UseWinLogonCredentials**</span></span>](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) | <span data-ttu-id="4efad-113">boolean</span><span class="sxs-lookup"><span data-stu-id="4efad-113">boolean</span></span> | <span data-ttu-id="4efad-114">Controla el uso de las credenciales de WinLogin.</span><span class="sxs-lookup"><span data-stu-id="4efad-114">Controls use of the winlogin credentials.</span></span> <span data-ttu-id="4efad-115">Si es TRUE, EAP MS-CHAPv2 obtiene las credenciales de Winlogon.</span><span class="sxs-lookup"><span data-stu-id="4efad-115">If TRUE, then EAP MS-CHAPv2 obtains credentials from winlogon.</span></span> <span data-ttu-id="4efad-116">Si es FALSE, EAP MS-CHAPv2 obtiene las credenciales del usuario.</span><span class="sxs-lookup"><span data-stu-id="4efad-116">If FALSE, then EAP MS-CHAPv2 obtains credentials from the user.</span></span> <br/> <span data-ttu-id="4efad-117">El elemento [**UseWinLogonCredentials (EapType)**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="4efad-117">The [**UseWinLogonCredentials (EapType)**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) element is optional.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4efad-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4efad-118">Remarks</span></span>

<span data-ttu-id="4efad-119">El elemento **processContents** permite futuras mejoras en el esquema.</span><span class="sxs-lookup"><span data-stu-id="4efad-119">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="4efad-120">El elemento **processContents** es opcional.</span><span class="sxs-lookup"><span data-stu-id="4efad-120">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="4efad-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4efad-121">Requirements</span></span>



| <span data-ttu-id="4efad-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4efad-122">Requirement</span></span> | <span data-ttu-id="4efad-123">Value</span><span class="sxs-lookup"><span data-stu-id="4efad-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4efad-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4efad-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4efad-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4efad-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4efad-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4efad-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4efad-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4efad-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4efad-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4efad-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4efad-129">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="4efad-129">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="4efad-130">Esquema mschapv2connectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="4efad-130">mschapv2connectionpropertiesv1 Schema</span></span>](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 






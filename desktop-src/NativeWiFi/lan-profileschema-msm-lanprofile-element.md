---
description: Contiene la configuración del módulo específico del medio (MSM).
ms.assetid: fe858701-e0eb-4817-b3c2-ae61e96a4cbe
title: Elemento MSM (LANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSM
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e9e58895ae36a304e713ecdb21b4008a2027e8c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277730"
---
# <a name="msm-lanprofile-element"></a><span data-ttu-id="14a87-103">Elemento MSM (LANProfile)</span><span class="sxs-lookup"><span data-stu-id="14a87-103">MSM (LANProfile) Element</span></span>

<span data-ttu-id="14a87-104">El elemento MSM (LANProfile) contiene la configuración del módulo específico del medio (MSM).</span><span class="sxs-lookup"><span data-stu-id="14a87-104">The MSM (LANProfile) element contains media-specific module (MSM) settings.</span></span>

``` syntax
<xs:element name="MSM">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="security">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="OneXEnforced"
                            type="boolean"
                         />
                        <xs:element name="OneXEnabled"
                            type="boolean"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="14a87-105">El elemento **MSM** se define mediante el elemento [**LANProfile**](lan-profileschema-lanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="14a87-105">The **MSM** element is defined by the [**LANProfile**](lan-profileschema-lanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="14a87-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="14a87-106">Child elements</span></span>



| <span data-ttu-id="14a87-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="14a87-107">Element</span></span>                                                                 | <span data-ttu-id="14a87-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="14a87-108">Type</span></span>    | <span data-ttu-id="14a87-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="14a87-109">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14a87-110">**OneXEnabled**</span><span class="sxs-lookup"><span data-stu-id="14a87-110">**OneXEnabled**</span></span>](lan-profileschema-onexenabled-security-element.md)   | <span data-ttu-id="14a87-111">boolean</span><span class="sxs-lookup"><span data-stu-id="14a87-111">boolean</span></span> | <span data-ttu-id="14a87-112">Especifica si el servicio de configuración automática de redes cableadas intentará la autenticación del puerto mediante 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="14a87-112">Specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span><br/>       |
| [<span data-ttu-id="14a87-113">**OneXEnforced**</span><span class="sxs-lookup"><span data-stu-id="14a87-113">**OneXEnforced**</span></span>](lan-profileschema-onexenforced-security-element.md) | <span data-ttu-id="14a87-114">boolean</span><span class="sxs-lookup"><span data-stu-id="14a87-114">boolean</span></span> | <span data-ttu-id="14a87-115">Especifica si el servicio de configuración automática para redes cableadas requiere el uso de 802.1 X para la autenticación de puertos.</span><span class="sxs-lookup"><span data-stu-id="14a87-115">Specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <br/> |
| [<span data-ttu-id="14a87-116">**bursátil**</span><span class="sxs-lookup"><span data-stu-id="14a87-116">**security**</span></span>](lan-profileschema-security-msm-element.md)              |         | <span data-ttu-id="14a87-117">Contiene la configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="14a87-117">Contains security settings.</span></span> <br/>                                                                                                  |



## <a name="requirements"></a><span data-ttu-id="14a87-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14a87-118">Requirements</span></span>



| <span data-ttu-id="14a87-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="14a87-119">Requirement</span></span> | <span data-ttu-id="14a87-120">Value</span><span class="sxs-lookup"><span data-stu-id="14a87-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="14a87-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14a87-121">Minimum supported client</span></span><br/> | <span data-ttu-id="14a87-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="14a87-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="14a87-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14a87-123">Minimum supported server</span></span><br/> | <span data-ttu-id="14a87-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="14a87-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14a87-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="14a87-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="14a87-126">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="14a87-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="14a87-127">**LANProfile**</span><span class="sxs-lookup"><span data-stu-id="14a87-127">**LANProfile**</span></span>](lan-profileschema-lanprofile-element.md)
</dt> <dt>

<span data-ttu-id="14a87-128">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="14a87-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="14a87-129">**LANProfile**</span><span class="sxs-lookup"><span data-stu-id="14a87-129">**LANProfile**</span></span>](lan-profileschema-lanprofile-element.md)
</dt> </dl>

 

 





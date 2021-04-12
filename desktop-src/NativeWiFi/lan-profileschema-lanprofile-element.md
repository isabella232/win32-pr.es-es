---
description: Contiene un perfil de red con cable.
ms.assetid: f5f9fcdc-febf-4730-8be4-5e1885d9ab08
title: Elemento LANProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANProfile
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 58ad88c9f975455bdd2d77a0ef8ee028d9027d9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277732"
---
# <a name="lanprofile-element"></a><span data-ttu-id="40e24-103">Elemento LANProfile</span><span class="sxs-lookup"><span data-stu-id="40e24-103">LANProfile Element</span></span>

<span data-ttu-id="40e24-104">El elemento LANProfile contiene un perfil de red con cable.</span><span class="sxs-lookup"><span data-stu-id="40e24-104">The LANProfile element contains a wired network profile.</span></span> <span data-ttu-id="40e24-105">Este elemento es el elemento raíz único para un perfil de red con cable.</span><span class="sxs-lookup"><span data-stu-id="40e24-105">This element is the unique root element for a wired network profile.</span></span>

<span data-ttu-id="40e24-106">El espacio de nombres de destino para el elemento LANProfile es `https://www.microsoft.com/networking/LAN/profile/v1` .</span><span class="sxs-lookup"><span data-stu-id="40e24-106">The target namespace for the LANProfile element is `https://www.microsoft.com/networking/LAN/profile/v1`.</span></span>

``` syntax
<xs:element name="LANProfile">
    <xs:complexType>
        <xs:sequence>
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

## <a name="child-elements"></a><span data-ttu-id="40e24-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="40e24-107">Child elements</span></span>



| <span data-ttu-id="40e24-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="40e24-108">Element</span></span>                                                                 | <span data-ttu-id="40e24-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="40e24-109">Type</span></span>    | <span data-ttu-id="40e24-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="40e24-110">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40e24-111">**MSM**</span><span class="sxs-lookup"><span data-stu-id="40e24-111">**MSM**</span></span>](lan-profileschema-msm-lanprofile-element.md)                 |         | <span data-ttu-id="40e24-112">Contiene la configuración del módulo específico del medio (MSM).</span><span class="sxs-lookup"><span data-stu-id="40e24-112">Contains media-specific module (MSM) settings.</span></span> <br/>                                                                               |
| [<span data-ttu-id="40e24-113">**OneXEnabled**</span><span class="sxs-lookup"><span data-stu-id="40e24-113">**OneXEnabled**</span></span>](lan-profileschema-onexenabled-security-element.md)   | <span data-ttu-id="40e24-114">boolean</span><span class="sxs-lookup"><span data-stu-id="40e24-114">boolean</span></span> | <span data-ttu-id="40e24-115">Especifica si el servicio de configuración automática de redes cableadas intentará la autenticación del puerto mediante 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="40e24-115">Specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span> <br/>      |
| [<span data-ttu-id="40e24-116">**OneXEnforced**</span><span class="sxs-lookup"><span data-stu-id="40e24-116">**OneXEnforced**</span></span>](lan-profileschema-onexenforced-security-element.md) | <span data-ttu-id="40e24-117">boolean</span><span class="sxs-lookup"><span data-stu-id="40e24-117">boolean</span></span> | <span data-ttu-id="40e24-118">Especifica si el servicio de configuración automática para redes cableadas requiere el uso de 802.1 X para la autenticación de puertos.</span><span class="sxs-lookup"><span data-stu-id="40e24-118">Specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <br/> |
| [<span data-ttu-id="40e24-119">**bursátil**</span><span class="sxs-lookup"><span data-stu-id="40e24-119">**security**</span></span>](lan-profileschema-security-msm-element.md)              |         | <span data-ttu-id="40e24-120">Contiene la configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="40e24-120">Contains security settings.</span></span> <br/>                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="40e24-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40e24-121">Remarks</span></span>

<span data-ttu-id="40e24-122">Para ver la lista de elementos secundarios en una estructura similar a un árbol, [vea \_ elementos de esquema de Perfil de LAN](lan-profileschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="40e24-122">To view the list of child elements in a tree-like structure, see [LAN\_profile Schema Elements](lan-profileschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="40e24-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40e24-123">Requirements</span></span>



| <span data-ttu-id="40e24-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="40e24-124">Requirement</span></span> | <span data-ttu-id="40e24-125">Value</span><span class="sxs-lookup"><span data-stu-id="40e24-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="40e24-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40e24-126">Minimum supported client</span></span><br/> | <span data-ttu-id="40e24-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="40e24-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="40e24-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40e24-128">Minimum supported server</span></span><br/> | <span data-ttu-id="40e24-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="40e24-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





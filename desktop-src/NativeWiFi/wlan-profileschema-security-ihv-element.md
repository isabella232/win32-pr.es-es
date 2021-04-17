---
description: Contiene diversas opciones de seguridad que utilizan los proveedores de hardware independientes.
ms.assetid: 237c5d98-3f3c-4279-b2ad-b0d05df041f9
title: Elemento Security (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ace1bb0ca31f40fdc9d10fba13832797d8d4306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677992"
---
# <a name="security-ihv-element"></a><span data-ttu-id="41c27-103">Elemento Security (IHV)</span><span class="sxs-lookup"><span data-stu-id="41c27-103">security (IHV) Element</span></span>

<span data-ttu-id="41c27-104">El elemento de seguridad (IHV) contiene varias configuraciones de seguridad utilizadas por proveedores de hardware independientes.</span><span class="sxs-lookup"><span data-stu-id="41c27-104">The security (IHV) element contains various security settings used by independent hardware vendors.</span></span>

<span data-ttu-id="41c27-105">La configuración de seguridad de Microsoft y la configuración de seguridad de IHV son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="41c27-105">Microsoft security settings and IHV security settings are mutually exclusive.</span></span> <span data-ttu-id="41c27-106">Si ambos conjuntos de configuración de seguridad están presentes en el mismo perfil, el perfil no es válido.</span><span class="sxs-lookup"><span data-stu-id="41c27-106">If both sets of security settings are present in the same profile, the profile is invalid.</span></span>

<span data-ttu-id="41c27-107">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="41c27-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="security">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="41c27-108">El elemento de **seguridad** se define mediante el elemento [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="41c27-108">The **security** element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="41c27-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41c27-109">Requirements</span></span>



| <span data-ttu-id="41c27-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="41c27-110">Requirement</span></span> | <span data-ttu-id="41c27-111">Value</span><span class="sxs-lookup"><span data-stu-id="41c27-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="41c27-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41c27-112">Minimum supported client</span></span><br/> | <span data-ttu-id="41c27-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="41c27-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="41c27-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41c27-114">Minimum supported server</span></span><br/> | <span data-ttu-id="41c27-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="41c27-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="41c27-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="41c27-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="41c27-117">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="41c27-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="41c27-118">**IHV**</span><span class="sxs-lookup"><span data-stu-id="41c27-118">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="41c27-119">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="41c27-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="41c27-120">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="41c27-120">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 





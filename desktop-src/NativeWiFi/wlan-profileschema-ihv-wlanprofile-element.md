---
description: Contiene diversos valores para los proveedores de hardware independientes.
ms.assetid: 4ad8c991-7849-41d6-9852-1ecadc372a2d
title: Elemento IHV (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IHV
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d2d2902522c84ebe2939d42301a491521ac8a70f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687128"
---
# <a name="ihv-wlanprofile-element"></a><span data-ttu-id="232d1-103">Elemento IHV (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="232d1-103">IHV (WLANProfile) Element</span></span>

<span data-ttu-id="232d1-104">El elemento IHV (WLANProfile) contiene varias opciones de configuración para los proveedores de hardware independientes.</span><span class="sxs-lookup"><span data-stu-id="232d1-104">The IHV (WLANProfile) element contains various settings for independent hardware vendors.</span></span> <span data-ttu-id="232d1-105">Si un perfil incluye la configuración de seguridad de IHV, invalidará cualquier seguridad definida por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="232d1-105">If a profile includes IHV security settings, they override any Microsoft-defined security.</span></span>

<span data-ttu-id="232d1-106">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="232d1-106">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="IHV"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUIHeader">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="OUI">
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:length
                                        value="3"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="type">
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:length
                                        value="1"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
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
            <xs:element name="connectivity"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="security"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="useMSOneX"
                type="boolean"
                minOccurs="0"
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
```

<span data-ttu-id="232d1-107">El elemento se define mediante el elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="232d1-107">The element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="232d1-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="232d1-108">Child elements</span></span>



| <span data-ttu-id="232d1-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="232d1-109">Element</span></span>                                                             | <span data-ttu-id="232d1-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="232d1-110">Type</span></span>                                                              | <span data-ttu-id="232d1-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="232d1-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="232d1-112">**Conectividad**</span><span class="sxs-lookup"><span data-stu-id="232d1-112">**connectivity**</span></span>](wlan-profileschema-connectivity-ihv-element.md) |                                                                   | <span data-ttu-id="232d1-113">Contiene la configuración de conectividad relacionada con IHV.</span><span class="sxs-lookup"><span data-stu-id="232d1-113">Contains IHV-related connectivity settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="232d1-114">**OUI**</span><span class="sxs-lookup"><span data-stu-id="232d1-114">**OUI**</span></span>](wlan-profileschema-oui-ouiheader-element.md)             |                                                                   | <span data-ttu-id="232d1-115">Contiene un hexBinary de 3 bytes que identifica el IHV.</span><span class="sxs-lookup"><span data-stu-id="232d1-115">Contains a 3 byte hexBinary that identifies the IHV.</span></span><br/>                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="232d1-116">**OUIHeader**</span><span class="sxs-lookup"><span data-stu-id="232d1-116">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)       |                                                                   | <span data-ttu-id="232d1-117">Identifica el IHV.</span><span class="sxs-lookup"><span data-stu-id="232d1-117">Identifies the IHV.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="232d1-118">**bursátil**</span><span class="sxs-lookup"><span data-stu-id="232d1-118">**security**</span></span>](wlan-profileschema-security-ihv-element.md)         |                                                                   | <span data-ttu-id="232d1-119">Contiene la configuración de seguridad específica de IHV.</span><span class="sxs-lookup"><span data-stu-id="232d1-119">Contains IHV-specific security settings.</span></span> <span data-ttu-id="232d1-120">La configuración de seguridad de Microsoft y la configuración de seguridad de IHV son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="232d1-120">Microsoft security settings and IHV security settings are mutually exclusive.</span></span> <span data-ttu-id="232d1-121">El perfil completo no es válido si ambas opciones de seguridad están presentes.</span><span class="sxs-lookup"><span data-stu-id="232d1-121">The entire profile is invalid if both security settings are present.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="232d1-122">**automáticamente**</span><span class="sxs-lookup"><span data-stu-id="232d1-122">**type**</span></span>](wlan-profileschema-type-ouiheader-element.md)           |                                                                   | <span data-ttu-id="232d1-123">Contiene un hexBinary de 1 byte que se usa para diferenciar las NIC del mismo IHV.</span><span class="sxs-lookup"><span data-stu-id="232d1-123">Contains a 1 byte hexBinary that is used to differentiate NICs by the same IHV.</span></span><br/>                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="232d1-124">**useMSOneX**</span><span class="sxs-lookup"><span data-stu-id="232d1-124">**useMSOneX**</span></span>](wlan-profileschema-usemsonex-ihv-element.md)       | [<span data-ttu-id="232d1-125">boolean</span><span class="sxs-lookup"><span data-stu-id="232d1-125">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="232d1-126">Especifica el origen de la configuración de seguridad de 802.1 X usada por un componente de seguridad IHV.</span><span class="sxs-lookup"><span data-stu-id="232d1-126">Specifies the origin of 802.1X security settings used by an IHV security component.</span></span> <span data-ttu-id="232d1-127">Cuando [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) es true, los componentes de seguridad de IHV usan la configuración de 802.1 x definida por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="232d1-127">When [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) is true, IHV security components use Microsoft-defined 802.1X settings.</span></span> <span data-ttu-id="232d1-128">Cuando **useMSOneX** es false, los componentes de seguridad de IHV usan la configuración de 802.1 x suministrada por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="232d1-128">When **useMSOneX** is false, IHV security components use vendor-supplied 802.1X settings.</span></span> <span data-ttu-id="232d1-129">De forma predeterminada, **useMSOneX** es false.</span><span class="sxs-lookup"><span data-stu-id="232d1-129">By default, **useMSOneX** is false.</span></span> <span data-ttu-id="232d1-130">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="232d1-130">This element is optional.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="232d1-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="232d1-131">Requirements</span></span>



| <span data-ttu-id="232d1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="232d1-132">Requirement</span></span> | <span data-ttu-id="232d1-133">Value</span><span class="sxs-lookup"><span data-stu-id="232d1-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="232d1-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="232d1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="232d1-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="232d1-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="232d1-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="232d1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="232d1-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="232d1-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="232d1-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="232d1-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="232d1-139">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="232d1-139">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="232d1-140">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="232d1-140">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="232d1-141">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="232d1-141">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="232d1-142">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="232d1-142">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 

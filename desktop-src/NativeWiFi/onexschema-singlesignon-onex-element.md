---
description: Especifica la información de configuración de red de inicio de sesión único (SSO).
ms.assetid: c0a26f15-77fd-43e9-a6af-54e9b46f03fa
title: Elemento singleSignOn (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- singleSignOn
api_type:
- Schema
api_location: ''
ms.openlocfilehash: fd25767ed311e9a6f0e75f8dec090d4b80d3f0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677749"
---
# <a name="singlesignon-onex-element"></a><span data-ttu-id="79c99-103">Elemento singleSignOn (OneX)</span><span class="sxs-lookup"><span data-stu-id="79c99-103">singleSignOn (OneX) Element</span></span>

<span data-ttu-id="79c99-104">El elemento singleSignOn (OneX) especifica la información de configuración de red de inicio de sesión único (SSO).</span><span class="sxs-lookup"><span data-stu-id="79c99-104">The singleSignOn (OneX) element specifies single sign-on (SSO) network configuration information.</span></span>

<span data-ttu-id="79c99-105">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="79c99-105">This element is optional.</span></span> <span data-ttu-id="79c99-106">No use el elemento singleSignOn en un perfil si la red no lo requiere.</span><span class="sxs-lookup"><span data-stu-id="79c99-106">Do not use the singleSignOn element in a profile if the network does not require it.</span></span>

<span data-ttu-id="79c99-107">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.</span><span class="sxs-lookup"><span data-stu-id="79c99-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="singleSignOn">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="type"
                minOccurs="1"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="preLogon"
                         />
                        <xs:enumeration
                            value="postLogon"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxDelay"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="0"
                         />
                        <xs:enumeration
                            value="120"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="userBasedVirtualLan"
                type="boolean"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="79c99-108">El elemento **singleSignOn** se define mediante el elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="79c99-108">The **singleSignOn** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="79c99-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="79c99-109">Child elements</span></span>



| <span data-ttu-id="79c99-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="79c99-110">Element</span></span>                                                                            | <span data-ttu-id="79c99-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="79c99-111">Type</span></span>    | <span data-ttu-id="79c99-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="79c99-112">Description</span></span>                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79c99-113">**maxDelay**</span><span class="sxs-lookup"><span data-stu-id="79c99-113">**maxDelay**</span></span>](onexschema-maxdelay-singlesignon-element.md)                       |         | <span data-ttu-id="79c99-114">Especifica, en segundos, el retraso máximo antes de que se produzca un error en el intento de conexión de inicio de sesión único.</span><span class="sxs-lookup"><span data-stu-id="79c99-114">Specifies, in seconds, the maximum delay before the single sign-on connection attempt fails.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="79c99-115">**automáticamente**</span><span class="sxs-lookup"><span data-stu-id="79c99-115">**type**</span></span>](onexschema-type-singlesignon-element.md)                               |         | <span data-ttu-id="79c99-116">Especifica cuándo se realiza el inicio de sesión único.</span><span class="sxs-lookup"><span data-stu-id="79c99-116">Specifies when single sign-on is performed.</span></span> <span data-ttu-id="79c99-117">Cuando se establece en `preLogon` , se realiza el inicio de sesión único antes de que el usuario inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="79c99-117">When set to `preLogon`, single sign-on is performed before the user logs on.</span></span> <span data-ttu-id="79c99-118">Cuando se establece en `postLogon` , el inicio de sesión único se realiza inmediatamente después de que el usuario inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="79c99-118">When set to `postLogon`, single sign-on is performed immediately after the user logs on.</span></span><br/> |
| [<span data-ttu-id="79c99-119">**userBasedVirtualLan**</span><span class="sxs-lookup"><span data-stu-id="79c99-119">**userBasedVirtualLan**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md) | <span data-ttu-id="79c99-120">boolean</span><span class="sxs-lookup"><span data-stu-id="79c99-120">boolean</span></span> | <span data-ttu-id="79c99-121">Especifica si la LAN virtual (VLAN) usada por el dispositivo cambia en función de las credenciales del usuario.</span><span class="sxs-lookup"><span data-stu-id="79c99-121">Specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span><br/>                                                                                                                   |



## <a name="remarks"></a><span data-ttu-id="79c99-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79c99-122">Remarks</span></span>

<span data-ttu-id="79c99-123">Este parámetro se puede establecer en la línea de comandos mediante el comando **netsh wlan set ProfileParameter**</span><span class="sxs-lookup"><span data-stu-id="79c99-123">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="79c99-124">Para obtener más información, consulte [comandos Netsh para red de área local inalámbrica (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="79c99-124">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="79c99-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79c99-125">Requirements</span></span>



| <span data-ttu-id="79c99-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="79c99-126">Requirement</span></span> | <span data-ttu-id="79c99-127">Value</span><span class="sxs-lookup"><span data-stu-id="79c99-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="79c99-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79c99-128">Minimum supported client</span></span><br/> | <span data-ttu-id="79c99-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="79c99-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="79c99-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79c99-130">Minimum supported server</span></span><br/> | <span data-ttu-id="79c99-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="79c99-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="79c99-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="79c99-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="79c99-133">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="79c99-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="79c99-134">**Onex-**</span><span class="sxs-lookup"><span data-stu-id="79c99-134">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="79c99-135">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="79c99-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="79c99-136">**Onex-**</span><span class="sxs-lookup"><span data-stu-id="79c99-136">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 

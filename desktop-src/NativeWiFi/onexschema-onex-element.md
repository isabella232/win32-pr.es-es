---
description: Especifica la información de configuración de 802.1 X para un perfil de LAN inalámbrica o cableada.
ms.assetid: 4528fcb5-ee8e-4824-a69e-8d67622c4b4d
title: Elemento OneX
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4b3e3d91087a394efb7909d36d6244bfbf6115e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667139"
---
# <a name="onex-element"></a><span data-ttu-id="86c1f-103">Elemento OneX</span><span class="sxs-lookup"><span data-stu-id="86c1f-103">OneX Element</span></span>

<span data-ttu-id="86c1f-104">El elemento OneX especifica la información de configuración de 802.1 X para un perfil de LAN inalámbrica o cableada.</span><span class="sxs-lookup"><span data-stu-id="86c1f-104">The OneX element specifies 802.1X configuration information for a wired or wireless LAN profile.</span></span> <span data-ttu-id="86c1f-105">Este elemento es el elemento raíz único para un perfil de 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="86c1f-105">This element is the unique root element for an 802.1X profile.</span></span>

<span data-ttu-id="86c1f-106">El espacio de nombres de destino para el elemento OneX es `https://www.microsoft.com/networking/OneX/v1` .</span><span class="sxs-lookup"><span data-stu-id="86c1f-106">The target namespace for the OneX element is `https://www.microsoft.com/networking/OneX/v1`.</span></span> <span data-ttu-id="86c1f-107">La mayoría de los elementos secundarios del elemento OneX se encuentran en el `OneX` espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="86c1f-107">Most child elements of the OneX element are in the `OneX` namespace.</span></span> <span data-ttu-id="86c1f-108">Hay una excepción: el elemento [**EAPConfig**](onexschema-eapconfig-onex-element.md) está en el `https://www.microsoft.com/provisioning/EapHostConfig` espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="86c1f-108">There is one exception: the [**EAPConfig**](onexschema-eapconfig-onex-element.md) element is in the `https://www.microsoft.com/provisioning/EapHostConfig` namespace.</span></span>

<span data-ttu-id="86c1f-109">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Solo se admite el elemento [**EAPConfig**](onexschema-eapconfig-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="86c1f-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** Only the [**EAPConfig**](onexschema-eapconfig-onex-element.md) element is supported.</span></span> <span data-ttu-id="86c1f-110">Otros elementos, si están presentes en un perfil, se omitirán.</span><span class="sxs-lookup"><span data-stu-id="86c1f-110">Other elements, if present in a profile, will be ignored.</span></span>

``` syntax
<xs:element name="OneX">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="cacheUserData"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="heldPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="startPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxStart"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="100"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxAuthFailures"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="100"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="supplicantMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="inhibitTransmission"
                         />
                        <xs:enumeration
                            value="includeLearning"
                         />
                        <xs:enumeration
                            value="compliant"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="machineOrUser"
                         />
                        <xs:enumeration
                            value="machine"
                         />
                        <xs:enumeration
                            value="user"
                         />
                        <xs:enumeration
                            value="guest"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="singleSignOn"
                minOccurs="0"
            >
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
            <xs:element name="EAPConfig">
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            minOccurs="1"
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

## <a name="child-elements"></a><span data-ttu-id="86c1f-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="86c1f-111">Child elements</span></span>



| <span data-ttu-id="86c1f-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="86c1f-112">Element</span></span>                                                                            | <span data-ttu-id="86c1f-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="86c1f-113">Type</span></span>    | <span data-ttu-id="86c1f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="86c1f-114">Description</span></span>                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="86c1f-115">**authMode**</span><span class="sxs-lookup"><span data-stu-id="86c1f-115">**authMode**</span></span>](onexschema-authmode-onex-element.md)                               |         | <span data-ttu-id="86c1f-116">Especifica el tipo de credenciales utilizado para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="86c1f-116">Specifies the type of credentials used for authentication.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="86c1f-117">**authPeriod**</span><span class="sxs-lookup"><span data-stu-id="86c1f-117">**authPeriod**</span></span>](onexschema-authperiod-onex-element.md)                           |         | <span data-ttu-id="86c1f-118">Especifica el período de tiempo máximo, en segundos, en el que un cliente espera una respuesta del autenticador.</span><span class="sxs-lookup"><span data-stu-id="86c1f-118">Specifies the maximum length of time, in seconds, in which a client waits for a response from the authenticator.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="86c1f-119">**cacheUserData**</span><span class="sxs-lookup"><span data-stu-id="86c1f-119">**cacheUserData**</span></span>](onexschema-cacheuserdata-onex-element.md)                     | <span data-ttu-id="86c1f-120">boolean</span><span class="sxs-lookup"><span data-stu-id="86c1f-120">boolean</span></span> | <span data-ttu-id="86c1f-121">Especifica si las credenciales del usuario se almacenan en caché para las conexiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="86c1f-121">Specifies whether the user credentials are cached for subsequent connections.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="86c1f-122">**EAPConfig**</span><span class="sxs-lookup"><span data-stu-id="86c1f-122">**EAPConfig**</span></span>](onexschema-eapconfig-onex-element.md)                             |         | <span data-ttu-id="86c1f-123">Especifica la configuración de EAPHost.</span><span class="sxs-lookup"><span data-stu-id="86c1f-123">Specifies the EAPHost configuration.</span></span><br/>                                                                                                                                                                              |
| [<span data-ttu-id="86c1f-124">**heldPeriod**</span><span class="sxs-lookup"><span data-stu-id="86c1f-124">**heldPeriod**</span></span>](onexschema-heldperiod-onex-element.md)                           |         | <span data-ttu-id="86c1f-125">Especifica el período de tiempo, en segundos, en el que un cliente no volverá a intentar la autenticación después de un intento de autenticación erróneo.</span><span class="sxs-lookup"><span data-stu-id="86c1f-125">Specifies the length of time, in seconds, in which a client will not re-attempt authentication after a failed authentication attempt.</span></span><br/>                                                                             |
| [<span data-ttu-id="86c1f-126">**maxAuthFailures**</span><span class="sxs-lookup"><span data-stu-id="86c1f-126">**maxAuthFailures**</span></span>](onexschema-maxauthfailures-onex-element.md)                 |         | <span data-ttu-id="86c1f-127">Especifica el número máximo de errores de autenticación permitido para un conjunto de credenciales.</span><span class="sxs-lookup"><span data-stu-id="86c1f-127">Specifies the maximum number of authentication failures allowed for a set of credentials.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="86c1f-128">**maxDelay**</span><span class="sxs-lookup"><span data-stu-id="86c1f-128">**maxDelay**</span></span>](onexschema-maxdelay-singlesignon-element.md)                       |         | <span data-ttu-id="86c1f-129">Especifica, en segundos, el retraso máximo antes de que se produzca un error en el intento de conexión de inicio de sesión único.</span><span class="sxs-lookup"><span data-stu-id="86c1f-129">Specifies, in seconds, the maximum delay before the single sign-on connection attempt fails.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="86c1f-130">**maxStart**</span><span class="sxs-lookup"><span data-stu-id="86c1f-130">**maxStart**</span></span>](onexschema-maxstart-onex-element.md)                               |         | <span data-ttu-id="86c1f-131">Especifica el número máximo de mensajes de EAPOL-Start enviados.</span><span class="sxs-lookup"><span data-stu-id="86c1f-131">Specifies the maximum number of EAPOL-Start messages sent.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="86c1f-132">**singleSignOn**</span><span class="sxs-lookup"><span data-stu-id="86c1f-132">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)                       |         | <span data-ttu-id="86c1f-133">Especifica la información de configuración de red de inicio de sesión único.</span><span class="sxs-lookup"><span data-stu-id="86c1f-133">Specifies single sign-on network configuration information.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="86c1f-134">**startPeriod**</span><span class="sxs-lookup"><span data-stu-id="86c1f-134">**startPeriod**</span></span>](onexschema-startperiod-onex-element.md)                         |         | <span data-ttu-id="86c1f-135">Especifica el período de tiempo, en segundos, que hay que esperar antes de que se envíe un EAPOL-Start.</span><span class="sxs-lookup"><span data-stu-id="86c1f-135">Specifies the length of time, in seconds, to wait before an EAPOL-Start is sent.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="86c1f-136">**supplicantMode**</span><span class="sxs-lookup"><span data-stu-id="86c1f-136">**supplicantMode**</span></span>](onexschema-supplicantmode-onex-element.md)                   |         | <span data-ttu-id="86c1f-137">Especifica el método de transmisión que se usa para los paquetes EAPOL.</span><span class="sxs-lookup"><span data-stu-id="86c1f-137">Specifies the method of transmission used for EAPOL packets.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="86c1f-138">**automáticamente**</span><span class="sxs-lookup"><span data-stu-id="86c1f-138">**type**</span></span>](onexschema-type-singlesignon-element.md)                               |         | <span data-ttu-id="86c1f-139">Especifica cuándo se realiza el inicio de sesión único.</span><span class="sxs-lookup"><span data-stu-id="86c1f-139">Specifies when single sign-on is performed.</span></span> <span data-ttu-id="86c1f-140">Cuando se establece en `preLogon` , se realiza el inicio de sesión único antes de que el usuario inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="86c1f-140">When set to `preLogon`, single sign-on is performed before the user logs on.</span></span> <span data-ttu-id="86c1f-141">Cuando se establece en `postLogon` , el inicio de sesión único se realiza inmediatamente después de que el usuario inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="86c1f-141">When set to `postLogon`, single sign-on is performed immediately after the user logs on.</span></span><br/> |
| [<span data-ttu-id="86c1f-142">**userBasedVirtualLan**</span><span class="sxs-lookup"><span data-stu-id="86c1f-142">**userBasedVirtualLan**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md) | <span data-ttu-id="86c1f-143">boolean</span><span class="sxs-lookup"><span data-stu-id="86c1f-143">boolean</span></span> | <span data-ttu-id="86c1f-144">Especifica si la LAN virtual (VLAN) usada por el dispositivo cambia en función de las credenciales del usuario.</span><span class="sxs-lookup"><span data-stu-id="86c1f-144">Specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span><br/>                                                                                                                   |



## <a name="remarks"></a><span data-ttu-id="86c1f-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86c1f-145">Remarks</span></span>

<span data-ttu-id="86c1f-146">Para ver la lista de elementos secundarios en una estructura similar a un árbol, vea [elementos de esquema Onex](onexschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="86c1f-146">To view the list of child elements in a tree-like structure, see [OneX Schema Elements](onexschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="86c1f-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86c1f-147">Requirements</span></span>



| <span data-ttu-id="86c1f-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="86c1f-148">Requirement</span></span> | <span data-ttu-id="86c1f-149">Value</span><span class="sxs-lookup"><span data-stu-id="86c1f-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="86c1f-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86c1f-150">Minimum supported client</span></span><br/> | <span data-ttu-id="86c1f-151">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="86c1f-151">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="86c1f-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86c1f-152">Minimum supported server</span></span><br/> | <span data-ttu-id="86c1f-153">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="86c1f-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="86c1f-154">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="86c1f-154">Redistributable</span></span><br/>          | <span data-ttu-id="86c1f-155">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="86c1f-155">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



 

 





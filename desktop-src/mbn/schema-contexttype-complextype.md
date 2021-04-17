---
description: Especifica el contexto de connenction de un dispositivo de banda ancha móvil.
ms.assetid: 513e744d-bd62-43e9-a636-6690867d8b9b
title: Tipo complejo de contextType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- contextType
api_type:
- Schema
ms.openlocfilehash: 63d221c6bd388196abfb73a8ac38a26de516d0df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659801"
---
# <a name="contexttype-complex-type"></a><span data-ttu-id="6d89c-103">Tipo complejo de contextType</span><span class="sxs-lookup"><span data-stu-id="6d89c-103">contextType Complex Type</span></span>

<span data-ttu-id="6d89c-104">El tipo complejo **contextType** especifica el contexto connenction de un dispositivo de banda ancha móvil.</span><span class="sxs-lookup"><span data-stu-id="6d89c-104">The **contextType** complex type specifies the connenction context of a Mobile Broadband device.</span></span>

``` syntax
<xs:complexType name="contextType">
    <xs:sequence>
        <xs:element name="AccessString"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:minLength
                        value="1"
                     />
                    <xs:maxLength
                        value="100"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="UserLogonCred"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="UserName"
                        type="nameType"
                     />
                    <xs:element name="IgnorePassword"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element name="Password"
                        type="string"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:element name="Compression"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:enumeration
                        value="DISABLE"
                     />
                    <xs:enumeration
                        value="ENABLE"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="AuthProtocol"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:enumeration
                        value="NONE"
                     />
                    <xs:enumeration
                        value="PAP"
                     />
                    <xs:enumeration
                        value="CHAP"
                     />
                    <xs:enumeration
                        value="MsCHAPv2"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="6d89c-105">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6d89c-105">Child elements</span></span>



| <span data-ttu-id="6d89c-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="6d89c-106">Element</span></span>                                                               | <span data-ttu-id="6d89c-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="6d89c-107">Type</span></span>                                           | <span data-ttu-id="6d89c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d89c-108">Description</span></span>                                                                                    |
|-----------------------------------------------------------------------|------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d89c-109">**AccessString**</span><span class="sxs-lookup"><span data-stu-id="6d89c-109">**AccessString**</span></span>](schema-accessstring-contexttype-element.md)       |                                                | <span data-ttu-id="6d89c-110">APN o cadena de marcado que se va a usar para establecer una conexión de datos</span><span class="sxs-lookup"><span data-stu-id="6d89c-110">APN or dial string to be used to establish a data connection</span></span><br/>                        |
| [<span data-ttu-id="6d89c-111">**AuthProtocol**</span><span class="sxs-lookup"><span data-stu-id="6d89c-111">**AuthProtocol**</span></span>](schema-authprotocol-contexttype-element.md)       |                                                | <span data-ttu-id="6d89c-112">Protocolo de autenticación que se va a usar para activar un contexto PDP.</span><span class="sxs-lookup"><span data-stu-id="6d89c-112">Authentication protocol to be used for activating a PDP context.</span></span><br/>                    |
| [<span data-ttu-id="6d89c-113">**Compresión**</span><span class="sxs-lookup"><span data-stu-id="6d89c-113">**Compression**</span></span>](schema-compression-contexttype-element.md)         |                                                | <span data-ttu-id="6d89c-114">Especifica si se usará la compresión en el vínculo de datos para el encabezado y la transferencia de datos</span><span class="sxs-lookup"><span data-stu-id="6d89c-114">Specifies if compression will be used at the data link for header and data transfer</span></span><br/> |
| [<span data-ttu-id="6d89c-115">**IgnorePassword**</span><span class="sxs-lookup"><span data-stu-id="6d89c-115">**IgnorePassword**</span></span>](schema-ignorepassword-userlogoncred-element.md) | <span data-ttu-id="6d89c-116">boolean</span><span class="sxs-lookup"><span data-stu-id="6d89c-116">boolean</span></span>                                        | <span data-ttu-id="6d89c-117">Cómo administrar las contraseñas al actualizar perfiles.</span><span class="sxs-lookup"><span data-stu-id="6d89c-117">How to handle passwords when upgrading profiles.</span></span><br/>                                    |
| [<span data-ttu-id="6d89c-118">**Contraseña**</span><span class="sxs-lookup"><span data-stu-id="6d89c-118">**Password**</span></span>](schema-password-userlogoncred-element.md)             | <span data-ttu-id="6d89c-119">string</span><span class="sxs-lookup"><span data-stu-id="6d89c-119">string</span></span>                                         | <span data-ttu-id="6d89c-120">Contraseña usada para autenticar a un usuario</span><span class="sxs-lookup"><span data-stu-id="6d89c-120">Password used to authenticate a user</span></span><br/>                                                |
| [<span data-ttu-id="6d89c-121">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="6d89c-121">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)     |                                                | <span data-ttu-id="6d89c-122">Credenciales de inicio de sesión para una conexión.</span><span class="sxs-lookup"><span data-stu-id="6d89c-122">Log on credentials for a connection.</span></span><br/>                                                |
| [<span data-ttu-id="6d89c-123">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="6d89c-123">**UserName**</span></span>](schema-username-userlogoncred-element.md)             | [<span data-ttu-id="6d89c-124">**nameType**</span><span class="sxs-lookup"><span data-stu-id="6d89c-124">**nameType**</span></span>](schema-nametype-simpletype.md) | <span data-ttu-id="6d89c-125">Nombre de usuario para el inicio de sesión</span><span class="sxs-lookup"><span data-stu-id="6d89c-125">User name for logon</span></span><br/>                                                                 |



## <a name="requirements"></a><span data-ttu-id="6d89c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d89c-126">Requirements</span></span>



| <span data-ttu-id="6d89c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d89c-127">Requirement</span></span> | <span data-ttu-id="6d89c-128">Value</span><span class="sxs-lookup"><span data-stu-id="6d89c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="6d89c-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d89c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6d89c-130">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="6d89c-130">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="6d89c-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d89c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6d89c-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6d89c-132">None supported</span></span><br/>                         |



 

 





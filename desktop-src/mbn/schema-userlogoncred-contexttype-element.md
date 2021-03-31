---
description: Contiene las credenciales de inicio de sesión de una conexión.
ms.assetid: 79c1d277-6284-4adb-a1bd-6c207b37e33e
title: Elemento UserLogonCred (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UserLogonCred
api_type:
- Schema
ms.openlocfilehash: d3dc0c22d6242ee894545bd61f839574afd06141
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154469"
---
# <a name="userlogoncred-contexttype-element"></a><span data-ttu-id="c8a8c-103">Elemento UserLogonCred (contextType)</span><span class="sxs-lookup"><span data-stu-id="c8a8c-103">UserLogonCred (contextType) Element</span></span>

<span data-ttu-id="c8a8c-104">El elemento **UserLogonCred (contextType)** contiene las credenciales de inicio de sesión de una conexión.</span><span class="sxs-lookup"><span data-stu-id="c8a8c-104">The **UserLogonCred (contextType)** element contains logon credentials for a connection.</span></span>

<span data-ttu-id="c8a8c-105">Este elemento puede tener los siguientes elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="c8a8c-105">This element can have the following child elements.</span></span>

-   [<span data-ttu-id="c8a8c-106">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c8a8c-106">**UserName**</span></span>](schema-username-userlogoncred-element.md)
-   [<span data-ttu-id="c8a8c-107">**Contraseña**</span><span class="sxs-lookup"><span data-stu-id="c8a8c-107">**Password**</span></span>](schema-password-userlogoncred-element.md)
-   [<span data-ttu-id="c8a8c-108">**IgnorePassword**</span><span class="sxs-lookup"><span data-stu-id="c8a8c-108">**IgnorePassword**</span></span>](schema-ignorepassword-userlogoncred-element.md)

<span data-ttu-id="c8a8c-109">Este elemento puede tener un máximo de una repetición.</span><span class="sxs-lookup"><span data-stu-id="c8a8c-109">This element can have a maximum of one occurrence.</span></span>

<span data-ttu-id="c8a8c-110">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="c8a8c-110">This element is optional.</span></span>

``` syntax
<xs:element name="UserLogonCred">
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
```

<span data-ttu-id="c8a8c-111">El elemento **UserLogonCred** se define mediante el tipo complejo de [**contextType**](schema-contexttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c8a8c-111">The **UserLogonCred** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c8a8c-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c8a8c-112">Child elements</span></span>



| <span data-ttu-id="c8a8c-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="c8a8c-113">Element</span></span>                                                               | <span data-ttu-id="c8a8c-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="c8a8c-114">Type</span></span>                                           | <span data-ttu-id="c8a8c-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8a8c-115">Description</span></span>                                                 |
|-----------------------------------------------------------------------|------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="c8a8c-116">**IgnorePassword**</span><span class="sxs-lookup"><span data-stu-id="c8a8c-116">**IgnorePassword**</span></span>](schema-ignorepassword-userlogoncred-element.md) | <span data-ttu-id="c8a8c-117">boolean</span><span class="sxs-lookup"><span data-stu-id="c8a8c-117">boolean</span></span>                                        | <span data-ttu-id="c8a8c-118">Cómo administrar las contraseñas al actualizar perfiles.</span><span class="sxs-lookup"><span data-stu-id="c8a8c-118">How to handle passwords when upgrading profiles.</span></span><br/> |
| [<span data-ttu-id="c8a8c-119">**Contraseña**</span><span class="sxs-lookup"><span data-stu-id="c8a8c-119">**Password**</span></span>](schema-password-userlogoncred-element.md)             | <span data-ttu-id="c8a8c-120">string</span><span class="sxs-lookup"><span data-stu-id="c8a8c-120">string</span></span>                                         | <span data-ttu-id="c8a8c-121">Contraseña de usuario.</span><span class="sxs-lookup"><span data-stu-id="c8a8c-121">User password.</span></span><br/>                                   |
| [<span data-ttu-id="c8a8c-122">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c8a8c-122">**UserName**</span></span>](schema-username-userlogoncred-element.md)             | [<span data-ttu-id="c8a8c-123">**nameType**</span><span class="sxs-lookup"><span data-stu-id="c8a8c-123">**nameType**</span></span>](schema-nametype-simpletype.md) | <span data-ttu-id="c8a8c-124">Nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="c8a8c-124">User name.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="c8a8c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8a8c-125">Requirements</span></span>



| <span data-ttu-id="c8a8c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8a8c-126">Requirement</span></span> | <span data-ttu-id="c8a8c-127">Value</span><span class="sxs-lookup"><span data-stu-id="c8a8c-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="c8a8c-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8a8c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c8a8c-129">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="c8a8c-129">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="c8a8c-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8a8c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c8a8c-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c8a8c-131">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="c8a8c-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8a8c-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="c8a8c-133">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="c8a8c-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c8a8c-134">**contextType**</span><span class="sxs-lookup"><span data-stu-id="c8a8c-134">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="c8a8c-135">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="c8a8c-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c8a8c-136">**Contexto (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="c8a8c-136">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 





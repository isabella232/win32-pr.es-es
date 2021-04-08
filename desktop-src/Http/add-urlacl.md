---
title: add urlacl
description: Reserva la URL especificada para las cuentas y los usuarios que no son administradores.
ms.assetid: 5d89dec3-26e6-4db8-b4cc-e9b933ac60c5
keywords:
- Agregar urlacl HTTP
topic_type:
- apiref
api_name:
- add urlacl
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 16f6cb64c0c784f3a5400e2c97e212edbc50936c
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104003751"
---
# <a name="add-urlacl"></a><span data-ttu-id="ddca5-104">add urlacl</span><span class="sxs-lookup"><span data-stu-id="ddca5-104">add urlacl</span></span>

<span data-ttu-id="ddca5-105">Reserva la URL especificada para las cuentas y los usuarios que no son administradores.</span><span class="sxs-lookup"><span data-stu-id="ddca5-105">Reserves the specified URL for non-administrator users and accounts.</span></span> <span data-ttu-id="ddca5-106">La lista de control de acceso discrecional (DACL) se puede especificar mediante el uso de un nombre de cuenta con los parámetros Listen y Delegate o mediante una cadena de lenguaje de definición de descriptores de seguridad (SDDL).</span><span class="sxs-lookup"><span data-stu-id="ddca5-106">The discretionary access control list (DACL) can be specified by using an account name with the listen and delegate parameters or by using a security descriptor definition language (SDDL) string.</span></span>

``` syntax
add urlacl [url=]string
           [[user=]string
           {[[listen={yes|no}] [delegate={yes|no}]] | [sddl=]string}

 
```

## <a name="parameters"></a><span data-ttu-id="ddca5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ddca5-107">Parameters</span></span>

<dl> <span data-ttu-id="ddca5-108"><dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[URL =] cadena**
</dt> </span><span class="sxs-lookup"><span data-stu-id="ddca5-108"><dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[url=] string**
</dt> </span></span><dd>

<span data-ttu-id="ddca5-109">Especifica la dirección URL completa.</span><span class="sxs-lookup"><span data-stu-id="ddca5-109">Specifies the fully qualified URL.</span></span>

<span data-ttu-id="ddca5-110"></dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**[user =] cadena**
</dt> </span><span class="sxs-lookup"><span data-stu-id="ddca5-110"></dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**[user=] string**
</dt> </span></span><dd>

<span data-ttu-id="ddca5-111">Especifica el nombre del usuario o del grupo de usuarios.</span><span class="sxs-lookup"><span data-stu-id="ddca5-111">Specifies the user or user group name.</span></span>

</dd> <dt>

<span data-ttu-id="ddca5-112"><span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[Listen = {sí \| no}\]**</span><span class="sxs-lookup"><span data-stu-id="ddca5-112"><span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[listen={yes\|no}\]**</span></span>
</dt> <dd>

<span data-ttu-id="ddca5-113">Especifica uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="ddca5-113">Specifies one of the following values:</span></span>

-   <span data-ttu-id="ddca5-114">sí: permite al usuario registrar las direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="ddca5-114">yes: Allows the user to register URLs.</span></span> <span data-ttu-id="ddca5-115">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ddca5-115">This is the default value.</span></span>
-   <span data-ttu-id="ddca5-116">no: deniega al usuario el registro de las direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="ddca5-116">no: Denies the user from registering URLs.</span></span>

</dd> <dt>

<span data-ttu-id="ddca5-117"><span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[Delegado = {sí \| no}\]**</span><span class="sxs-lookup"><span data-stu-id="ddca5-117"><span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[delegate={yes\|no}\]**</span></span>
</dt> <dd>

<span data-ttu-id="ddca5-118">Especifica uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="ddca5-118">Specifies one of the following values:</span></span>

-   <span data-ttu-id="ddca5-119">sí: permite que el usuario delegue las direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="ddca5-119">yes: Allows the user to delegate URLs.</span></span>
-   <span data-ttu-id="ddca5-120">no: deniega al usuario que delegue las direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="ddca5-120">no: Denies the user from delegating URLs.</span></span> <span data-ttu-id="ddca5-121">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ddca5-121">This is the default value.</span></span>

<span data-ttu-id="ddca5-122"></dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[SDDL =] cadena**
</dt> </span><span class="sxs-lookup"><span data-stu-id="ddca5-122"></dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[sddl=] string**
</dt> </span></span><dd>

<span data-ttu-id="ddca5-123">Especifica la cadena SDDL que describe la DACL.</span><span class="sxs-lookup"><span data-stu-id="ddca5-123">Specifies the SDDL string that describes the DACL.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="ddca5-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ddca5-124">Examples</span></span>

* <span data-ttu-id="ddca5-125">add urlacl url=https://+:80/MyUri user=DOMAIN\\ user</span><span class="sxs-lookup"><span data-stu-id="ddca5-125">add urlacl url=https://+:80/MyUri user=DOMAIN\\user</span></span>

* <span data-ttu-id="ddca5-126">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes</span><span class="sxs-lookup"><span data-stu-id="ddca5-126">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes</span></span>

* <span data-ttu-id="ddca5-127">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no</span><span class="sxs-lookup"><span data-stu-id="ddca5-127">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no</span></span>

 
## <a name="see-also"></a><span data-ttu-id="ddca5-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ddca5-128">See Also</span></span>

* [<span data-ttu-id="ddca5-129">Comandos http Netsh</span><span class="sxs-lookup"><span data-stu-id="ddca5-129">Netsh http commands</span></span>](/windows-server/networking/technologies/netsh/netsh-http#add-urlacl)
 
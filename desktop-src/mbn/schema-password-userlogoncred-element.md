---
description: Especifica la contraseña que se usa para autenticar a un usuario.
ms.assetid: 9c02413b-a4c7-4c1f-a150-e27cc125faf6
title: Password (UserLogonCred), elemento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Password
api_type:
- Schema
ms.openlocfilehash: b05e34bcbaa91aba5cbfbd14f2bc8534aa91dd37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666491"
---
# <a name="password-userlogoncred-element"></a><span data-ttu-id="d40d9-103">Password (UserLogonCred), elemento</span><span class="sxs-lookup"><span data-stu-id="d40d9-103">Password (UserLogonCred) Element</span></span>

<span data-ttu-id="d40d9-104">El elemento [**password (UserLogonCred)**](schema-ignorepassword-userlogoncred-element.md) especifica la contraseña que se usa para autenticar a un usuario.</span><span class="sxs-lookup"><span data-stu-id="d40d9-104">The [**Password (UserLogonCred)**](schema-ignorepassword-userlogoncred-element.md) element specifies the password used to authenticate a user.</span></span>

<span data-ttu-id="d40d9-105">El elemento es una cadena de hasta 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d40d9-105">The element is a string of up to 255 characters.</span></span>

<span data-ttu-id="d40d9-106">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="d40d9-106">This element is optional.</span></span>

``` syntax
<xs:element name="Password"
    type="string"
 />
```

<span data-ttu-id="d40d9-107">El elemento de **contraseña** se define mediante el elemento [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d40d9-107">The **Password** element is defined by the [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="d40d9-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d40d9-108">Requirements</span></span>



| <span data-ttu-id="d40d9-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="d40d9-109">Requirement</span></span> | <span data-ttu-id="d40d9-110">Value</span><span class="sxs-lookup"><span data-stu-id="d40d9-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="d40d9-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d40d9-111">Minimum supported client</span></span><br/> | <span data-ttu-id="d40d9-112">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="d40d9-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="d40d9-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d40d9-113">Minimum supported server</span></span><br/> | <span data-ttu-id="d40d9-114">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d40d9-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="d40d9-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="d40d9-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="d40d9-116">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="d40d9-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d40d9-117">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="d40d9-117">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

<span data-ttu-id="d40d9-118">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="d40d9-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d40d9-119">**UserLogonCred (contextType)**</span><span class="sxs-lookup"><span data-stu-id="d40d9-119">**UserLogonCred (contextType)**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 





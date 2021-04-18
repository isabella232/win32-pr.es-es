---
description: Especifica cómo administrar las contraseñas al actualizar perfiles.
ms.assetid: 74d7ceb1-d778-4a12-907b-0528d9ff45be
title: Elemento IgnorePassword (UserLogonCred)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnorePassword
api_type:
- Schema
ms.openlocfilehash: 40211a8f848d8d0551ed39297178bc985d9efba4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715255"
---
# <a name="ignorepassword-userlogoncred-element"></a><span data-ttu-id="a6807-103">Elemento IgnorePassword (UserLogonCred)</span><span class="sxs-lookup"><span data-stu-id="a6807-103">IgnorePassword (UserLogonCred) Element</span></span>

<span data-ttu-id="a6807-104">El elemento **IgnorePassword (UserLogonCred)** especifica cómo administrar las contraseñas al actualizar perfiles.</span><span class="sxs-lookup"><span data-stu-id="a6807-104">The **IgnorePassword (UserLogonCred)** element specifies how to handle passwords when upgrading profiles.</span></span>

<span data-ttu-id="a6807-105">Si se establece en **true** y existe un perfil con el mismo nombre en el momento de la operación de actualización, se tomará la contraseña de ese perfil y se almacenará en el perfil nuevo.</span><span class="sxs-lookup"><span data-stu-id="a6807-105">If set to **TRUE** and a profile with the same name exists at the time of the update operation, then the password from that profile will be taken and stored in new profile.</span></span>

<span data-ttu-id="a6807-106">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="a6807-106">This element is optional.</span></span>

``` syntax
<xs:element name="IgnorePassword"
    type="boolean"
 />
```

<span data-ttu-id="a6807-107">El elemento **IgnorePassword** se define mediante el elemento [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a6807-107">The **IgnorePassword** element is defined by the [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6807-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6807-108">Requirements</span></span>



| <span data-ttu-id="a6807-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6807-109">Requirement</span></span> | <span data-ttu-id="a6807-110">Value</span><span class="sxs-lookup"><span data-stu-id="a6807-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="a6807-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6807-111">Minimum supported client</span></span><br/> | <span data-ttu-id="a6807-112">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="a6807-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="a6807-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6807-113">Minimum supported server</span></span><br/> | <span data-ttu-id="a6807-114">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a6807-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="a6807-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6807-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="a6807-116">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="a6807-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a6807-117">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="a6807-117">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

<span data-ttu-id="a6807-118">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="a6807-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a6807-119">**UserLogonCred (contextType)**</span><span class="sxs-lookup"><span data-stu-id="a6807-119">**UserLogonCred (contextType)**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 





---
title: Los atributos wire_marshal y user_marshal
description: En esta sección se describe la implementación de la conversión de tipos de datos de programador mediante el uso de los atributos MIDL \ cable \_ Marshal \ y \ User \_ Marshal \.
ms.assetid: 0ee2ce86-cd14-4659-a69f-6336145359da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a789f11fa15a20eab0fcd468cc410bb5a7200717
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078166"
---
# <a name="the-wire_marshal-and-user_marshal-attributes"></a><span data-ttu-id="cae7c-103">Atributos de serialización de conexión \_ y cálculo de referencias del usuario \_</span><span class="sxs-lookup"><span data-stu-id="cae7c-103">The wire\_marshal and user\_marshal Attributes</span></span>

<span data-ttu-id="cae7c-104">En esta sección se describe la implementación de la conversión de tipos de datos de programador mediante los atributos de serialización y cálculo de referencias de \[ [red \_ ](/windows/desktop/Midl/wire-marshal) de MIDL \] \[ [ \_ ](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="cae7c-104">This section discusses the implementation of programmer data type conversion using the MIDL \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="cae7c-105">La información se presenta en las secciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="cae7c-105">The information is presented in the following sections:</span></span>

-   [<span data-ttu-id="cae7c-106">Atributo de \_ serialización de cable</span><span class="sxs-lookup"><span data-stu-id="cae7c-106">The wire\_marshal Attribute</span></span>](the-wire-marshal-attribute.md)
-   [<span data-ttu-id="cae7c-107">Atributo User \_ Marshal</span><span class="sxs-lookup"><span data-stu-id="cae7c-107">The user\_marshal Attribute</span></span>](the-user-marshal-attribute.md)
-   [<span data-ttu-id="cae7c-108">La función de tipo de \_ usuario</span><span class="sxs-lookup"><span data-stu-id="cae7c-108">The type\_UserSize Function</span></span>](the-type-usersize-function.md)
-   [<span data-ttu-id="cae7c-109">La \_ función type UserMarshal</span><span class="sxs-lookup"><span data-stu-id="cae7c-109">The type\_UserMarshal Function</span></span>](the-type-usermarshal-function.md)
-   [<span data-ttu-id="cae7c-110">La \_ función type UserUnmarshal</span><span class="sxs-lookup"><span data-stu-id="cae7c-110">The type\_UserUnmarshal Function</span></span>](the-type-userunmarshal-function.md)
-   [<span data-ttu-id="cae7c-111">La \_ función type UserFree</span><span class="sxs-lookup"><span data-stu-id="cae7c-111">The type\_UserFree Function</span></span>](the-type-userfree-function.md)
-   [<span data-ttu-id="cae7c-112">Serialización de reglas para serialización de usuario \_ y \_ serialización de conexión</span><span class="sxs-lookup"><span data-stu-id="cae7c-112">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)

 

 
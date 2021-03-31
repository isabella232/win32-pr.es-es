---
title: OP_POLICY_ELEMENT_LIST
description: Definición de OP_POLICY_ELEMENT_LIST IDL
ms.assetid: 1eebbdd2-655b-4bd3-938c-6bc687ffe7bb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 3c46e7208e6c142b9f58a7704be9bd3461c845b2
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "103797175"
---
# <a name="op_policy_element_list-structure"></a><span data-ttu-id="b6ea1-103">Estructura de OP_POLICY_ELEMENT_LIST</span><span class="sxs-lookup"><span data-stu-id="b6ea1-103">OP_POLICY_ELEMENT_LIST structure</span></span>

<span data-ttu-id="b6ea1-104">Define una clave del Registro raíz y una matriz de elementos de clave del registro que se van a configurar bajo esa clave.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-104">Defines  a root registry key and an array of registry key elements to be configured under that key.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6ea1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6ea1-105">Syntax</span></span>

```C++
typedef struct _OP_POLICY_ELEMENT_LIST
{
    [string] wchar_t                            *pSource;
    ULONG                                       ulRootKeyId;
    ULONG                                       cElements;
    [size_is(cElements)]    POP_POLICY_ELEMENT  pElements;
} OP_POLICY_ELEMENT_LIST, *POP_POLICY_ELEMENT_LIST;
```

## <a name="members"></a><span data-ttu-id="b6ea1-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="b6ea1-106">Members</span></span>

### <a name="psource"></a><span data-ttu-id="b6ea1-107">pSource</span><span class="sxs-lookup"><span data-stu-id="b6ea1-107">pSource</span></span>

<span data-ttu-id="b6ea1-108">Contiene la ruta de acceso del archivo directiva de grupo desde el que se produjeron los elementos contenidos.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-108">Contains the path of the Group Policy file that the contained elements were sourced from.</span></span>

### <a name="ulrootkeyid"></a><span data-ttu-id="b6ea1-109">ulRootKeyId</span><span class="sxs-lookup"><span data-stu-id="b6ea1-109">ulRootKeyId</span></span>

<span data-ttu-id="b6ea1-110">Contiene el identificador de la clave del Registro raíz; Actualmente debe establecerse en HKEY_LOCAL_MACHINE.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-110">Contains the identifier of the root registry key; currently must be set to HKEY_LOCAL_MACHINE.</span></span>

### <a name="celements"></a><span data-ttu-id="b6ea1-111">cElements</span><span class="sxs-lookup"><span data-stu-id="b6ea1-111">cElements</span></span>

<span data-ttu-id="b6ea1-112">Contiene el número de elementos de los mismos.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-112">Contains the number of elements in pElements.</span></span>

### <a name="pelements"></a><span data-ttu-id="b6ea1-113">Los mismos</span><span class="sxs-lookup"><span data-stu-id="b6ea1-113">pElements</span></span>

<span data-ttu-id="b6ea1-114">Contiene una matriz de elementos OP_POLICY_ELEMENT.</span><span class="sxs-lookup"><span data-stu-id="b6ea1-114">Contains an array of OP_POLICY_ELEMENT elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="b6ea1-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6ea1-115">See also</span></span>

[<span data-ttu-id="b6ea1-116">**Definiciones IDL de unión a dominio sin conexión**</span><span class="sxs-lookup"><span data-stu-id="b6ea1-116">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="b6ea1-117">**\_elemento de directiva de OP \_**</span><span class="sxs-lookup"><span data-stu-id="b6ea1-117">**OP\_POLICY\_ELEMENT**</span></span>](odj-op_policy_element.md)

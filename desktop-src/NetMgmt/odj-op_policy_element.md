---
title: OP_POLICY_ELEMENT
description: Definición de OP_POLICY_ELEMENT IDL
ms.assetid: 69f6e0e7-3f47-4fee-8a4c-df94093dcffa
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: df6fc6852a5efd0a6a2e01a805878ed51bc7c263
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "104359564"
---
# <a name="op_policy_element-structure"></a><span data-ttu-id="39863-103">Estructura de OP_POLICY_ELEMENT</span><span class="sxs-lookup"><span data-stu-id="39863-103">OP_POLICY_ELEMENT structure</span></span>

<span data-ttu-id="39863-104">Define una clave del registro y un nombre de valor, tipo y valor que deben configurarse bajo esa clave.</span><span class="sxs-lookup"><span data-stu-id="39863-104">Defines a registry key and a value name, type, and value that should be configured under that key.</span></span>

## <a name="syntax"></a><span data-ttu-id="39863-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39863-105">Syntax</span></span>

```C++
typedef struct _OP_POLICY_ELEMENT
{
    [string] wchar_t                *pKeyPath;
    [string] wchar_t                *pValueName;
    ULONG                           ulValueType;
    ULONG                           cbValueData;
    [size_is(cbValueData)]  PBYTE   pValueData;
} OP_POLICY_ELEMENT, *POP_POLICY_ELEMENT;
```

## <a name="members"></a><span data-ttu-id="39863-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="39863-106">Members</span></span>

### <a name="pkeypath"></a><span data-ttu-id="39863-107">pKeyPath</span><span class="sxs-lookup"><span data-stu-id="39863-107">pKeyPath</span></span>

<span data-ttu-id="39863-108">Contiene la ruta de acceso de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="39863-108">Contains the path of the registry key.</span></span>

### <a name="pvaluename"></a><span data-ttu-id="39863-109">pValueName</span><span class="sxs-lookup"><span data-stu-id="39863-109">pValueName</span></span>

<span data-ttu-id="39863-110">Contiene el nombre del valor del registro.</span><span class="sxs-lookup"><span data-stu-id="39863-110">Contains the name of the registry value.</span></span>

### <a name="ulvaluetype"></a><span data-ttu-id="39863-111">ulValueType</span><span class="sxs-lookup"><span data-stu-id="39863-111">ulValueType</span></span>

<span data-ttu-id="39863-112">Contiene uno de los valores de los [tipos de valor del registro](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="39863-112">Contains one of the values from [Registry Value Types](../sysinfo/registry-value-types.md).</span></span>

### <a name="cbvaluedata"></a><span data-ttu-id="39863-113">cbValueData</span><span class="sxs-lookup"><span data-stu-id="39863-113">cbValueData</span></span>

<span data-ttu-id="39863-114">Contiene el tamaño de pValueData en bytes.</span><span class="sxs-lookup"><span data-stu-id="39863-114">Contains the size of pValueData in bytes.</span></span>

### <a name="ulvaluetype"></a><span data-ttu-id="39863-115">ulValueType</span><span class="sxs-lookup"><span data-stu-id="39863-115">ulValueType</span></span>

<span data-ttu-id="39863-116">Contiene el valor del valor del registro.</span><span class="sxs-lookup"><span data-stu-id="39863-116">Contains the value of the registry value.</span></span>

## <a name="see-also"></a><span data-ttu-id="39863-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="39863-117">See also</span></span>

[<span data-ttu-id="39863-118">**Definiciones IDL de unión a dominio sin conexión**</span><span class="sxs-lookup"><span data-stu-id="39863-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
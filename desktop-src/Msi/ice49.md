---
description: ICE49 comprueba las entradas del Registro predeterminadas que no son del \_ tipo REG SZ.
ms.assetid: 53d976fe-07d2-4b68-ae21-1dbd00d76942
title: ICE49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edc5ba319380e92fe7d1b7410673c1c688eb337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911913"
---
# <a name="ice49"></a><span data-ttu-id="93313-103">ICE49</span><span class="sxs-lookup"><span data-stu-id="93313-103">ICE49</span></span>

<span data-ttu-id="93313-104">ICE49 comprueba las entradas del Registro predeterminadas que no son del tipo **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="93313-104">ICE49 checks for default registry entries that are not a **REG\_SZ** type.</span></span>

## <a name="result"></a><span data-ttu-id="93313-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="93313-105">Result</span></span>

<span data-ttu-id="93313-106">ICE49 publica una advertencia si hay una entrada del registro predeterminada que no es un **tipo \_ de reg** .</span><span class="sxs-lookup"><span data-stu-id="93313-106">ICE49 posts an warning if there is a default registry entry that is not a **REG\_SZ** type.</span></span>

## <a name="example"></a><span data-ttu-id="93313-107">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="93313-107">Example</span></span>

<span data-ttu-id="93313-108">ICE49 notifica la siguiente advertencia para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="93313-108">ICE49 reports the following warning for the example shown.</span></span>

``` syntax
Reg Entry 'Reg1' is not of type REG_SZ. Default types must be REG_SZ 
    on Win95 Systems. Make sure the component is conditionalized 
    to never be installed on Win95 machines.
```

<span data-ttu-id="93313-109">El valor ' \# 123 ' es un valor del registro **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="93313-109">The value '\#123' is a **DWORD** registry value.</span></span>

<span data-ttu-id="93313-110">[Tabla del registro](registry-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="93313-110">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="93313-111">Registro</span><span class="sxs-lookup"><span data-stu-id="93313-111">Registry</span></span> | <span data-ttu-id="93313-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="93313-112">Name</span></span> | <span data-ttu-id="93313-113">Value</span><span class="sxs-lookup"><span data-stu-id="93313-113">Value</span></span> |
|----------|------|-------|
| <span data-ttu-id="93313-114">Reg1</span><span class="sxs-lookup"><span data-stu-id="93313-114">Reg1</span></span>     |      | <span data-ttu-id="93313-115">\#123</span><span class="sxs-lookup"><span data-stu-id="93313-115">\#123</span></span> |



 

<span data-ttu-id="93313-116">Para corregir esta advertencia, cambie el valor a tipo **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="93313-116">To fix this warning, change the value to type **REG\_SZ**.</span></span>

<span data-ttu-id="93313-117">Los componentes que no son de **reg \_** son válidos.</span><span class="sxs-lookup"><span data-stu-id="93313-117">Components with non-**REG\_SZ** are valid.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93313-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="93313-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93313-119">Sintaxis de la instrucción condicional</span><span class="sxs-lookup"><span data-stu-id="93313-119">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> <dt>

[<span data-ttu-id="93313-120">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="93313-120">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




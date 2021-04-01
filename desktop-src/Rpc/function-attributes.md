---
title: Atributos de función
description: Los atributos \ callback \ y \ local \ se pueden aplicar como atributos de función.
ms.assetid: 05e19164-072c-4a5a-878d-845273975854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ef199b937d5a3e9a8444be9ed65749da007ced
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793383"
---
# <a name="function-attributes"></a><span data-ttu-id="e9b96-103">Atributos de función</span><span class="sxs-lookup"><span data-stu-id="e9b96-103">Function Attributes</span></span>

<span data-ttu-id="e9b96-104">La **\[** [**devolución de llamada**](/windows/desktop/Midl/callback) **\]** y **\[** [](/windows/desktop/Midl/local) **\]** los atributos locales se pueden aplicar como atributos de función.</span><span class="sxs-lookup"><span data-stu-id="e9b96-104">The **\[**[**callback**](/windows/desktop/Midl/callback)**\]** and **\[**[**local**](/windows/desktop/Midl/local)**\]** attributes can be applied as function attributes.</span></span>

<span data-ttu-id="e9b96-105">Una devolución de llamada es una llamada remota entre el servidor y el cliente que se ejecuta como parte de un subproceso conceptual de ejecución única.</span><span class="sxs-lookup"><span data-stu-id="e9b96-105">A callback is a remote call from server to client that executes as part of a conceptual single-execution thread.</span></span> <span data-ttu-id="e9b96-106">Una devolución de llamada siempre se emite en el contexto de una llamada remota (o devolución de llamada) y la ejecuta el subproceso que emitió la llamada remota original (o devolución de llamada).</span><span class="sxs-lookup"><span data-stu-id="e9b96-106">A callback is always issued in the context of a remote call (or callback) and is executed by the thread that issued the original remote call (or callback).</span></span>

<span data-ttu-id="e9b96-107">A menudo es conveniente colocar una declaración de procedimiento local en el archivo IDL, ya que se trata del lugar lógico para describir las interfaces de un paquete.</span><span class="sxs-lookup"><span data-stu-id="e9b96-107">It is often desirable to place a local procedure declaration in the IDL file, since this is the logical place to describe interfaces to a package.</span></span> <span data-ttu-id="e9b96-108">El **\[** [](/windows/desktop/Midl/local) **\]** atributo local indica que una declaración de procedimiento no es realmente una función remota, sino un procedimiento local.</span><span class="sxs-lookup"><span data-stu-id="e9b96-108">The **\[**[**local**](/windows/desktop/Midl/local)**\]** attribute indicates that a procedure declaration is not actually a remote function, but a local procedure.</span></span> <span data-ttu-id="e9b96-109">El compilador MIDL no genera ningún código auxiliar para las funciones con el atributo **\[ local \]** .</span><span class="sxs-lookup"><span data-stu-id="e9b96-109">The MIDL compiler does not generate any stubs for functions with the **\[local\]** attribute.</span></span>

<span data-ttu-id="e9b96-110">Es importante tener en cuenta que no se recomienda el uso de la **\[** [**devolución de llamada**](/windows/desktop/Midl/callback) **\]** en la programación multiproceso.</span><span class="sxs-lookup"><span data-stu-id="e9b96-110">It is important to note that the use of **\[**[**callback**](/windows/desktop/Midl/callback)**\]** is not recommended in multi-thread programming.</span></span> <span data-ttu-id="e9b96-111">Como función de programación de un solo subproceso, no está equipada para admitir las demandas de seguridad que proporciona un entorno con varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="e9b96-111">As a single-thread programming function, it is not equipped to support the security demands a multi-thread environment provides.</span></span>

 

 
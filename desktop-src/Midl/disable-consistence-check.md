---
title: disable_consistency_check atributo)
description: Indica a RPC que no aplique la comprobación de coherencia de la correlación.
ms.assetid: 33ba331d-56e5-4965-a844-7780ea81623d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc55197b5eb680533745a09d4fca4f5827574a7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356865"
---
# <a name="disable_consistency_check-attribute"></a><span data-ttu-id="72451-103">deshabilitar \_ atributo de comprobación de coherencia \_</span><span class="sxs-lookup"><span data-stu-id="72451-103">disable\_consistency\_check Attribute</span></span>

<span data-ttu-id="72451-104">Indica a RPC que no aplique la comprobación de coherencia de la correlación.</span><span class="sxs-lookup"><span data-stu-id="72451-104">Directs RPC to not enforce correlation consistency checking.</span></span>

``` syntax
interface interface-name
{
  return-type function-name(
        [[attribute-list,] disable_consistency_check] param-type param-name
}
```

<span data-ttu-id="72451-105">En el caso de los parámetros correlacionados, RPC exigirá que se pase un búfer que no sea NULL cuando la variable Count de correlación no sea NULL.</span><span class="sxs-lookup"><span data-stu-id="72451-105">For correlated parameters, RPC will enforce that a non-null buffer is passed when the correlation count variable is non-null.</span></span>

## <a name="example"></a><span data-ttu-id="72451-106">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="72451-106">Example</span></span>

``` syntax
HRESULT PassString( [in] DWORD Length, [in, unique, string, 
    size_is( Length )]LPWSTR MyString );
```

<span data-ttu-id="72451-107">Si el valor de la *cadena* es **null**, RPC rechazará la llamada a menos que la longitud esté establecida en 0.</span><span class="sxs-lookup"><span data-stu-id="72451-107">If *MyString* is **NULL**, RPC will reject the call unless Length is set to 0.</span></span> <span data-ttu-id="72451-108">Tenga en cuenta que RPC permitirá que la *longitud* sea 0, mientras que el valor de la *cadena* no es null, y RPC tratará la *cadena* como una asignación de búfer de longitud 0.</span><span class="sxs-lookup"><span data-stu-id="72451-108">Note that RPC will allow *Length* to be 0 while *MyString* is non-NULL, and RPC will treat *MyString* as a 0-length buffer allocation.</span></span>

## <a name="remarks"></a><span data-ttu-id="72451-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72451-109">Remarks</span></span>

<span data-ttu-id="72451-110">Para deshabilitar esta comprobación, el IDL puede contener \[ el \_ atributo deshabilitar \_ comprobación de coherencia \] en un parámetro, typedef o tipo de puntero.</span><span class="sxs-lookup"><span data-stu-id="72451-110">To disable this checking, the IDL can contain the \[disable\_consistency\_check\] attribute on a parameter, typedef, or pointer type.</span></span> <span data-ttu-id="72451-111">Esto indicará a RPC que no aplique la coherencia entre el puntero de búfer y la variable de correlación del búfer al que apunta el parámetro o el puntero.</span><span class="sxs-lookup"><span data-stu-id="72451-111">This will direct RPC to not enforce the consistency between the buffer pointer and the correlation variable for the buffer pointed to by the parameter or pointer.</span></span>

<span data-ttu-id="72451-112">Para deshabilitar la comprobación de coherencia para una compilación de MIDL completa (y deshabilitar la aplicación de la comprobación en todos los casos), se puede usar el modificador de la línea de comandos de MIDL [/backward \_ compatible maybenull \_ size](-backward-compat.md) .</span><span class="sxs-lookup"><span data-stu-id="72451-112">To disable consistency checking for an entire MIDL compilation (and disable enforcement of the checking in all cases), the MIDL command line switch [/backward\_compat maybenull\_sizeis](-backward-compat.md) can be used.</span></span> <span data-ttu-id="72451-113">Esto requiere que el destino de la compilación de MIDL sea al menos â € "Target NT60.</span><span class="sxs-lookup"><span data-stu-id="72451-113">This requires that the target of the MIDL compilation be at least â€“target NT60.</span></span>

 

 





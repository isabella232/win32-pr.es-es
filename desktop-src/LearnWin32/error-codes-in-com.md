---
title: Códigos de error en COM
description: .
ms.assetid: ed430863-f416-4611-81b4-0c31d819944a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f082afbabf367179b02c0fb3b0fc979dcda664a4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790191"
---
# <a name="error-codes-in-com"></a><span data-ttu-id="406db-103">Códigos de error en COM</span><span class="sxs-lookup"><span data-stu-id="406db-103">Error Codes in COM</span></span>

<span data-ttu-id="406db-104">Para indicar si se ha realizado correctamente o no, las funciones y los métodos COM devuelven un valor de tipo **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="406db-104">To indicate success or failure, COM methods and functions return a value of type **HRESULT**.</span></span> <span data-ttu-id="406db-105">Un **valor HRESULT** es un entero de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="406db-105">An **HRESULT** is a 32-bit integer.</span></span> <span data-ttu-id="406db-106">El bit de orden superior de **HRESULT** indica que el resultado es correcto o incorrecto.</span><span class="sxs-lookup"><span data-stu-id="406db-106">The high-order bit of the **HRESULT** signals success or failure.</span></span> <span data-ttu-id="406db-107">Cero (0) indica que se ha realizado correctamente y 1 indica un error.</span><span class="sxs-lookup"><span data-stu-id="406db-107">Zero (0) indicates success and 1 indicates failure.</span></span>

<span data-ttu-id="406db-108">Esto produce los siguientes intervalos numéricos:</span><span class="sxs-lookup"><span data-stu-id="406db-108">This produces the following numeric ranges:</span></span>

-   <span data-ttu-id="406db-109">Códigos de éxito: 0X0 – 0x7FFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="406db-109">Success codes: 0x0–0x7FFFFFFF.</span></span>
-   <span data-ttu-id="406db-110">Códigos de error: 0x80000000 – 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="406db-110">Error codes: 0x80000000–0xFFFFFFFF.</span></span>

<span data-ttu-id="406db-111">Un número pequeño de métodos COM no devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="406db-111">A small number of COM methods do not return an **HRESULT** value.</span></span> <span data-ttu-id="406db-112">Por ejemplo, los métodos [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) y [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) devuelven valores Long sin signo.</span><span class="sxs-lookup"><span data-stu-id="406db-112">For example, the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods return unsigned long values.</span></span> <span data-ttu-id="406db-113">Pero todos los métodos COM que devuelven un código de error lo hace devolviendo un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="406db-113">But every COM method that returns an error code does so by returning an **HRESULT** value.</span></span>

<span data-ttu-id="406db-114">Para comprobar si un método COM se realiza correctamente, examine el bit de orden superior del **HRESULT** devuelto.</span><span class="sxs-lookup"><span data-stu-id="406db-114">To check whether a COM method succeeds, examine the high-order bit of the returned **HRESULT**.</span></span> <span data-ttu-id="406db-115">Los encabezados de Windows SDK proporcionan dos macros que facilitan esta tarea: la macro [**Succeeded**](/windows/desktop/api/winerror/nf-winerror-succeeded) y la macro [**failed**](/windows/desktop/api/winerror/nf-winerror-failed) .</span><span class="sxs-lookup"><span data-stu-id="406db-115">The Windows SDK headers provide two macros that make this easier: the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) macro and the [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro.</span></span> <span data-ttu-id="406db-116">La macro **Succeeded** devuelve **true** si un **valor HRESULT** es un código de operación correcta y **false** si es un código de error.</span><span class="sxs-lookup"><span data-stu-id="406db-116">The **SUCCEEDED** macro returns **TRUE** if an **HRESULT** is a success code and **FALSE** if it is an error code.</span></span> <span data-ttu-id="406db-117">En el ejemplo siguiente se comprueba si [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="406db-117">The following example checks whether [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) succeeds.</span></span>


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    // The function succeeded.
}
else
{
    // Handle the error.
}
```



<span data-ttu-id="406db-118">A veces resulta más cómodo probar la condición inversa.</span><span class="sxs-lookup"><span data-stu-id="406db-118">Sometimes it is more convenient to test the inverse condition.</span></span> <span data-ttu-id="406db-119">La macro [**failed**](/windows/desktop/api/winerror/nf-winerror-failed) hace lo contrario de [**Succeeded**](/windows/desktop/api/winerror/nf-winerror-succeeded).</span><span class="sxs-lookup"><span data-stu-id="406db-119">The [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro does the opposite of [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded).</span></span> <span data-ttu-id="406db-120">Devuelve **true** para un código de error y **false** para un código de éxito.</span><span class="sxs-lookup"><span data-stu-id="406db-120">It returns **TRUE** for an error code and **FALSE** for a success code.</span></span>


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (FAILED(hr))
{
    // Handle the error.
}
else
{
    // The function succeeded.
}
```



<span data-ttu-id="406db-121">Más adelante en este módulo, veremos algunos consejos prácticos sobre cómo estructurar el código para controlar los errores de COM.</span><span class="sxs-lookup"><span data-stu-id="406db-121">Later in this module, we will look at some practical advice for how to structure your code to handle COM errors.</span></span> <span data-ttu-id="406db-122">(Vea [control de errores en com](error-handling-in-com.md)).</span><span class="sxs-lookup"><span data-stu-id="406db-122">(See [Error Handling in COM](error-handling-in-com.md).)</span></span>

## <a name="next"></a><span data-ttu-id="406db-123">Siguientes</span><span class="sxs-lookup"><span data-stu-id="406db-123">Next</span></span>

[<span data-ttu-id="406db-124">Crear un objeto en COM</span><span class="sxs-lookup"><span data-stu-id="406db-124">Creating an Object in COM</span></span>](creating-an-object-in-com.md)

 

 
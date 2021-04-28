---
title: Códigos de error en COM
description: Códigos de error en COM
ms.assetid: ed430863-f416-4611-81b4-0c31d819944a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733cbe0799a22b0f0c01ee9cb226ad7e0b8660da
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103963"
---
# <a name="error-codes-in-com"></a><span data-ttu-id="5a1ed-103">Códigos de error en COM</span><span class="sxs-lookup"><span data-stu-id="5a1ed-103">Error Codes in COM</span></span>

<span data-ttu-id="5a1ed-104">Para indicar que se ha hecho correctamente o no, los métodos COM y las funciones devuelven un valor de tipo **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5a1ed-104">To indicate success or failure, COM methods and functions return a value of type **HRESULT**.</span></span> <span data-ttu-id="5a1ed-105">Un **valor HRESULT** es un entero de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5a1ed-105">An **HRESULT** is a 32-bit integer.</span></span> <span data-ttu-id="5a1ed-106">El bit de orden superior del **valor HRESULT** indica que se ha hecho correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="5a1ed-106">The high-order bit of the **HRESULT** signals success or failure.</span></span> <span data-ttu-id="5a1ed-107">Cero (0) indica que se ha hecho correctamente y 1 indica error.</span><span class="sxs-lookup"><span data-stu-id="5a1ed-107">Zero (0) indicates success and 1 indicates failure.</span></span>

<span data-ttu-id="5a1ed-108">Esto genera los siguientes intervalos numéricos:</span><span class="sxs-lookup"><span data-stu-id="5a1ed-108">This produces the following numeric ranges:</span></span>

-   <span data-ttu-id="5a1ed-109">Códigos de éxito: 0x0–0x7FFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="5a1ed-109">Success codes: 0x0–0x7FFFFFFF.</span></span>
-   <span data-ttu-id="5a1ed-110">Códigos de error: 0x80000000–0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="5a1ed-110">Error codes: 0x80000000–0xFFFFFFFF.</span></span>

<span data-ttu-id="5a1ed-111">Un pequeño número de métodos COM no devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="5a1ed-111">A small number of COM methods do not return an **HRESULT** value.</span></span> <span data-ttu-id="5a1ed-112">Por ejemplo, los [**métodos AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) [**y Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) devuelven valores long sin signo.</span><span class="sxs-lookup"><span data-stu-id="5a1ed-112">For example, the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods return unsigned long values.</span></span> <span data-ttu-id="5a1ed-113">Pero todos los métodos COM que devuelven un código de error lo hace devolviendo un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="5a1ed-113">But every COM method that returns an error code does so by returning an **HRESULT** value.</span></span>

<span data-ttu-id="5a1ed-114">Para comprobar si un método COM se realiza correctamente, examine el bit de orden superior del **HRESULT devuelto.**</span><span class="sxs-lookup"><span data-stu-id="5a1ed-114">To check whether a COM method succeeds, examine the high-order bit of the returned **HRESULT**.</span></span> <span data-ttu-id="5a1ed-115">Los Windows SDK proporcionan dos macros que facilitan esta tarea: la macro [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) y la [**macro FAILED.**](/windows/desktop/api/winerror/nf-winerror-failed)</span><span class="sxs-lookup"><span data-stu-id="5a1ed-115">The Windows SDK headers provide two macros that make this easier: the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) macro and the [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro.</span></span> <span data-ttu-id="5a1ed-116">La **macro SUCCEEDED** devuelve **TRUE si** un **HRESULT** es un código correcto y **FALSE** si es un código de error.</span><span class="sxs-lookup"><span data-stu-id="5a1ed-116">The **SUCCEEDED** macro returns **TRUE** if an **HRESULT** is a success code and **FALSE** if it is an error code.</span></span> <span data-ttu-id="5a1ed-117">En el ejemplo siguiente se comprueba [**si CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="5a1ed-117">The following example checks whether [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) succeeds.</span></span>


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



<span data-ttu-id="5a1ed-118">A veces resulta más conveniente probar la condición inversa.</span><span class="sxs-lookup"><span data-stu-id="5a1ed-118">Sometimes it is more convenient to test the inverse condition.</span></span> <span data-ttu-id="5a1ed-119">La [**macro FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) hace lo contrario que [**SUCCEEDED.**](/windows/desktop/api/winerror/nf-winerror-succeeded)</span><span class="sxs-lookup"><span data-stu-id="5a1ed-119">The [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro does the opposite of [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded).</span></span> <span data-ttu-id="5a1ed-120">Devuelve **TRUE para** un código de error y **FALSE para** un código correcto.</span><span class="sxs-lookup"><span data-stu-id="5a1ed-120">It returns **TRUE** for an error code and **FALSE** for a success code.</span></span>


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



<span data-ttu-id="5a1ed-121">Más adelante en este módulo, se verán algunos consejos prácticos sobre cómo estructurar el código para controlar los errores COM.</span><span class="sxs-lookup"><span data-stu-id="5a1ed-121">Later in this module, we will look at some practical advice for how to structure your code to handle COM errors.</span></span> <span data-ttu-id="5a1ed-122">(Consulte [Control de errores en COM).](error-handling-in-com.md)</span><span class="sxs-lookup"><span data-stu-id="5a1ed-122">(See [Error Handling in COM](error-handling-in-com.md).)</span></span>

## <a name="next"></a><span data-ttu-id="5a1ed-123">Siguientes</span><span class="sxs-lookup"><span data-stu-id="5a1ed-123">Next</span></span>

[<span data-ttu-id="5a1ed-124">Crear un objeto en COM</span><span class="sxs-lookup"><span data-stu-id="5a1ed-124">Creating an Object in COM</span></span>](creating-an-object-in-com.md)

 

 

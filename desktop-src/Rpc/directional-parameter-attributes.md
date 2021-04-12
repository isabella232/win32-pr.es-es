---
title: Atributos direccionales (parámetro)
description: Los atributos direccionales describen si los datos se transmiten entre el cliente y el servidor, el servidor al cliente o ambos.
ms.assetid: 1e4f92ae-2d98-412f-a693-54bb09ae4674
keywords:
- RPC de llamada a procedimiento remoto, descripción, atributos direccionales
- in
- out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eec37dbf65919f5aae9e7674cf7102eddcdf5170
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149448"
---
# <a name="directional-parameter-attributes"></a><span data-ttu-id="ee335-106">Atributos direccionales (parámetro)</span><span class="sxs-lookup"><span data-stu-id="ee335-106">Directional (Parameter) Attributes</span></span>

<span data-ttu-id="ee335-107">Los atributos direccionales describen si los datos se transmiten entre el cliente y el servidor, el servidor al cliente o ambos.</span><span class="sxs-lookup"><span data-stu-id="ee335-107">Directional attributes describe whether the data is transmitted from client to server, server to client, or both.</span></span> <span data-ttu-id="ee335-108">Todos los parámetros del prototipo de función deben estar asociados a atributos direccionales.</span><span class="sxs-lookup"><span data-stu-id="ee335-108">All parameters in the function prototype must be associated with directional attributes.</span></span> <span data-ttu-id="ee335-109">Las tres combinaciones posibles de atributos direccionales son: 1) \[ [**in**](/windows/desktop/Midl/in) \] , 2) \[ [**out**](/windows/desktop/Midl/out-idl) \] y 3) \[ **in**, **out** \] .</span><span class="sxs-lookup"><span data-stu-id="ee335-109">The three possible combinations of directional attributes are: 1) \[[**in**](/windows/desktop/Midl/in)\], 2) \[[**out**](/windows/desktop/Midl/out-idl)\], and 3) \[**in**, **out**\].</span></span> <span data-ttu-id="ee335-110">Estos describen la manera en que se pasan los parámetros entre los procedimientos de llamada y los que se llaman.</span><span class="sxs-lookup"><span data-stu-id="ee335-110">These describe the way parameters are passed between calling and called procedures.</span></span> <span data-ttu-id="ee335-111">Al compilar en el valor predeterminado (modo extendido de Microsoft) y omitir un atributo direccional para un parámetro, el compilador MIDL supone un valor predeterminado de \[ **en** \] .</span><span class="sxs-lookup"><span data-stu-id="ee335-111">When you compile in the default (Microsoft-extended mode) and you omit a directional attribute for a parameter, the MIDL compiler assumes a default value of \[**in**\].</span></span>

<span data-ttu-id="ee335-112">Un \[ parámetro [**out**](/windows/desktop/Midl/out-idl) \] debe ser un puntero.</span><span class="sxs-lookup"><span data-stu-id="ee335-112">An \[[**out**](/windows/desktop/Midl/out-idl)\] parameter must be a pointer.</span></span> <span data-ttu-id="ee335-113">De hecho, el \[  \] atributo out no es significativo cuando se aplica a parámetros que no actúan como punteros, ya que los parámetros de la función de C se pasan por valor.</span><span class="sxs-lookup"><span data-stu-id="ee335-113">In fact, the \[**out**\] attribute is not meaningful when applied to parameters that do not act as pointers because C function parameters are passed by value.</span></span> <span data-ttu-id="ee335-114">En C, la función a la que se llama recibe una copia privada del valor del parámetro. no puede cambiar el valor de la función de llamada para ese parámetro.</span><span class="sxs-lookup"><span data-stu-id="ee335-114">In C, the called function receives a private copy of the parameter value; it cannot change the calling function's value for that parameter.</span></span> <span data-ttu-id="ee335-115">Sin embargo, si el parámetro actúa como un puntero, se puede utilizar para tener acceso a la memoria y modificarla.</span><span class="sxs-lookup"><span data-stu-id="ee335-115">If the parameter acts as a pointer, however, it can be used to access and modify memory.</span></span> <span data-ttu-id="ee335-116">El \[ atributo **out** \] indica que la función de servidor debe devolver el valor a la función de llamada del cliente y que se debe devolver la memoria asociada al puntero de acuerdo con los atributos asignados al puntero.</span><span class="sxs-lookup"><span data-stu-id="ee335-116">The \[**out**\] attribute indicates that the server function should return the value to the client's calling function, and that memory associated with the pointer should be returned in accordance with the attributes assigned to the pointer.</span></span>

<span data-ttu-id="ee335-117">La interfaz siguiente muestra las tres combinaciones posibles de atributos direccionales que se pueden aplicar a un parámetro.</span><span class="sxs-lookup"><span data-stu-id="ee335-117">The following interface demonstrates the three possible combinations of directional attributes that can be applied to a parameter.</span></span> <span data-ttu-id="ee335-118">La función **InOutProc** se define en el archivo IDL como:</span><span class="sxs-lookup"><span data-stu-id="ee335-118">The function **InOutProc** is defined in the IDL file as:</span></span>

``` syntax
void InOutProc ([in]       short     s1,
                [in, out]  short *  ps2,
                [out]      float *  pf3);
```

<span data-ttu-id="ee335-119">El primer parámetro, *S1*, es \[ solo [**en**](/windows/desktop/Midl/in) \] .</span><span class="sxs-lookup"><span data-stu-id="ee335-119">The first parameter, *s1*, is \[[**in**](/windows/desktop/Midl/in)\] only.</span></span> <span data-ttu-id="ee335-120">Su valor se transmite al equipo remoto, pero no se devuelve al procedimiento que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="ee335-120">Its value is transmitted to the remote computer, but is not returned to the calling procedure.</span></span> <span data-ttu-id="ee335-121">Aunque la aplicación de servidor puede cambiar su valor para *S1*, el valor de *S1* en el cliente es el mismo antes y después de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ee335-121">Although the server application can change its value for *s1*, the value of *s1* on the client is the same before and after the call.</span></span>

<span data-ttu-id="ee335-122">El segundo parámetro, *PS2*, se define en el prototipo de función como un puntero con \[ [](/windows/desktop/Midl/in) \] los atributos in y \[ [**out**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="ee335-122">The second parameter, *ps2*, is defined in the function prototype as a pointer with both \[[**in**](/windows/desktop/Midl/in)\] and \[[**out**](/windows/desktop/Midl/out-idl)\] attributes.</span></span> <span data-ttu-id="ee335-123">El \[ atributo **in** \] indica que el valor del parámetro se pasa desde el cliente al servidor.</span><span class="sxs-lookup"><span data-stu-id="ee335-123">The \[**in**\] attribute indicates that the value of the parameter is passed from the client to the server.</span></span> <span data-ttu-id="ee335-124">El \[ atributo **out** \] indica que el valor al que apunta *PS2* se devuelve al cliente.</span><span class="sxs-lookup"><span data-stu-id="ee335-124">The \[**out**\] attribute indicates that the value pointed to by *ps2* is returned to the client.</span></span>

<span data-ttu-id="ee335-125">El tercer parámetro es \[ solo [**out**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="ee335-125">The third parameter is \[[**out**](/windows/desktop/Midl/out-idl)\] only.</span></span> <span data-ttu-id="ee335-126">Se asigna espacio para el parámetro en el servidor, pero el valor no está definido en la entrada.</span><span class="sxs-lookup"><span data-stu-id="ee335-126">Space is allocated for the parameter on the server, but the value is undefined on entry.</span></span> <span data-ttu-id="ee335-127">Como se mencionó anteriormente, todos los \[ parámetros **out** \] deben ser punteros.</span><span class="sxs-lookup"><span data-stu-id="ee335-127">As mentioned above, all \[**out**\] parameters must be pointers.</span></span>

<span data-ttu-id="ee335-128">El procedimiento remoto cambia el valor de los tres parámetros, pero solo los nuevos valores de los \[ [](/windows/desktop/Midl/out-idl) \] parámetros out y \[ [**in**](/windows/desktop/Midl/in) \] están disponibles para el cliente.</span><span class="sxs-lookup"><span data-stu-id="ee335-128">The remote procedure changes the value of all three parameters, but only the new values of the \[[**out**](/windows/desktop/Midl/out-idl)\] and \[[**in**](/windows/desktop/Midl/in)\] parameters are available to the client.</span></span>


```C++
#define MAX 257

void InOutProc(short    s1,
               short * ps2,
               float * pf3)
{
    *pf3 = (float) s1 / (float) *ps2;
    *ps2 = (short) MAX - s1;
    s1++;  // in only; not changed on the client side
    return;
}
```



<span data-ttu-id="ee335-129">En la devolución de la llamada a **InOutProc**, se modifican los parámetros segundo y tercero.</span><span class="sxs-lookup"><span data-stu-id="ee335-129">On return from the call to **InOutProc**, the second and third parameters are modified.</span></span> <span data-ttu-id="ee335-130">El primer parámetro, que solo es \[ [**en**](/windows/desktop/Midl/in) \] , no cambia.</span><span class="sxs-lookup"><span data-stu-id="ee335-130">The first parameter, which is \[[**in**](/windows/desktop/Midl/in)\] only, is unchanged.</span></span>

![in (parámetros)](images/prog-a22.png)

![out (parámetros)](images/prog-a23.png)

![parámetros de salida](images/prog-a21.png)

 

 
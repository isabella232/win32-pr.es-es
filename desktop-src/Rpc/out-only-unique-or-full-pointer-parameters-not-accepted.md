---
title: Out-Only parámetros único o de puntero completo no aceptados
description: El compilador de MIDL no acepta los punteros únicos o completos. Tales especificaciones hacen que el compilador MIDL genere un mensaje de error.
ms.assetid: 0477980e-d76e-452f-9ab1-71a8ed8642d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b21baa370c1b68fb3c708a8fdb21115686646f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533363"
---
# <a name="out-only-unique-or-full-pointer-parameters-not-accepted"></a><span data-ttu-id="62dc9-104">Out-Only parámetros único o de puntero completo no aceptados</span><span class="sxs-lookup"><span data-stu-id="62dc9-104">Out-Only Unique or Full Pointer Parameters Not Accepted</span></span>

<span data-ttu-id="62dc9-105">\[ [](/windows/desktop/Midl/out-idl) \] El compilador MIDL no acepta los punteros únicos o completos que son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="62dc9-105">Unique or full pointers that are \[ [out](/windows/desktop/Midl/out-idl)\]-only are not accepted by the MIDL compiler.</span></span> <span data-ttu-id="62dc9-106">Tales especificaciones hacen que el compilador MIDL genere un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="62dc9-106">Such specifications cause the MIDL compiler to generate an error message.</span></span>

<span data-ttu-id="62dc9-107">El código auxiliar de servidor generado automáticamente tiene que asignar memoria para el puntero de forma que la aplicación de servidor pueda almacenar datos en ese área de memoria.</span><span class="sxs-lookup"><span data-stu-id="62dc9-107">The automatically generated server stub has to allocate memory for the pointer referent so that the server application can store data in that memory area.</span></span> <span data-ttu-id="62dc9-108">Según la definición de un parámetro de solo **\[ salida \]**, no se transmite información sobre el parámetro desde el cliente al servidor.</span><span class="sxs-lookup"><span data-stu-id="62dc9-108">According to the definition of an **\[out\]**-only parameter, no information about the parameter is transmitted from client to server.</span></span> <span data-ttu-id="62dc9-109">En el caso de un puntero único, que puede tomar el valor null, el código auxiliar del servidor no tiene suficiente información para duplicar correctamente el puntero único en el espacio de direcciones del servidor, ni tampoco información sobre si el puntero debe apuntar a una dirección válida o si debe establecerse en NULL.</span><span class="sxs-lookup"><span data-stu-id="62dc9-109">In the case of a unique pointer, which can take the value null, the server stub does not have enough information to correctly duplicate the unique pointer in the server's address space, nor does the stub have any information about whether the pointer should point to a valid address or whether it should be set to null.</span></span> <span data-ttu-id="62dc9-110">Por lo tanto, esta combinación no está permitida.</span><span class="sxs-lookup"><span data-stu-id="62dc9-110">Therefore, this combination is not allowed.</span></span>

<span data-ttu-id="62dc9-111">En lugar de \[ **out**, [Unique](/windows/desktop/Midl/unique) \] o \[ **out**, punteros [ptr](/windows/desktop/Midl/ptr) \] , use \[ **in**, **out**, **Unique** \] o \[ **in**, **out** o **ptr** , \] o use otro nivel de direccionamiento indirecto, como un puntero de referencia que apunte al puntero completo o único válido.</span><span class="sxs-lookup"><span data-stu-id="62dc9-111">Rather than \[**out**, [unique](/windows/desktop/Midl/unique)\] or \[**out**, [ptr](/windows/desktop/Midl/ptr)\] pointers, use \[**in**, **out**, **unique**\] or \[**in**, **out**, **ptr**\] pointers, or use another level of indirection such as a reference pointer that points to the valid unique or full pointer.</span></span>

 

 
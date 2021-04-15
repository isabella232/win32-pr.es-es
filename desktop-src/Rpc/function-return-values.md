---
title: Valores devueltos de función
description: Los valores devueltos de función son similares a los parámetros de solo lectura, ya que la aplicación cliente no proporciona sus datos.
ms.assetid: 98d8d228-7222-49bf-9f29-7749a7a76d5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ada3808d024f201ef01a5f4977149a0ab9c75e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676484"
---
# <a name="function-return-values"></a><span data-ttu-id="6bd6c-103">Valores devueltos de función</span><span class="sxs-lookup"><span data-stu-id="6bd6c-103">Function Return Values</span></span>

<span data-ttu-id="6bd6c-104">Los valores devueltos de función son similares a los parámetros de solo **\[ salida \]** porque la aplicación cliente no proporciona sus datos.</span><span class="sxs-lookup"><span data-stu-id="6bd6c-104">Function return values are similar to **\[out\]**-only parameters because their data is not provided by the client application.</span></span> <span data-ttu-id="6bd6c-105">Sin embargo, se administran de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="6bd6c-105">However they are managed differently.</span></span> <span data-ttu-id="6bd6c-106">A diferencia de los parámetros de solo **\[ salida \]**, no es necesario que sean punteros.</span><span class="sxs-lookup"><span data-stu-id="6bd6c-106">Unlike **\[out\]**-only parameters, they are not required to be pointers.</span></span> <span data-ttu-id="6bd6c-107">El procedimiento remoto puede devolver cualquier tipo de datos válido, excepto los punteros de referencia y las uniones no encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="6bd6c-107">The remote procedure can return any valid data type except reference pointers and nonencapsulated unions.</span></span>

<span data-ttu-id="6bd6c-108">Sin embargo, se recomienda el uso de un parámetro **\[ out \]** en lugar de un valor devuelto para tipos de datos complejos.</span><span class="sxs-lookup"><span data-stu-id="6bd6c-108">However, using an **\[out\]** parameter instead of a return value for complex data types is recommended.</span></span> <span data-ttu-id="6bd6c-109">Al devolver tipos de datos complejos, el compilador MIDL generará un código auxiliar del modo/os.</span><span class="sxs-lookup"><span data-stu-id="6bd6c-109">While returning complex data types, the MIDL compiler will generate an /Os mode stub.</span></span> <span data-ttu-id="6bd6c-110">Como resultado, se pierde toda la información de comprobación de errores reciente proporcionada por/Robust.</span><span class="sxs-lookup"><span data-stu-id="6bd6c-110">As a result, all recent error-checking information provided by /robust is lost.</span></span>

<span data-ttu-id="6bd6c-111">Los valores devueltos de función que son tipos de puntero se asignan mediante el código auxiliar de cliente con una llamada a la [ \_ \_ asignación de usuarios de MIDL](/windows/desktop/Midl/midl-user-allocate-1).</span><span class="sxs-lookup"><span data-stu-id="6bd6c-111">Function return values that are pointer types are allocated by the client stub with a call to [midl\_user\_allocate](/windows/desktop/Midl/midl-user-allocate-1).</span></span> <span data-ttu-id="6bd6c-112">En consecuencia, solo se puede aplicar el atributo de puntero único o completo a un tipo de valor devuelto de función de puntero.</span><span class="sxs-lookup"><span data-stu-id="6bd6c-112">Accordingly, only the unique or full pointer attribute can be applied to a pointer function-return type.</span></span>

 

 
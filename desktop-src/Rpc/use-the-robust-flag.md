---
title: Usar la marca/Robust
description: Compile siempre los archivos. idl mediante el modificador/Robust.
ms.assetid: bb2fd026-3ad8-4bb5-b05e-4835b874882f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db395841842331d9297a782fdcd8ea7573139f9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995394"
---
# <a name="use-the-robust-flag"></a><span data-ttu-id="f961b-103">Usar la marca/Robust</span><span class="sxs-lookup"><span data-stu-id="f961b-103">Use the /robust Flag</span></span>

<span data-ttu-id="f961b-104">Compile siempre los archivos. idl mediante el modificador [**/Robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="f961b-104">Always compile .idl files using the [**/robust**](/windows/desktop/Midl/-robust) switch.</span></span> <span data-ttu-id="f961b-105">El uso del modificador **/Robust** genera información adicional que permite que el motor de representación de datos de la red (NDR) realice la comprobación de errores en tiempo de ejecución en argumentos correlacionados en matrices dinámicas, uniones y en punteros de interfaz out en aplicaciones com y RPC.</span><span class="sxs-lookup"><span data-stu-id="f961b-105">Using the **/robust** switch generates additional information that enables the Network Data Representation (NDR) engine to perform run-time error checking on correlated arguments in dynamic arrays, unions, and in out interface pointers in COM and RPC applications.</span></span> <span data-ttu-id="f961b-106">Si el software no se puede compilar con esta marca, el software está tan expuesto a los ataques que ningún esfuerzo en otras áreas pueda proteger.</span><span class="sxs-lookup"><span data-stu-id="f961b-106">If software fails to compile with this flag, the software is so exposed to attacks that no efforts in any other area can protect it.</span></span>

 

 
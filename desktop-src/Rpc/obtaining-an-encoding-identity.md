---
title: Obtener una identidad de codificación
description: Una aplicación que está descodificando datos codificados puede obtener la identidad de la rutina utilizada para codificar los datos, antes de llamar a una rutina para descodificarlo. La rutina MesInqProcEncodingId proporciona esta identidad.
ms.assetid: 53cbd6c5-b267-4ff1-a45b-7e22093f41a5
keywords:
- RPC llamada a procedimiento remoto, tareas, obtener identidad de codificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8591e030913d659fb48034e4c386295773227f7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778607"
---
# <a name="obtaining-an-encoding-identity"></a><span data-ttu-id="0637c-105">Obtener una identidad de codificación</span><span class="sxs-lookup"><span data-stu-id="0637c-105">Obtaining an Encoding Identity</span></span>

<span data-ttu-id="0637c-106">Una aplicación que está descodificando datos codificados puede obtener la identidad de la rutina utilizada para codificar los datos, antes de llamar a una rutina para descodificarlo.</span><span class="sxs-lookup"><span data-stu-id="0637c-106">An application that is decoding encoded data can obtain the identity of the routine used to encode the data, prior to calling a routine to decode it.</span></span> <span data-ttu-id="0637c-107">La rutina [**MesInqProcEncodingId**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid) proporciona esta identidad.</span><span class="sxs-lookup"><span data-stu-id="0637c-107">The [**MesInqProcEncodingId**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid) routine provides this identity.</span></span>

<span data-ttu-id="0637c-108">A cada procedimiento de una interfaz se le asigna un número de identificación entero, denominado *identificador de procedimiento* o *identificador de proceso*, por el compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="0637c-108">Each procedure in an interface is assigned an integer identification number, called a *procedure identifier* or a *proc ID*, by the MIDL compiler.</span></span> <span data-ttu-id="0637c-109">La numeración empieza por cero.</span><span class="sxs-lookup"><span data-stu-id="0637c-109">Numbering begins with zero.</span></span> <span data-ttu-id="0637c-110">Las bibliotecas en tiempo de ejecución de RPC no implican traducir el identificador de procedimiento en una llamada a procedimiento real.</span><span class="sxs-lookup"><span data-stu-id="0637c-110">The RPC run-time libraries are not involved in translating the procedure ID into an actual procedure call.</span></span> <span data-ttu-id="0637c-111">Dado un identificador de procedimiento, la aplicación debe proporcionar un medio para llamar al procedimiento correcto.</span><span class="sxs-lookup"><span data-stu-id="0637c-111">Given a proc ID, your application must provide a means of calling the correct procedure.</span></span> <span data-ttu-id="0637c-112">Normalmente, los desarrolladores de aplicaciones usan una serie de instrucciones **If** o (cuando se usa C/C++) una instrucción **Switch** con este fin.</span><span class="sxs-lookup"><span data-stu-id="0637c-112">Typically, application developers use a series of **if** statements, or (when using C/C++) a **switch** statement for this purpose.</span></span>

 

 





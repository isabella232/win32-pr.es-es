---
title: Atributos ACF de optimización de código auxiliar
description: Estos atributos permiten optimizar el tamaño y la velocidad del código auxiliar.
ms.assetid: 8c98b9ff-d91c-4a17-90c9-298f588e46c5
keywords:
- Los MIDL, atributos y optimización de código auxiliar de ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209490d6064d134a51492afee39c501059879bab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903343"
---
# <a name="stub-optimization-acf-attributes"></a><span data-ttu-id="de33d-104">Atributos ACF de optimización de código auxiliar</span><span class="sxs-lookup"><span data-stu-id="de33d-104">Stub Optimization ACF Attributes</span></span>

<span data-ttu-id="de33d-105">Estos atributos permiten optimizar el tamaño y la velocidad del código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="de33d-105">These attributes enable you to optimize the size and speed of your stub code.</span></span>



| <span data-ttu-id="de33d-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="de33d-106">Attribute</span></span>                                    | <span data-ttu-id="de33d-107">Uso</span><span class="sxs-lookup"><span data-stu-id="de33d-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de33d-108">[**código**](code.md)[**nocode**](nocode.md)</span><span class="sxs-lookup"><span data-stu-id="de33d-108">[**code**](code.md)[**nocode**](nocode.md)</span></span> | <span data-ttu-id="de33d-109">Use los atributos [**code**](code.md) y [**nocode**](nocode.md) juntos para evitar la generación de código auxiliar para las funciones no utilizadas.</span><span class="sxs-lookup"><span data-stu-id="de33d-109">Use the [**code**](code.md) and [**nocode**](nocode.md) attributes together to avoid generating stub code for unused functions.</span></span> <span data-ttu-id="de33d-110">Aplique el atributo **nocode** al encabezado de la interfaz y aplique el atributo **code** a los procedimientos que va a implementar la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="de33d-110">Apply the **nocode** attribute to the interface header, and apply the **code** attribute to those procedures that the client application will implement.</span></span> <span data-ttu-id="de33d-111">El código auxiliar de cliente solo se generará para los procedimientos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="de33d-111">Client stub code will be generated only for the selected procedures.</span></span>                                                                |
| [<span data-ttu-id="de33d-112">**optimiz**</span><span class="sxs-lookup"><span data-stu-id="de33d-112">**optimize**</span></span>](optimize.md)                 | <span data-ttu-id="de33d-113">Permite ajustar el nivel de optimización que realiza el compilador MIDL al generar código auxiliar, especificando que se van a calcular las referencias de los datos mediante el método mixto o el método interpretado.</span><span class="sxs-lookup"><span data-stu-id="de33d-113">Lets you fine-tune the level of optimization that the MIDL compiler performs when generating stub code, by specifying that data is to be marshaled by either the mixed-mode or interpreted method.</span></span> <span data-ttu-id="de33d-114">Puede aplicar el atributo [**Optimize**](optimize.md) a una interfaz o a las funciones seleccionadas dentro de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="de33d-114">You can apply the [**optimize**](optimize.md) attribute to an interface or to selected functions within the interface.</span></span> <span data-ttu-id="de33d-115">En cualquier caso, su uso invalidará las optimizaciones de la línea de comandos y los valores predeterminados que ya existan.</span><span class="sxs-lookup"><span data-stu-id="de33d-115">In either case, its use will override the command-line optimizations and any pre-existing defaults.</span></span> |



 

 

 





---
title: Archivo de configuración de la aplicación (ACF)
description: Puede haber aspectos de la aplicación distribuida que afecten a un componente, pero no tienen nada que hacer con otro.
ms.assetid: 017d93fd-1701-4713-a786-752a7695b5a6
keywords:
- MIDL DE ACF
- Lenguaje de definición de interfaz de Microsoft MIDL, se describe el archivo de configuración de la aplicación
- archivo de configuración de la aplicación MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9066e5641d6b71e68ba670984765661f1b9f6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105651312"
---
# <a name="application-configuration-file-acf"></a><span data-ttu-id="b1013-106">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="b1013-106">Application Configuration File (ACF)</span></span>

<span data-ttu-id="b1013-107">Puede haber aspectos de la aplicación distribuida que afecten a un componente, pero no tienen nada que hacer con otro.</span><span class="sxs-lookup"><span data-stu-id="b1013-107">There may be aspects of your distributed application that affect one component, but have nothing to do with another.</span></span> <span data-ttu-id="b1013-108">Por ejemplo, un objeto puede contener una estructura de datos grande y compleja y pasar el contenido de esta estructura de datos a otro objeto.</span><span class="sxs-lookup"><span data-stu-id="b1013-108">For example, an object may contain a large, complex data structure and pass the contents of this data structure to another object.</span></span> <span data-ttu-id="b1013-109">El diseño exacto de esta estructura de datos puede no tener sentido para la aplicación receptora.</span><span class="sxs-lookup"><span data-stu-id="b1013-109">The exact layout of this data structure may be meaningless to the receiving application.</span></span> <span data-ttu-id="b1013-110">Además, la estructura puede contener tipos de datos que el compilador MIDL no reconoce y no puede generar el cálculo de referencias y el código de serialización.</span><span class="sxs-lookup"><span data-stu-id="b1013-110">Also, the structure may contain data types that the MIDL compiler does not recognize and cannot generate marshaling and unmarshaling code.</span></span>

<span data-ttu-id="b1013-111">Las aplicaciones cliente pueden compartir la misma interfaz pero se ejecutan en distintas plataformas. cada una de ellas puede necesitar su propio conjunto de rutinas de serialización.</span><span class="sxs-lookup"><span data-stu-id="b1013-111">Client applications may share the same interface but run on different platforms; they may each need their own set of marshaling routines.</span></span> <span data-ttu-id="b1013-112">Por último, es posible que los clientes individuales no siempre necesiten el mismo conjunto de funciones.</span><span class="sxs-lookup"><span data-stu-id="b1013-112">Finally, individual clients may not always need the same set of functions.</span></span> <span data-ttu-id="b1013-113">No es eficaz generar código auxiliar para las funciones que nunca se implementarán en una aplicación cliente determinada.</span><span class="sxs-lookup"><span data-stu-id="b1013-113">It is inefficient to generate stub code for functions that will never be implemented in a particular client application.</span></span>

<span data-ttu-id="b1013-114">Al definir estos aspectos locales de la interfaz en un archivo de configuración de la aplicación (ACF), puede separar las diferencias entre las interfaces de cliente de su representación en la red, lo que permite al servidor enviar y recibir datos en un formato coherente, y hacer que el código auxiliar sea más compacto y eficaz.</span><span class="sxs-lookup"><span data-stu-id="b1013-114">By defining these local aspects of your interface in an application configuration file (ACF), you can separate the differences between the client interfaces from their network representation, allowing the server to send and receive data in a consistent format, and making your stub code more compact and efficient.</span></span>

<span data-ttu-id="b1013-115">La estructura y la sintaxis de una definición de interfaz ACF son idénticas a la definición de IDL:</span><span class="sxs-lookup"><span data-stu-id="b1013-115">The structure and syntax of an ACF interface definition are identical to the IDL definition:</span></span>

``` syntax
[ interface-attribute-list] interface interface-name {. . .}
```

<span data-ttu-id="b1013-116">De forma predeterminada, el nombre de la interfaz ACF debe coincidir con su nombre en la definición de IDL.</span><span class="sxs-lookup"><span data-stu-id="b1013-116">By default, the ACF interface name must match its name in the IDL definition.</span></span> <span data-ttu-id="b1013-117">Sin embargo, cuando se usa la opción del compilador de MIDL/ [**ACF**](-acf.md) para especificar explícitamente un nombre de archivo ACF, no es necesario que coincidan los nombres de interfaz.</span><span class="sxs-lookup"><span data-stu-id="b1013-117">However, when you use the MIDL compiler option / [**acf**](-acf.md) to explicitly specify an ACF file name, the interface names do not have to match.</span></span> <span data-ttu-id="b1013-118">Esta característica permite que varias interfaces compartan una especificación ACF única.</span><span class="sxs-lookup"><span data-stu-id="b1013-118">This feature allows several interfaces to share a single ACF specification.</span></span>

 

 





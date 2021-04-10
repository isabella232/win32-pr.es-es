---
title: Códigos en FACILITY_ITF
description: Códigos en facil \_ ITF
ms.assetid: 1f9f7b2c-a4e4-41c0-9ba5-b8bbf722e077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc4375b5956502dbaee97057d347aff1da77e3a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994063"
---
# <a name="codes-in-facility_itf"></a><span data-ttu-id="83996-103">Códigos en facil \_ ITF</span><span class="sxs-lookup"><span data-stu-id="83996-103">Codes in FACILITY\_ITF</span></span>

<span data-ttu-id="83996-104">Los **resultados HRESULT** con recursos como Facility \_ y Facility \_ RPC tienen un significado universal porque se definen en un único origen: Microsoft.</span><span class="sxs-lookup"><span data-stu-id="83996-104">**HRESULT** s with facilities such as FACILITY\_NULL and FACILITY\_RPC have universal meaning because they are defined at a single source: Microsoft.</span></span> <span data-ttu-id="83996-105">Sin embargo, los **HRESULT** s en \_ la utilidad ITF se determinan mediante la función o el método de interfaz desde el que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="83996-105">However, **HRESULT** s in FACILITY\_ITF are determined by the function or interface method from which they are returned.</span></span> <span data-ttu-id="83996-106">Esto significa que el mismo valor de 32 bits en el \_ ITF de instalación devuelto de dos métodos de interfaz diferentes puede tener significados diferentes.</span><span class="sxs-lookup"><span data-stu-id="83996-106">This means that the same 32-bit value in FACILITY\_ITF returned from two different interface methods might have different meanings.</span></span>

<span data-ttu-id="83996-107">La razón por la que los **Valores HRESULT** de la utilidad \_ ITF pueden tener diferentes significados en distintas interfaces es que los **Valores HRESULT** se mantienen en un tamaño de tipo de datos eficaz de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="83996-107">The reason **HRESULT** s in FACILITY\_ITF can have different meanings in different interfaces is that **HRESULT** s are kept to an efficient data type size of 32 bits.</span></span> <span data-ttu-id="83996-108">Desafortunadamente, 32 bits no es lo suficientemente grande como para el desarrollo de un sistema de asignación de códigos de error que evita los códigos en conflicto asignados por diferentes programadores en distintos momentos en distintos lugares (a diferencia del control de identificadores de interfaz y CLSIDs).</span><span class="sxs-lookup"><span data-stu-id="83996-108">Unfortunately, 32 bits is not large enough for the development of an error code allocation system that avoids conflicting codes allocated by different programmers at different times in different places (unlike the handling of interface identifiers and CLSIDs).</span></span> <span data-ttu-id="83996-109">Como resultado, el **HRESULT** de 32 bits está estructurado de modo que Microsoft pueda definir varios códigos de error universales, a la vez que permite que otros programadores definan nuevos códigos de error sin temor de conflicto.</span><span class="sxs-lookup"><span data-stu-id="83996-109">As a result, the 32-bit **HRESULT** is structured such that Microsoft can define several universal error codes, while allowing other programmers to define new error codes without fear of conflict.</span></span> <span data-ttu-id="83996-110">La Convención de código de estado es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="83996-110">The status code convention is as follows:</span></span>

-   <span data-ttu-id="83996-111">Los códigos de estado de los servicios que no sean de \_ ITF solo pueden ser definidos por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="83996-111">Status codes in facilities other than FACILITY\_ITF can be defined only by Microsoft.</span></span>
-   <span data-ttu-id="83996-112">Los códigos de estado de \_ la instalación de ITF se definen únicamente por el desarrollador de la interfaz o función que devuelve el código de estado.</span><span class="sxs-lookup"><span data-stu-id="83996-112">Status codes in facility FACILITY\_ITF are defined solely by the developer of the interface or function that returns the status code.</span></span> <span data-ttu-id="83996-113">Para evitar conflictos de códigos de error, quien define la interfaz es responsable de coordinar y publicar los \_ códigos de estado ITF de las instalaciones asociadas a esa interfaz.</span><span class="sxs-lookup"><span data-stu-id="83996-113">To avoid conflicting error codes, whoever defines the interface is responsible for coordinating and publishing the FACILITY\_ITF status codes associated with that interface.</span></span>

<span data-ttu-id="83996-114">Todos los códigos ITF de la función definida por COM \_ tienen un valor de código en el intervalo de 0x0000-0x01FF.</span><span class="sxs-lookup"><span data-stu-id="83996-114">All the COM-defined FACILITY\_ITF codes have a code value in the range of 0x0000-0x01FF.</span></span> <span data-ttu-id="83996-115">Aunque es legal usar cualquier código en \_ la ITF de servicio, se recomienda usar solo los valores de código en el intervalo de 0x0200-0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="83996-115">While it is legal to use any codes in FACILITY\_ITF, it is recommended that only code values in the range of 0x0200-0xFFFF be used.</span></span> <span data-ttu-id="83996-116">Esta recomendación se realiza como un medio para reducir la confusión con los errores definidos por COM.</span><span class="sxs-lookup"><span data-stu-id="83996-116">This recommendation is made as a means of reducing confusion with any COM-defined errors.</span></span>

<span data-ttu-id="83996-117">También se recomienda que los desarrolladores definan nuevas funciones e interfaces para devolver los códigos de error, tal y como se definen en COM y en otros medios distintos de la instalación de \_ ITF.</span><span class="sxs-lookup"><span data-stu-id="83996-117">It is also recommended that developers define new functions and interfaces to return error codes as defined by COM and in facilities other than FACILITY\_ITF.</span></span> <span data-ttu-id="83996-118">En concreto, las interfaces que tienen la posibilidad de ser remotas con RPC en el futuro deben definir los códigos de RPC de los servicios \_ como válidos.</span><span class="sxs-lookup"><span data-stu-id="83996-118">In particular, interfaces that have any chance of being remoted using RPC in the future should define the FACILITY\_RPC codes as legal.</span></span> <span data-ttu-id="83996-119">E \_ inesperado es un código de error específico que la mayoría de los desarrolladores querrán convertir en universalmente legal.</span><span class="sxs-lookup"><span data-stu-id="83996-119">E\_UNEXPECTED is a specific error code that most developers will want to make universally legal.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83996-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="83996-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83996-121">Control de errores en COM</span><span class="sxs-lookup"><span data-stu-id="83996-121">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

 





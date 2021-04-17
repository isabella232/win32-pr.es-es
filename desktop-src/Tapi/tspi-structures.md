---
description: Las estructuras de datos que usa TSPI son idénticas a las definidas en estructuras TAPI, con la excepción de TUISPICREATEDIALOGINSTANCEPARAMS.
ms.assetid: 99d966ea-49b5-4a84-83a1-99dc8465c751
title: Estructuras TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e3468171bc160ca03ac9f5501a9eba7fd9221ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687484"
---
# <a name="tspi-structures"></a><span data-ttu-id="47fe8-103">Estructuras TSPI</span><span class="sxs-lookup"><span data-stu-id="47fe8-103">TSPI Structures</span></span>

<span data-ttu-id="47fe8-104">Las estructuras de datos que usa TSPI son idénticas a las definidas en [estructuras TAPI](./tapi-structures.md), con la excepción de [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams).</span><span class="sxs-lookup"><span data-stu-id="47fe8-104">The data structures TSPI uses are identical to those defined in [TAPI Structures](./tapi-structures.md), with the exception of [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams).</span></span>

<span data-ttu-id="47fe8-105">En el caso de la mayoría de las estructuras de datos más grandes, la responsabilidad de rellenar los miembros se divide entre el proveedor de servicios y TAPI.</span><span class="sxs-lookup"><span data-stu-id="47fe8-105">In the case of most of the larger data structures, the responsibility for filling in members is divided between the service provider and TAPI.</span></span> <span data-ttu-id="47fe8-106">El proveedor de servicios debe conservar los valores presentes en los miembros que pertenecen a TAPI.</span><span class="sxs-lookup"><span data-stu-id="47fe8-106">The service provider must preserve the values present in members owned by TAPI.</span></span> <span data-ttu-id="47fe8-107">La descripción de los miembros que debe establecer el proveedor de servicios y que debe conservarse se proporciona en la sección funciones de las funciones que hacen referencia a esa estructura de datos.</span><span class="sxs-lookup"><span data-stu-id="47fe8-107">The description of which members must be set by the service provider and which must be preserved is provided in the Functions section in the functions that refer to that data structure.</span></span>

<span data-ttu-id="47fe8-108">Para cada estructura, en la sección de referencia se enumeran los elementos siguientes:</span><span class="sxs-lookup"><span data-stu-id="47fe8-108">For each structure, the reference section lists the following items:</span></span>

-   <span data-ttu-id="47fe8-109">El propósito de la estructura</span><span class="sxs-lookup"><span data-stu-id="47fe8-109">The purpose of the structure</span></span>
-   <span data-ttu-id="47fe8-110">Una descripción de los valores o campos</span><span class="sxs-lookup"><span data-stu-id="47fe8-110">A description of the values or fields</span></span>
-   <span data-ttu-id="47fe8-111">Descripción de la extensibilidad de la estructura.</span><span class="sxs-lookup"><span data-stu-id="47fe8-111">A description of the structure's extensibility</span></span>
-   <span data-ttu-id="47fe8-112">Comentarios opcionales sobre el uso de la estructura</span><span class="sxs-lookup"><span data-stu-id="47fe8-112">Optional comments about using the structure</span></span>
-   <span data-ttu-id="47fe8-113">Referencias opcionales a otras funciones, mensajes, constantes o estructuras.</span><span class="sxs-lookup"><span data-stu-id="47fe8-113">Optional references to other functions, messages, constants, or structures.</span></span>

<span data-ttu-id="47fe8-114">La memoria de todas las estructuras de datos cuya representación se publica y comparte con TAPI y el proveedor de servicios se asigna mediante TAPI o una aplicación que utiliza TAPI.</span><span class="sxs-lookup"><span data-stu-id="47fe8-114">Memory for all data structures whose representation is published and shared by both TAPI and the service provider is allocated by TAPI or an application using TAPI.</span></span> <span data-ttu-id="47fe8-115">TAPI pasa un puntero a la función TSPI que devuelve la información.</span><span class="sxs-lookup"><span data-stu-id="47fe8-115">TAPI passes a pointer to the TSPI function that returns the information.</span></span> <span data-ttu-id="47fe8-116">TSPI rellena la estructura de datos con la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="47fe8-116">TSPI fills the data structure with the requested information.</span></span> <span data-ttu-id="47fe8-117">Si la operación es asincrónica, la información no estará disponible hasta que la devolución de llamada de respuesta asincrónica indique Success.</span><span class="sxs-lookup"><span data-stu-id="47fe8-117">If the operation is asynchronous, the information is not available until the asynchronous reply callback indicates success.</span></span>

> [!Note]  
> <span data-ttu-id="47fe8-118">Algunas estructuras incluyen campos de tamaño y desplazamiento para definir la ubicación y la longitud de las cadenas en la parte variable de la estructura.</span><span class="sxs-lookup"><span data-stu-id="47fe8-118">Some structures include Size and Offset fields for defining the location and length of strings in the variable portion of the structure.</span></span> <span data-ttu-id="47fe8-119">Si se solicita al proveedor de servicios que agregue una cadena pero no hay ninguna cadena disponible, el proveedor de servicios debe indicar esta condición de una de estas maneras:</span><span class="sxs-lookup"><span data-stu-id="47fe8-119">If the service provider is requested to add a string but no string is available, the service provider must indicate this condition in one of these ways:</span></span>
>
> -   <span data-ttu-id="47fe8-120">Establezca los campos tamaño y desplazamiento en 0.</span><span class="sxs-lookup"><span data-stu-id="47fe8-120">Set both the Size and Offset fields to 0.</span></span>
> -   <span data-ttu-id="47fe8-121">Establezca el campo desplazamiento en distinto de cero, pero el tamaño en 0.</span><span class="sxs-lookup"><span data-stu-id="47fe8-121">Set the Offset field to nonzero but Size to 0.</span></span>
> -   <span data-ttu-id="47fe8-122">Establezca el campo desplazamiento en distinto de cero, el tamaño en 1 y el byte en el desplazamiento en 0.</span><span class="sxs-lookup"><span data-stu-id="47fe8-122">Set the Offset field to nonzero, Size to 1, and the byte at the Offset to 0.</span></span>

 

 

 

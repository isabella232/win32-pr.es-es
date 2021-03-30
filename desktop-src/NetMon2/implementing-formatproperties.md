---
description: Monitor de red llama a la función FormatProperties para dar formato a los datos que se muestran en el panel de detalles de la interfaz de usuario de Monitor de red.
ms.assetid: d0a58e1d-c867-4277-916e-f408627b5269
title: Implementación de FormatProperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 660b581bf29fd8e5d40af65f5ff90e1e9223ad2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154144"
---
# <a name="implementing-formatproperties"></a><span data-ttu-id="c93c3-103">Implementación de FormatProperties</span><span class="sxs-lookup"><span data-stu-id="c93c3-103">Implementing FormatProperties</span></span>

<span data-ttu-id="c93c3-104">Monitor de red llama a la función [**FormatProperties**](formatproperties.md) para dar formato a los datos que se muestran en el panel de detalles de la interfaz de usuario de monitor de red.</span><span class="sxs-lookup"><span data-stu-id="c93c3-104">Network Monitor calls the [**FormatProperties**](formatproperties.md) function to format the data that is displayed in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="c93c3-105">Normalmente, se llama a **FormatProperties** para dar formato a la línea de Resumen de un protocolo y, a continuación, para dar formato a todas las instancias de propiedad del protocolo dentro de un marco.</span><span class="sxs-lookup"><span data-stu-id="c93c3-105">Typically, **FormatProperties** is called to format the summary line for a protocol, and then to format all the property instances of the protocol within a frame.</span></span> <span data-ttu-id="c93c3-106">Sin embargo, Monitor de red no identifica el número de veces que se llama a **FormatProperties** para un analizador específico.</span><span class="sxs-lookup"><span data-stu-id="c93c3-106">However, Network Monitor does not identify the number of times that **FormatProperties** is called for a specific parser.</span></span>

<span data-ttu-id="c93c3-107">Al llamar a [**FormatProperties**](formatproperties.md), monitor de red proporciona una estructura [**PROPERTYINST**](propertyinst.md) para cada propiedad que muestra.</span><span class="sxs-lookup"><span data-stu-id="c93c3-107">When calling [**FormatProperties**](formatproperties.md), Network Monitor provides a [**PROPERTYINST**](propertyinst.md) structure for each property that it displays.</span></span> <span data-ttu-id="c93c3-108">La estructura **PROPERTYINST** proporciona información sobre los datos que se van a mostrar, incluido un puntero a la estructura [**PROPERTYINFO**](propertyinfo.md) que especifica la función que se va a utilizar para dar formato a la propiedad de datos mostrada.</span><span class="sxs-lookup"><span data-stu-id="c93c3-108">The **PROPERTYINST** structure provides information about the data to be displayed, including a pointer to the [**PROPERTYINFO**](propertyinfo.md) structure that specifies the function to use to format the displayed data property.</span></span>

> [!Note]  
> <span data-ttu-id="c93c3-109">Cuando se agrega una propiedad a la base de datos de [*propiedades*](p.md) del analizador, se especifica una estructura [**PROPERTYINFO**](propertyinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="c93c3-109">A [**PROPERTYINFO**](propertyinfo.md) structure is specified when adding a property to the [*property database*](p.md) of the parser.</span></span>

 

<span data-ttu-id="c93c3-110">Monitor de red identifica la función de formato que se va a llamar para cada instancia de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c93c3-110">Network Monitor identifies the format function to call for each property instance.</span></span> <span data-ttu-id="c93c3-111">El miembro **InstanceData** de la estructura [**PROPERTYINFO**](propertyinfo.md) puede especificar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c93c3-111">The **InstanceData** member of the [**PROPERTYINFO**](propertyinfo.md) structure can specify the following:</span></span>

-   <span data-ttu-id="c93c3-112">La función [**FormatPropertyInstance**](formatpropertyinstance.md) para usar el [*formateador genérico*](g.md) que proporciona monitor de red.</span><span class="sxs-lookup"><span data-stu-id="c93c3-112">The [**FormatPropertyInstance**](formatpropertyinstance.md) function to use the [*generic formatter*](g.md) that Network Monitor provides.</span></span>

    <span data-ttu-id="c93c3-113">-O bien-</span><span class="sxs-lookup"><span data-stu-id="c93c3-113">– or –</span></span>

-   <span data-ttu-id="c93c3-114">Nombre de una función de formato personalizado que proporciona el analizador.</span><span class="sxs-lookup"><span data-stu-id="c93c3-114">The name of a custom format function that the parser provides.</span></span>

<span data-ttu-id="c93c3-115">Las funciones de formato personalizado y [**FormatPropertyInstance**](formatpropertyinstance.md) devuelven los datos con formato que se muestran en el panel de detalles de la interfaz de usuario de monitor de red.</span><span class="sxs-lookup"><span data-stu-id="c93c3-115">The [**FormatPropertyInstance**](formatpropertyinstance.md) and the custom format functions return the formatted data that is displayed in the details pane of the Network Monitor UI.</span></span>

<span data-ttu-id="c93c3-116">En la ilustración siguiente se muestra cómo Monitor de red identifica la función a la que se va a llamar para cada instancia de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c93c3-116">The following illustration shows how Network Monitor identifies the function to call for each property instance.</span></span>

![Cómo identifica el monitor de red la función a la que se va a llamar](images/formatprop1.png)

<span data-ttu-id="c93c3-118">En el procedimiento siguiente se identifican los pasos necesarios para implementar [**FormatProperties**](formatproperties.md).</span><span class="sxs-lookup"><span data-stu-id="c93c3-118">The following procedure identifies the steps necessary to implement [**FormatProperties**](formatproperties.md).</span></span>

<span data-ttu-id="c93c3-119">**Para implementar FormatProperties**</span><span class="sxs-lookup"><span data-stu-id="c93c3-119">**To implement FormatProperties**</span></span>

-   <span data-ttu-id="c93c3-120">Con una estructura de bucle, llame a la función Format para cada estructura [**PROPERTYINST**](propertyinst.md) que se pasa al analizador en el parámetro *lpPropInst* de la función [**FormatProperties**](formatproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="c93c3-120">Using a loop structure, call the format function for each [**PROPERTYINST**](propertyinst.md) structure that is passed to the parser in the *lpPropInst* parameter of the [**FormatProperties**](formatproperties.md) function.</span></span>

<span data-ttu-id="c93c3-121">La siguiente es una implementación básica de [**FormatProperties**](formatproperties.md).</span><span class="sxs-lookup"><span data-stu-id="c93c3-121">The following is a basic implementation of [**FormatProperties**](formatproperties.md).</span></span>

``` syntax
#include <windows.h>

DWORD BHAPI MyProtocolFormatProperties( HFRAME hFrame,
                                        LPBYTE         pMacFrame,
                                        LPBYTE         pBLRPLATEFrame,
                                        DWORD          nPropertyInsts
                                        LPPROPERTYINST  p)
  {
    while( nPropertyInsts-- > 0)
      {
         ( (FORMAT) p->lpPropertyInfo->InstanceData) ) (p);
         p++;
      }
  return BHERR_SUCCESS;
  }
```

 

 




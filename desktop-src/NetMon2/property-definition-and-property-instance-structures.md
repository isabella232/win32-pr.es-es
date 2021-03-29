---
description: Monitor de red proporciona una estructura PROPERTYINFO para definir las propiedades de un protocolo, y una estructura PROPERTYINST y PROPERTYINSTEX para definir una instancia de una propiedad.
ms.assetid: d1e29bd6-c04a-48f1-9727-96b9450e256f
title: Definición de propiedad y estructuras de instancia de propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55aa67efb5054d93184b56c53f84f9fac0893abf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813309"
---
# <a name="property-definition-and-property-instance-structures"></a><span data-ttu-id="86524-103">Definición de propiedad y estructuras de instancia de propiedad</span><span class="sxs-lookup"><span data-stu-id="86524-103">Property Definition and Property Instance Structures</span></span>

<span data-ttu-id="86524-104">Monitor de red proporciona una estructura [**PROPERTYINFO**](propertyinfo.md) para definir las propiedades de un protocolo, y una estructura [**PROPERTYINST**](propertyinst.md)y [**PROPERTYINSTEX**](propertyinstex.md) para definir una instancia de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="86524-104">Network Monitor provides a [**PROPERTYINFO**](propertyinfo.md) structure to define the properties of a protocol, and a [**PROPERTYINST**](propertyinst.md), and [**PROPERTYINSTEX**](propertyinstex.md) structure to define an instance of a property.</span></span>

![estructuras de monitor de red](images/property1.png)

<span data-ttu-id="86524-106">El analizador asigna y rellena la estructura [**PROPERTYINFO**](propertyinfo.md) para todas las propiedades que admite un protocolo.</span><span class="sxs-lookup"><span data-stu-id="86524-106">The parser allocates and fills-in the [**PROPERTYINFO**](propertyinfo.md) structure for all the properties that a protocol supports.</span></span> <span data-ttu-id="86524-107">El analizador pasa la estructura a Monitor de red donde se agrega la estructura a la [*base de datos de propiedades*](p.md)de protocolo.</span><span class="sxs-lookup"><span data-stu-id="86524-107">The parser passes the structure to Network Monitor where the structure is added to the protocol [*property database*](p.md).</span></span> <span data-ttu-id="86524-108">La información de la estructura **PROPERTYINFO** se utiliza al analizar una instancia de una propiedad y al dar formato a los datos que se muestran en la interfaz de usuario de monitor de red.</span><span class="sxs-lookup"><span data-stu-id="86524-108">The information in the **PROPERTYINFO** structure is used when parsing an instance of a property, and when formatting the data that is displayed in the Network Monitor UI.</span></span>

<span data-ttu-id="86524-109">Monitor de red asigna las estructuras [**PROPERTYINST**](propertyinst.md) y [**PROPERTYINSTEX**](propertyinstex.md) cuando el analizador adjunta una definición de propiedad a una instancia de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="86524-109">Network Monitor allocates the [**PROPERTYINST**](propertyinst.md) and [**PROPERTYINSTEX**](propertyinstex.md) structures when the parser attaches a property definition to an instance of a property.</span></span>

<span data-ttu-id="86524-110">En el procedimiento siguiente se identifican los pasos necesarios para adjuntar una definición de propiedad.</span><span class="sxs-lookup"><span data-stu-id="86524-110">The following procedure identifies the steps necessary to attach a property definition.</span></span>

<span data-ttu-id="86524-111">**Para adjuntar una definición de propiedad**</span><span class="sxs-lookup"><span data-stu-id="86524-111">**To attach a property definition**</span></span>

1.  <span data-ttu-id="86524-112">Identifique cada propiedad que exista en una instancia del protocolo.</span><span class="sxs-lookup"><span data-stu-id="86524-112">Identify each property that exists in an instance of the protocol.</span></span> <span data-ttu-id="86524-113">Al adjuntar una definición, Monitor de red pasa los datos capturados al analizador.</span><span class="sxs-lookup"><span data-stu-id="86524-113">When attaching a definition, Network Monitor passes the captured data to the parser.</span></span> <span data-ttu-id="86524-114">Los datos se pasan en función de una instancia del protocolo.</span><span class="sxs-lookup"><span data-stu-id="86524-114">The data is passed on a protocol instance basis.</span></span>
2.  <span data-ttu-id="86524-115">Determine la ubicación de la propiedad en la instancia del protocolo.</span><span class="sxs-lookup"><span data-stu-id="86524-115">Determine the location of the property in the protocol instance.</span></span>
3.  <span data-ttu-id="86524-116">Adjunte una definición de propiedad a la ubicación de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="86524-116">Attach a property definition to the property location.</span></span>

<span data-ttu-id="86524-117">Monitor de red implementa una estructura [**PROPERTYINST**](propertyinst.md) cuando el analizador utiliza los datos de propiedad tal como existen en la captura.</span><span class="sxs-lookup"><span data-stu-id="86524-117">Network Monitor implements a [**PROPERTYINST**](propertyinst.md) structure when the parser uses the property data as it exists in the capture.</span></span> <span data-ttu-id="86524-118">Monitor de red implementa una estructura [**PROPERTYINSTEX**](propertyinstex.md) cuando el analizador debe modificar los datos de la propiedad en la captura.</span><span class="sxs-lookup"><span data-stu-id="86524-118">Network Monitor implements a [**PROPERTYINSTEX**](propertyinstex.md) structure when the parser must modify the property data in the capture.</span></span>

 

 




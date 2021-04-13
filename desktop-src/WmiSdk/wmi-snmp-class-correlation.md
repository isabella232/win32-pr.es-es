---
description: La correlación afecta al conjunto de clases devueltas desde SMIR.
ms.assetid: 799a0866-e7a0-492f-956e-b13bf591babe
ms.tgt_platform: multiple
title: Correlación de clases SNMP de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc0ca4740c90563fce05e1b6352ef33b0e3ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276248"
---
# <a name="wmi-snmp-class-correlation"></a><span data-ttu-id="17c1a-103">Correlación de clases SNMP de WMI</span><span class="sxs-lookup"><span data-stu-id="17c1a-103">WMI SNMP Class Correlation</span></span>

<span data-ttu-id="17c1a-104">La correlación afecta al conjunto de clases devueltas desde SMIR.</span><span class="sxs-lookup"><span data-stu-id="17c1a-104">Correlation affects the set of classes returned from the SMIR.</span></span> <span data-ttu-id="17c1a-105">Las clases correlacionadas son aquellas que se sabe que admite un dispositivo SNMP determinado en el momento en que se produce la enumeración.</span><span class="sxs-lookup"><span data-stu-id="17c1a-105">Correlated classes are those that a given SNMP device is known to support at the time enumeration occurs.</span></span> <span data-ttu-id="17c1a-106">La enumeración no correlacionada devuelve todas las clases presentes en el SMIR, independientemente de si el dispositivo las admite.</span><span class="sxs-lookup"><span data-stu-id="17c1a-106">Noncorrelated enumeration returns all classes present within the SMIR, regardless of whether the device supports them.</span></span> <span data-ttu-id="17c1a-107">La correlación es una característica del proveedor SNMP de WMI y se puede desactivar o activar (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="17c1a-107">Correlation is a feature of the WMI SNMP provider and can be turned off or on (default).</span></span>

> [!Note]  
> <span data-ttu-id="17c1a-108">Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="17c1a-108">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="17c1a-109">La correlación podría impedir ver todas las clases que realmente admite un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="17c1a-109">Correlation might prevent you from seeing all of the classes that are actually supported by a device.</span></span> <span data-ttu-id="17c1a-110">Si sabe que se admite una clase determinada, pero no aparece en SMIR, esto podría deberse a varios motivos, uno de los cuales es una correlación.</span><span class="sxs-lookup"><span data-stu-id="17c1a-110">If you know that a particular class is supported but it does not appear in the SMIR, this could be due to several reasons, one of which is correlation.</span></span> <span data-ttu-id="17c1a-111">Considere la posibilidad de desactivar la correlación antes de escribir en el dispositivo en cuestión.</span><span class="sxs-lookup"><span data-stu-id="17c1a-111">Consider turning correlation off before writing to the device in question.</span></span> <span data-ttu-id="17c1a-112">Sin embargo, si se desactiva la correlación, se produce la probabilidad de que muchas clases no admitidas por el dispositivo aparezcan en SMIR.</span><span class="sxs-lookup"><span data-stu-id="17c1a-112">However, turning correlation off results in the likelihood that many classes not supported by the device will appear in the SMIR.</span></span> <span data-ttu-id="17c1a-113">Además, existe un costo de rendimiento al usar la correlación porque el dispositivo se consulta para ver qué clases admite.</span><span class="sxs-lookup"><span data-stu-id="17c1a-113">Also, there is a performance cost in using correlation because the device is queried to see what classes it supports.</span></span> <span data-ttu-id="17c1a-114">Cuando se activa la correlación, el proveedor SNMP produce una enumeración de clases admitidas por el dispositivo similar al resultado de ejecutar una herramienta de *recorrido de MIB* .</span><span class="sxs-lookup"><span data-stu-id="17c1a-114">When correlation is turned on, the SNMP provider causes an enumeration of device-supported classes similar to the result of running a *mib walk* tool.</span></span>

<span data-ttu-id="17c1a-115">Por ejemplo, un administrador de red desea conocer varias partes clave de los datos de todos los concentradores administrados en una red determinada.</span><span class="sxs-lookup"><span data-stu-id="17c1a-115">For example, a network manager wants to know several key pieces of data about all the managed hubs in a particular network.</span></span> <span data-ttu-id="17c1a-116">Ya existe una base de datos de los dispositivos actuales y sus MIB compatibles, por lo que no es necesario depender de la función de correlación del dispositivo para proporcionar los elementos de datos admitidos.</span><span class="sxs-lookup"><span data-stu-id="17c1a-116">A database of the current devices and their supported MIBs already exists, so there is no need to rely on the correlation function of the device to provide the supported data elements.</span></span> <span data-ttu-id="17c1a-117">En este caso, la correlación podría desactivarse.</span><span class="sxs-lookup"><span data-stu-id="17c1a-117">In this case, correlation could be turned off.</span></span>

<span data-ttu-id="17c1a-118">En el ejemplo siguiente se muestra cómo desactivar la correlación.</span><span class="sxs-lookup"><span data-stu-id="17c1a-118">The following example shows how to turn off correlation.</span></span>


```VB
set objNamedValueSet = CreateObject( _
    "WbemScripting.SWbemNamedValueSet") 
objNamedValueSet.Add "Correlate", FALSE, 0
```



<span data-ttu-id="17c1a-119">Por otro lado, es posible que otro administrador de red desee supervisar todas las unidades de disco de la máquina UNIX en la red, pero no está familiarizado con los datos de la MIB de esas máquinas.</span><span class="sxs-lookup"><span data-stu-id="17c1a-119">On the other hand, another network manager may want to monitor all the UNIX machine disk drives on the network but is unfamiliar with the MIB data on those machines.</span></span> <span data-ttu-id="17c1a-120">En ese caso, se activaría la correlación.</span><span class="sxs-lookup"><span data-stu-id="17c1a-120">In that case, correlation would be turned on.</span></span>

 

 




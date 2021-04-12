---
description: El proveedor SNMP usa los siguientes calificadores de clase CIM al asignar definiciones de objeto MIB a definiciones de clase CIM.
ms.assetid: 458167dc-562e-47b8-8760-797ae13f9459
ms.tgt_platform: multiple
title: Calificadores de clase CIM para objetos MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60fe97debc7fd81b48a6daf0f5a955374546458
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278553"
---
# <a name="cim-class-qualifiers-for-mib-objects"></a><span data-ttu-id="abcd4-103">Calificadores de clase CIM para objetos MIB</span><span class="sxs-lookup"><span data-stu-id="abcd4-103">CIM Class Qualifiers for MIB Objects</span></span>

<span data-ttu-id="abcd4-104">El proveedor SNMP usa los siguientes calificadores de clase CIM al asignar definiciones de objeto MIB a definiciones de clase CIM.</span><span class="sxs-lookup"><span data-stu-id="abcd4-104">The SNMP Provider uses the following CIM class qualifiers when mapping MIB object definitions to CIM class definitions.</span></span> <span data-ttu-id="abcd4-105">Un calificador obligatorio debe estar presente para que el proveedor SNMP resuelva por completo un objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="abcd4-105">A mandatory qualifier must be present for the SNMP Provider to fully resolve a group object.</span></span> <span data-ttu-id="abcd4-106">Si no se define un calificador obligatorio, se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="abcd4-106">Failure to define a mandatory qualifier returns an error.</span></span> <span data-ttu-id="abcd4-107">Especificar un valor de calificador no válido también devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="abcd4-107">Specifying an illegal qualifier value also returns an error.</span></span>

> [!Note]  
> <span data-ttu-id="abcd4-108">Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="abcd4-108">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 



| <span data-ttu-id="abcd4-109">Qualifier</span><span class="sxs-lookup"><span data-stu-id="abcd4-109">Qualifier</span></span>           | <span data-ttu-id="abcd4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="abcd4-110">Description</span></span>                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abcd4-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="abcd4-111">**Description**</span></span>     | <span data-ttu-id="abcd4-112">**cadena** Opta</span><span class="sxs-lookup"><span data-stu-id="abcd4-112">**string** Optional</span></span><br/> <span data-ttu-id="abcd4-113">Descripción de la clase.</span><span class="sxs-lookup"><span data-stu-id="abcd4-113">Description of the class.</span></span><br/>                                                                      |
| <span data-ttu-id="abcd4-114">**ObjectId de grupo \_**</span><span class="sxs-lookup"><span data-stu-id="abcd4-114">**Group\_Objectid**</span></span> | <span data-ttu-id="abcd4-115">**cadena** Obligatorio, si la clase es para el proveedor de clase SNMP.</span><span class="sxs-lookup"><span data-stu-id="abcd4-115">**string** Mandatory, if the class is for the SNMP class provider.</span></span><br/> <span data-ttu-id="abcd4-116">Identificador de objeto de la colección fabricada.</span><span class="sxs-lookup"><span data-stu-id="abcd4-116">Object identifier of the fabricated collection.</span></span><br/> |
| <span data-ttu-id="abcd4-117">**\_Importaciones de módulos**</span><span class="sxs-lookup"><span data-stu-id="abcd4-117">**Module\_Imports**</span></span> | <span data-ttu-id="abcd4-118">**cadena** Opta</span><span class="sxs-lookup"><span data-stu-id="abcd4-118">**string** Optional</span></span><br/> <span data-ttu-id="abcd4-119">Lista separada por comas de nombres de módulos MIB utilizados para resolver importaciones.</span><span class="sxs-lookup"><span data-stu-id="abcd4-119">Comma-separated list of MIB module names used to resolve imports.</span></span><br/>                              |
| <span data-ttu-id="abcd4-120">**Nombre del módulo \_**</span><span class="sxs-lookup"><span data-stu-id="abcd4-120">**Module\_Name**</span></span>    | <span data-ttu-id="abcd4-121">**cadena** Opta</span><span class="sxs-lookup"><span data-stu-id="abcd4-121">**string** Optional</span></span><br/> <span data-ttu-id="abcd4-122">Nombre de identidad de un módulo MIB.</span><span class="sxs-lookup"><span data-stu-id="abcd4-122">Identity name of a MIB module.</span></span><br/>                                                                 |
| <span data-ttu-id="abcd4-123">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="abcd4-123">**Reference**</span></span>       | <span data-ttu-id="abcd4-124">**cadena** Opta</span><span class="sxs-lookup"><span data-stu-id="abcd4-124">**string** Optional</span></span><br/> <span data-ttu-id="abcd4-125">Hace referencia a otro documento que contiene más información sobre la clase.</span><span class="sxs-lookup"><span data-stu-id="abcd4-125">Refers to another document that contains more information about the class.</span></span><br/>                     |
| <span data-ttu-id="abcd4-126">**Simple**</span><span class="sxs-lookup"><span data-stu-id="abcd4-126">**Singleton**</span></span>       | <span data-ttu-id="abcd4-127">**Booleano** Obligatorio para las clases asignadas desde colecciones escalares.</span><span class="sxs-lookup"><span data-stu-id="abcd4-127">**Bool** Mandatory for classes mapped from scalar collections.</span></span><br/> <span data-ttu-id="abcd4-128">Indica una clase que solo puede tener una instancia.</span><span class="sxs-lookup"><span data-stu-id="abcd4-128">Indicates a class that can only have one instance.</span></span><br/>  |



 

 

 





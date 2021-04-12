---
title: Componente de proveedor de ejemplo ADSI
description: Active Directory los escritores de proveedores de interfaces de servicio encontrarán esta sección de especial interés, ya que describe el componente de proveedor de ejemplo ADSI en profundidad.
ms.assetid: 1ca73817-7a21-4a39-b496-fc82db26ea4e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7bf960021df9a3b26f252584cad2ff3374254a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356716"
---
# <a name="adsi-example-provider-component"></a><span data-ttu-id="419fc-103">Componente de proveedor de ejemplo ADSI</span><span class="sxs-lookup"><span data-stu-id="419fc-103">ADSI Example Provider Component</span></span>

<span data-ttu-id="419fc-104">Active Directory los escritores de proveedores de interfaces de servicio encontrarán esta sección de especial interés, ya que describe el componente de proveedor de ejemplo ADSI en profundidad.</span><span class="sxs-lookup"><span data-stu-id="419fc-104">Active Directory Service Interfaces provider writers will find this section of particular interest, because it describes the ADSI example provider component in depth.</span></span> <span data-ttu-id="419fc-105">Los escritores de proveedores ADSI pueden instalar el proveedor de ejemplo y usar el marco de código como base para crear su propia implementación.</span><span class="sxs-lookup"><span data-stu-id="419fc-105">ADSI provider writers can install the example provider and use the code framework as a basis to create their own implementation.</span></span> <span data-ttu-id="419fc-106">Se tratan los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="419fc-106">The following topics are discussed:</span></span>

<span data-ttu-id="419fc-107">[La instalación del componente de proveedor de ejemplo](installing-the-example-provider-component.md) describe cómo instalar el proveedor de ejemplo ADSI y su directorio ficticio.</span><span class="sxs-lookup"><span data-stu-id="419fc-107">[Installing the Example Provider Component](installing-the-example-provider-component.md) describes how to install the ADSI sample provider and its mock directory.</span></span> <span data-ttu-id="419fc-108">En esta sección se incluye una lista de los valores del registro.</span><span class="sxs-lookup"><span data-stu-id="419fc-108">This section includes a list of the registry settings.</span></span>

<span data-ttu-id="419fc-109">[Definición de directorio](directory-definition.md) describe las entradas de directorio definidas por el componente de proveedor de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="419fc-109">[Directory Definition](directory-definition.md) describes the directory entries defined by the example provider component.</span></span>

<span data-ttu-id="419fc-110">La [Administración de esquemas](schema-management.md) describe cómo cada elemento del servicio de directorio del componente de proveedor de ejemplo se puede representar mediante un tipo específico de Active Directory objeto.</span><span class="sxs-lookup"><span data-stu-id="419fc-110">[Schema Management](schema-management.md) describes how each element in the example provider component directory service can be represented by a specific type of Active Directory object.</span></span>

<span data-ttu-id="419fc-111">[Enlazar a un objeto de Active Directory](binding-to-an-active-directory-object.md) describe cómo, dada una cadena ADsPath, el componente proveedor de ejemplo identifica ese elemento, crea el tipo adecuado de Active Directory objeto para él y recupera el tipo de puntero de interfaz solicitado en ese objeto para devolverlo al software cliente de ADS.</span><span class="sxs-lookup"><span data-stu-id="419fc-111">[Binding to an Active Directory Object](binding-to-an-active-directory-object.md) describes how, given an ADsPath string, the example provider component identifies that element, creates the appropriate type of Active Directory object for it, and retrieves the requested type of interface pointer on that object to pass back to the ADs client software.</span></span>

<span data-ttu-id="419fc-112">[Objetos de enumerador](enumerator-objects.md) muestra los tipos de enumeraciones específicos proporcionados por el componente de proveedor de ejemplo y en qué código fuente se pueden encontrar las implementaciones.</span><span class="sxs-lookup"><span data-stu-id="419fc-112">[Enumerator Objects](enumerator-objects.md) lists the specific types of enumerations supplied by the example provider component and in which source code the implementations can be found.</span></span>

<span data-ttu-id="419fc-113">[Información general de código](code-overview.md) proporciona una descripción de nivel de tarea de cada parte del componente de proveedor de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="419fc-113">[Code Overview](code-overview.md) provides a task-level description of each part of the example provider component.</span></span>

<span data-ttu-id="419fc-114">[Detalles de código](code-details.md) enumera los módulos de software y su contenido.</span><span class="sxs-lookup"><span data-stu-id="419fc-114">[Code Details](code-details.md) lists the software modules and their contents.</span></span>

 

 





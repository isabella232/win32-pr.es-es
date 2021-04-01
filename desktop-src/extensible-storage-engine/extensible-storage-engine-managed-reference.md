---
description: 'Más información sobre: referencia administrada del motor de almacenamiento extensible'
title: Referencia administrada del motor de almacenamiento extensible
TOCTitle: Extensible Storage Engine Managed Reference
ms:assetid: b6dc69d0-82be-478d-b47f-37d7569cd200
ms:mtpsurl: https://msdn.microsoft.com/library/Dn375980(v=EXCHG.10)
ms:contentKeyID: 56355772
ms.date: 09/02/2015
ms.topic: article
ms.openlocfilehash: a1323d662cc7252ff6bda1eda53108751d3aedfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082306"
---
# <a name="extensible-storage-engine-managed-reference"></a><span data-ttu-id="77d7f-103">Referencia administrada del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="77d7f-103">Extensible Storage Engine Managed Reference</span></span>

<span data-ttu-id="77d7f-104">Busque información de referencia de la biblioteca ManagedESENT.</span><span class="sxs-lookup"><span data-stu-id="77d7f-104">Find reference information for the ManagedESENT library.</span></span> <span data-ttu-id="77d7f-105">La biblioteca ManagedESENT proporciona acceso administrado a ESENT, el motor de base de datos incrustable que está nativo en Windows.</span><span class="sxs-lookup"><span data-stu-id="77d7f-105">The ManagedESENT library provides managed access to ESENT, the embeddable database engine that is native to Windows.</span></span>


<span data-ttu-id="77d7f-106">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="77d7f-106">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="77d7f-107">**En este artículo**</span><span class="sxs-lookup"><span data-stu-id="77d7f-107">**In this article**</span></span>  
<span data-ttu-id="77d7f-108">¿En qué se diferencia la biblioteca ManagedESENT de ESENT?</span><span class="sxs-lookup"><span data-stu-id="77d7f-108">How is the ManagedESENT library different than ESENT?</span></span>  
<span data-ttu-id="77d7f-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77d7f-109">Requirements</span></span>  
<span data-ttu-id="77d7f-110">En esta sección</span><span class="sxs-lookup"><span data-stu-id="77d7f-110">In this section</span></span>  

## <a name="how-is-the-managedesent-library-different-than-esent"></a><span data-ttu-id="77d7f-111">¿En qué se diferencia la biblioteca ManagedESENT de ESENT?</span><span class="sxs-lookup"><span data-stu-id="77d7f-111">How is the ManagedESENT library different than ESENT?</span></span>

<span data-ttu-id="77d7f-112">ESENT es un motor de base de datos transaccional incrustable que le permite crear aplicaciones personalizadas que necesitan un almacenamiento confiable, de alto rendimiento y de baja sobrecarga de datos.</span><span class="sxs-lookup"><span data-stu-id="77d7f-112">ESENT is an embeddable, transactional database engine that allows you to create custom applications that need reliable, high-performance, low-overhead storage of data.</span></span> <span data-ttu-id="77d7f-113">El motor ESENT puede ayudar con los datos que van desde algo tan sencillo como una tabla hash que es demasiado grande para almacenar en memoria, algo más complejo, como una aplicación con tablas, columnas e índices.</span><span class="sxs-lookup"><span data-stu-id="77d7f-113">The ESENT engine can help with data needs that range from something as simple as a hash table that is too large to store in memory, to something more complex, such as an application with tables, columns, and indexes.</span></span> <span data-ttu-id="77d7f-114">Para crear una aplicación con ESENT, use el esent.dll DLL que forma parte del sistema operativo Windows y escriba el código con C/C++.</span><span class="sxs-lookup"><span data-stu-id="77d7f-114">To create an application with ESENT, you use the esent.dll DLL that is part of the Windows operating system and write your code with C/C++.</span></span> <span data-ttu-id="77d7f-115">Para obtener más información sobre ESENT, vea [Referencia del motor de almacenamiento extensible](./extensible-storage-engine-reference.md).</span><span class="sxs-lookup"><span data-stu-id="77d7f-115">For more information about ESENT, see [Extensible Storage Engine Reference](./extensible-storage-engine-reference.md).</span></span>

<span data-ttu-id="77d7f-116">ManagedESENT se basa en esent.dll, que forma parte de Windows, por lo que no hay archivos binarios no administrados adicionales para descargar e instalar.</span><span class="sxs-lookup"><span data-stu-id="77d7f-116">ManagedESENT is built on top of esent.dll, which is part of Windows, so there are no extra unmanaged binaries to download and install.</span></span> <span data-ttu-id="77d7f-117">Con la biblioteca ManagedESENT, puede crear la aplicación mediante un lenguaje administrado como C \# en lugar de c/C++.</span><span class="sxs-lookup"><span data-stu-id="77d7f-117">With the ManagedESENT library, you can create your application by using a managed language such as C\# instead of C/C++.</span></span> <span data-ttu-id="77d7f-118">La biblioteca usa el mismo tipo y los mismos nombres de miembro para exponer la API de ESE, por lo que si ya está familiarizado con la estructura de esta API, puede pasar fácilmente a esta biblioteca administrada.</span><span class="sxs-lookup"><span data-stu-id="77d7f-118">The library uses the same type and member names to expose the ESE API, so if you are already familiar with the structure of this API, you can easily transition to this managed library.</span></span>

## <a name="requirements"></a><span data-ttu-id="77d7f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77d7f-119">Requirements</span></span>

<span data-ttu-id="77d7f-120">Esta biblioteca administrada requiere lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="77d7f-120">This managed library requires the following:</span></span>

  - <span data-ttu-id="77d7f-121">Un equipo que ejecuta una versión de Windows a partir de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77d7f-121">A computer running a version of Windows starting with Windows Vista</span></span>

  - <span data-ttu-id="77d7f-122">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="77d7f-122">Visual Studio 2012</span></span>

  - <span data-ttu-id="77d7f-123">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="77d7f-123">The .NET Framework 4.5</span></span>

## <a name="in-this-section"></a><span data-ttu-id="77d7f-124">En esta sección</span><span class="sxs-lookup"><span data-stu-id="77d7f-124">In this section</span></span>

  - [<span data-ttu-id="77d7f-125">Microsoft. ISAM. esent</span><span class="sxs-lookup"><span data-stu-id="77d7f-125">Microsoft.Isam.Esent</span></span>](./microsoft.isam.esent-namespace.md)

  - [<span data-ttu-id="77d7f-126">Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="77d7f-126">Microsoft.Isam.Esent.Interop</span></span>](./microsoft.isam.esent.interop-namespace.md)

  - [<span data-ttu-id="77d7f-127">Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="77d7f-127">Microsoft.Isam.Esent.Interop.Server2003</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)

  - [<span data-ttu-id="77d7f-128">Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="77d7f-128">Microsoft.Isam.Esent.Interop.Vista</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)

  - [<span data-ttu-id="77d7f-129">Microsoft. ISAM. esent. Interop. Windows7</span><span class="sxs-lookup"><span data-stu-id="77d7f-129">Microsoft.Isam.Esent.Interop.Windows7</span></span>](./microsoft.isam.esent.interop.windows7-namespace.md)

  - [<span data-ttu-id="77d7f-130">Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="77d7f-130">Microsoft.Isam.Esent.Interop.Windows8</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)

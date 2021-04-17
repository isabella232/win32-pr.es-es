---
description: Aunque existen pocos límites técnicos para el tipo y el tamaño de los datos que una aplicación puede almacenar en el registro, existen ciertas directrices prácticas para fomentar la eficacia del sistema.
ms.assetid: fa85ff87-3d72-4f71-856a-f43df7d19aa8
title: Espacio de almacenamiento del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b776498528d6c7deaacd92f9e010758b5d57c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667588"
---
# <a name="registry-storage-space"></a><span data-ttu-id="523f8-103">Espacio de almacenamiento del registro</span><span class="sxs-lookup"><span data-stu-id="523f8-103">Registry Storage Space</span></span>

<span data-ttu-id="523f8-104">Aunque existen pocos límites técnicos para el tipo y el tamaño de los datos que una aplicación puede almacenar en el registro, existen ciertas directrices prácticas para fomentar la eficacia del sistema.</span><span class="sxs-lookup"><span data-stu-id="523f8-104">Although there are few technical limits to the type and size of data an application can store in the registry, certain practical guidelines exist to promote system efficiency.</span></span> <span data-ttu-id="523f8-105">Una aplicación debe almacenar los datos de inicialización y configuración en el registro y almacenar otros tipos de datos en otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="523f8-105">An application should store configuration and initialization data in the registry, and store other kinds of data elsewhere.</span></span>

<span data-ttu-id="523f8-106">Por lo general, los datos que se componen de más de uno o dos kilobytes (K) deben almacenarse como un archivo y se hace referencia a ellos mediante una clave en el registro en lugar de almacenarse como un valor.</span><span class="sxs-lookup"><span data-stu-id="523f8-106">Generally, data consisting of more than one or two kilobytes (K) should be stored as a file and referred to by using a key in the registry rather than being stored as a value.</span></span> <span data-ttu-id="523f8-107">En lugar de duplicar grandes fragmentos de datos en el registro, una aplicación debe guardar los datos como un archivo y hacer referencia al archivo.</span><span class="sxs-lookup"><span data-stu-id="523f8-107">Instead of duplicating large pieces of data in the registry, an application should save the data as a file and refer to the file.</span></span> <span data-ttu-id="523f8-108">El código binario ejecutable nunca debe almacenarse en el registro.</span><span class="sxs-lookup"><span data-stu-id="523f8-108">Executable binary code should never be stored in the registry.</span></span>

<span data-ttu-id="523f8-109">Una entrada de valor utiliza mucho menos espacio de registro que una clave.</span><span class="sxs-lookup"><span data-stu-id="523f8-109">A value entry uses much less registry space than a key.</span></span> <span data-ttu-id="523f8-110">Para ahorrar espacio, una aplicación debe agrupar datos similares como una estructura y almacenar la estructura como un valor en lugar de almacenar cada uno de los miembros de la estructura como una clave independiente.</span><span class="sxs-lookup"><span data-stu-id="523f8-110">To save space, an application should group similar data together as a structure and store the structure as a value rather than storing each of the structure members as a separate key.</span></span> <span data-ttu-id="523f8-111">(Almacenar los datos en formato binario permite a una aplicación almacenar datos en un valor que, de otro modo, se compone de varios tipos incompatibles).</span><span class="sxs-lookup"><span data-stu-id="523f8-111">(Storing the data in binary form allows an application to store data in one value that would otherwise be made up of several incompatible types.)</span></span>

<span data-ttu-id="523f8-112">Las vistas de los archivos del registro se asignan en la memoria del grupo paginado.</span><span class="sxs-lookup"><span data-stu-id="523f8-112">Views of the registry files are mapped in paged pool memory.</span></span>

<span data-ttu-id="523f8-113">**Windows server 2008 para 32 bits, Windows Vista con SP1 para 32 bits, Windows Vista, Windows Server 2003 y Windows XP:** Las vistas de los archivos de registro se asignan en el espacio de direcciones de caché del equipo.</span><span class="sxs-lookup"><span data-stu-id="523f8-113">**Windows Server 2008 for 32-bit, Windows Vista with SP1 for 32-bit, Windows Vista, Windows Server 2003, Windows XP:** Views of the registry files are mapped in the computer cache address space.</span></span> <span data-ttu-id="523f8-114">Por lo tanto, independientemente del tamaño de los datos del registro, no se le cobrarán más de 4 megabytes (MB).</span><span class="sxs-lookup"><span data-stu-id="523f8-114">Therefore, regardless of the size of the registry data, it is not charged more than 4 megabytes (MB).</span></span>

<span data-ttu-id="523f8-115">El tamaño máximo de un subárbol del registro es 2 GB, excepto el subárbol del sistema.</span><span class="sxs-lookup"><span data-stu-id="523f8-115">The maximum size of a registry hive is 2 GB, except for the system hive.</span></span>

<span data-ttu-id="523f8-116">**Windows server 2003 con SP1, Windows server 2003 y Windows XP:** No hay ningún límite explícito en la cantidad total de espacio que pueden consumir los subárboles en la memoria del grupo paginado y en el espacio en disco, aunque las cuotas del sistema pueden afectar al tamaño máximo real.</span><span class="sxs-lookup"><span data-stu-id="523f8-116">**Windows Server 2003 with SP1, Windows Server 2003 and Windows XP:** There are no explicit limits on the total amount of space that may be consumed by hives in paged pool memory and in disk space, although system quotas may affect the actual maximum size.</span></span> <span data-ttu-id="523f8-117">El tamaño máximo de un subárbol del registro estaba limitado a 2 GB a partir de Windows Server 2003 con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="523f8-117">The maximum size of a registry hive was limited to 2 GB starting with Windows Server 2003 with Service Pack 2 (SP2).</span></span>

<span data-ttu-id="523f8-118">El tamaño máximo del subárbol del sistema está limitado por la memoria física, tal como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="523f8-118">The maximum size of the system hive is limited by physical memory as shown in the following table.</span></span> 

| <span data-ttu-id="523f8-119">System</span><span class="sxs-lookup"><span data-stu-id="523f8-119">System</span></span>                      | <span data-ttu-id="523f8-120">Tamaño máximo del subárbol del sistema</span><span class="sxs-lookup"><span data-stu-id="523f8-120">Maximum size of the system hive</span></span>                                                                                                                                                                                                            |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="523f8-121">sistemas basados en x86</span><span class="sxs-lookup"><span data-stu-id="523f8-121">x86-based systems</span></span>           | <span data-ttu-id="523f8-122">50 por ciento de la memoria física, hasta 400 MB. **Windows server 2003 con SP2, Windows server 2003 con SP1, Windows server 2003 y Windows XP:** 25 por ciento de memoria física, hasta 200 MB.</span><span class="sxs-lookup"><span data-stu-id="523f8-122">50 percent of physical memory, up to 400 MB.**Windows Server 2003 with SP2, Windows Server 2003 with SP1, Windows Server 2003 and Windows XP:** 25 percent of physical memory, up to 200 MB.</span></span><br/>                                    |
| <span data-ttu-id="523f8-123">sistemas basados en x64</span><span class="sxs-lookup"><span data-stu-id="523f8-123">x64-based systems</span></span>           | <span data-ttu-id="523f8-124">50 por ciento de la memoria física, hasta 1,5 GB. **Windows Server 2003 con SP2:** 25 por ciento de la memoria del sistema, hasta 200 MB.</span><span class="sxs-lookup"><span data-stu-id="523f8-124">50 percent of physical memory, up to 1.5 GB.**Windows Server 2003 with SP2:** 25 percent of system memory, up to 200 MB.</span></span><br/> <span data-ttu-id="523f8-125">**Windows server 2003 con SP1, Windows server 2003 y Windows XP 64-bit Edition:** 32 MB.</span><span class="sxs-lookup"><span data-stu-id="523f8-125">**Windows Server 2003 with SP1, Windows Server 2003 and Windows XP 64-Bit Edition:** 32 MB.</span></span><br/> |
| <span data-ttu-id="523f8-126">Sistemas basados en Itanium de Intel</span><span class="sxs-lookup"><span data-stu-id="523f8-126">Intel Itanium-based systems</span></span> | <span data-ttu-id="523f8-127">50 por ciento de la memoria física, hasta 1 GB. **Windows server 2008, Windows Vista, Windows server 2003 con SP2, Windows server 2003 con SP1, Windows server 2003 y Windows XP 64-bit Edition:** 32 MB.</span><span class="sxs-lookup"><span data-stu-id="523f8-127">50 percent of physical memory, up to 1 GB.**Windows Server 2008, Windows Vista, Windows Server 2003 with SP2, Windows Server 2003 with SP1, Windows Server 2003 and Windows XP 64-Bit Edition:** 32 MB.</span></span><br/>                         |



 

## <a name="windows-2000"></a><span data-ttu-id="523f8-128">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="523f8-128">Windows 2000</span></span>

<span data-ttu-id="523f8-129">Los datos del registro se almacenan en el grupo paginado, un área de memoria física que se usa para los datos del sistema que se pueden escribir en el disco cuando no están en uso.</span><span class="sxs-lookup"><span data-stu-id="523f8-129">Registry data is stored in the paged pool, an area of physical memory used for system data that can be written to disk when not in use.</span></span> <span data-ttu-id="523f8-130">El valor **RegistrySizeLimit** establece la cantidad máxima de bloque paginado que pueden consumir los datos del registro de todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="523f8-130">The **RegistrySizeLimit** value establishes the maximum amount of paged pool that can be consumed by registry data from all applications.</span></span> <span data-ttu-id="523f8-131">Este valor se encuentra en la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="523f8-131">This value is located in the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
```

<span data-ttu-id="523f8-132">De forma predeterminada, el límite de tamaño del registro es el 25 por ciento del grupo paginado.</span><span class="sxs-lookup"><span data-stu-id="523f8-132">By default, the registry size limit is 25 percent of the paged pool.</span></span> <span data-ttu-id="523f8-133">(El tamaño predeterminado del grupo paginado es 32 MB, por lo que es de 8 MB). El sistema garantiza que el valor mínimo de **RegistrySizeLimit** es 4 MB y el máximo es aproximadamente el 80 por ciento del valor de **PagedPoolSize** .</span><span class="sxs-lookup"><span data-stu-id="523f8-133">(The default size of the paged pool is 32 MB, so this is 8 MB.) The system ensures that the minimum value of **RegistrySizeLimit** is 4 MB and the maximum is approximately 80 percent of the **PagedPoolSize** value.</span></span> <span data-ttu-id="523f8-134">Si el valor de esta entrada es superior al 80 por ciento del tamaño del grupo paginado, el sistema establece el tamaño máximo del registro en el 80 por ciento del tamaño del grupo paginado.</span><span class="sxs-lookup"><span data-stu-id="523f8-134">If the value of this entry is greater than 80 percent of the size of the paged pool, the system sets the maximum size of the registry to 80 percent of the size of the paged pool.</span></span> <span data-ttu-id="523f8-135">Esto impide que el registro consuma el espacio necesario para los procesos.</span><span class="sxs-lookup"><span data-stu-id="523f8-135">This prevents the registry from consuming space needed by processes.</span></span> <span data-ttu-id="523f8-136">Tenga en cuenta que el establecimiento de este valor no asigna espacio en el grupo paginado, ni garantiza que el espacio estará disponible si es necesario.</span><span class="sxs-lookup"><span data-stu-id="523f8-136">Note that setting this value does not allocate space in the paged pool, nor does it assure that the space will be available if needed.</span></span>

<span data-ttu-id="523f8-137">El tamaño del grupo paginado viene determinado por el valor de **PagedPoolSize** en la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="523f8-137">The paged pool size is determined by the **PagedPoolSize** value in the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            SessionManager
               MemoryManagement
```

<span data-ttu-id="523f8-138">Para obtener un ejemplo de cómo determinar los tamaños actuales y máximos del registro, vea [determinar el tamaño del registro](determining-the-registry-size.md).</span><span class="sxs-lookup"><span data-stu-id="523f8-138">For an example of how to determine the current and maximum sizes of the registry, see [Determining the Registry Size](determining-the-registry-size.md).</span></span>

<span data-ttu-id="523f8-139">El grupo paginado máximo es de aproximadamente 300.470 MB, por lo que el límite de tamaño del registro es de 240-376 MB.</span><span class="sxs-lookup"><span data-stu-id="523f8-139">The maximum paged pool is approximately 300,470 MB so the registry size limit is 240-376 MB.</span></span> <span data-ttu-id="523f8-140">Sin embargo, si se usa el modificador/3GB, el tamaño máximo del grupo paginado es 192 MB, por lo que el registro puede tener un máximo de 153,6 MB.</span><span class="sxs-lookup"><span data-stu-id="523f8-140">However, if the /3GB switch is used, the maximum paged pool size is 192 MB, so the registry can be a maximum of 153.6 MB.</span></span>

 

 





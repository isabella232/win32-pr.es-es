---
description: Como alternativa a la creación y configuración de particiones locales a través de la herramienta administrativa Servicios de componentes, puede administrar las particiones mediante programación con las propiedades y colecciones de administración de COM+ específicas de la partición.
ms.assetid: 82f790cf-3f94-44d9-b722-89a6013d0300
title: Administrar particiones locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd551fc73c76067c4ab2e988fba79ee702df53c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000781"
---
# <a name="managing-local-partitions"></a><span data-ttu-id="c087b-103">Administrar particiones locales</span><span class="sxs-lookup"><span data-stu-id="c087b-103">Managing Local Partitions</span></span>

<span data-ttu-id="c087b-104">Como alternativa a la creación y configuración de particiones locales a través de la herramienta administrativa Servicios de componentes, puede administrar las particiones mediante programación con las propiedades y colecciones de administración de COM+ específicas de la partición.</span><span class="sxs-lookup"><span data-stu-id="c087b-104">As an alternative to creating and configuring local partitions through the Component Services administrative tool, you can manage partitions programmatically by using partition-specific COM+ administration collections and properties.</span></span>

> [!Note]  
> <span data-ttu-id="c087b-105">El servicio de particiones COM+ no está habilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c087b-105">The COM+ partitions service is not enabled by default.</span></span> <span data-ttu-id="c087b-106">Para usar el servicio de particiones de COM+, debe habilitarlo mediante la herramienta de administración de servicios de componentes o cambiando la propiedad PartitionsEnabled de la colección [**LocalComputer**](localcomputer.md) a true.</span><span class="sxs-lookup"><span data-stu-id="c087b-106">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

<span data-ttu-id="c087b-107">La subrutina siguiente escrita en Visual Basic Script muestra cómo crear una partición en el equipo local:</span><span class="sxs-lookup"><span data-stu-id="c087b-107">The following subroutine written in Visual Basic script demonstrates how to create a partition on the local computer:</span></span>


```VB
Sub CreatePartition (PartitonGuid, PartitionName)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collPartitions = cat.GetCollection("Partitions")
   collPartitions.Populate
   Set part = collPartitions.Add
   ' If you don't specify a partition GUID, one is created for you.
   ' Otherwise, you can specify one this way:
   part.Value("ID") = PartitonGuid
   part.Value("Name") = PartitionName
   collPartitions.SaveChanges
   Set part = Nothing
   Set collPartitions = Nothing
   Set cat = Nothing
End Sub 
```



<span data-ttu-id="c087b-108">La subrutina siguiente escrita en Visual Basic Script muestra cómo eliminar una partición del equipo local:</span><span class="sxs-lookup"><span data-stu-id="c087b-108">The following subroutine written in Visual Basic script demonstrates how to delete a partition from the local computer:</span></span>


```VB
Sub DeletePartition (PartitionName)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collPartitions = cat.GetCollection("Partitions")
   collPartitions.Populate
   numPartitions = collPartitions.Count
   ' Begin with the last partition, and work forward through the list.
   For i = numPartitions - 1 To 0 Step -1 
       If collPartitions.Item(i).Value("Name") = PartitionName Then
           collPartitions.Remove i
       End If
   Next
   collPartitions.SaveChanges
   Set collPartitions = Nothing
   Set cat = Nothing
End Sub
```



<span data-ttu-id="c087b-109">La subrutina siguiente escrita en Visual Basic Script muestra cómo establecer la partición predeterminada para un usuario:</span><span class="sxs-lookup"><span data-stu-id="c087b-109">The following subroutine written in Visual Basic script demonstrates how to set the default partition for a user:</span></span>


```VB
Sub SetDefaultPartitionForUser(UserName, PartitionGuid)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collUsers = cat.GetCollection("PartitionUsers")
   collUsers.Populate
   Set user = collUsers.Add
   user.Value("AccountName") = UserName
   user.Value("DefaultPartitionID") = PartitionGuid
   collUsers.SaveChanges
   Set collUsers = Nothing
   Set cat = Nothing
End Sub
```



<span data-ttu-id="c087b-110">La subrutina siguiente escrita en Visual Basic Script muestra cómo quitar la partición predeterminada para un usuario:</span><span class="sxs-lookup"><span data-stu-id="c087b-110">The following subroutine written in Visual Basic script demonstrates how to remove the default partition for a user:</span></span>


```VB
Sub RemoveDefaultPartitionForUser(UserName)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collUsers = cat.GetCollection("PartitionUsers")
   collUsers.Populate
   numUsers = collUsers.Count
   ' Begin with the last user, and work forward through the list.
   For i = numUsers - 1 To 0 Step -1
       If collUsers.Item(i).Value("AccountName") = UserName Then
           collUsers.Remove i
       End If
   Next
   collUsers.SaveChanges
   Set collUsers = Nothing
   Set cat = Nothing
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="c087b-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c087b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c087b-112">Recopilación de métricas de partición</span><span class="sxs-lookup"><span data-stu-id="c087b-112">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="c087b-113">Configuración de la memoria caché de partición</span><span class="sxs-lookup"><span data-stu-id="c087b-113">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="c087b-114">Agrupar aplicaciones en particiones</span><span class="sxs-lookup"><span data-stu-id="c087b-114">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="c087b-115">Administrar particiones en Active Directory</span><span class="sxs-lookup"><span data-stu-id="c087b-115">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="c087b-116">Establecer derechos administrativos para una partición</span><span class="sxs-lookup"><span data-stu-id="c087b-116">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




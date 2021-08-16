---
description: Como alternativa a la creación y configuración de particiones locales a través de la herramienta administrativa Servicios de componentes, puede administrar particiones mediante programación mediante el uso de propiedades y colecciones de administración de COM+ específicas de la partición.
ms.assetid: 82f790cf-3f94-44d9-b722-89a6013d0300
title: Administración de particiones locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124d0b9ef7bf54f07a6b28561428c57834a6e15ec11c4ed5c89fb92f95f0a950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306266"
---
# <a name="managing-local-partitions"></a>Administración de particiones locales

Como alternativa a la creación y configuración de particiones locales a través de la herramienta administrativa Servicios de componentes, puede administrar particiones mediante programación mediante el uso de propiedades y colecciones de administración de COM+ específicas de la partición.

> [!Note]  
> El servicio de particiones COM+ no está habilitado de forma predeterminada. Para usar el servicio de particiones COM+, debe habilitarlo a través de la herramienta de administración servicios de componentes o cambiando la propiedad PartitionsEnabled de la colección [**LocalComputer**](localcomputer.md) a True.

 

La siguiente subrutina escrita Visual Basic script muestra cómo crear una partición en el equipo local:


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



La siguiente subrutina escrita en Visual Basic script muestra cómo eliminar una partición del equipo local:


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



La siguiente subrutina escrita en Visual Basic script muestra cómo establecer la partición predeterminada para un usuario:


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



La siguiente subrutina escrita en Visual Basic script muestra cómo quitar la partición predeterminada para un usuario:


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recopilación de métricas de partición](collecting-partition-metrics.md)
</dt> <dt>

[Configuración de la caché de particiones](configuring-the-partition-cache.md)
</dt> <dt>

[Agrupación de aplicaciones en particiones](grouping-applications-into-partitions.md)
</dt> <dt>

[Administración de particiones dentro de Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Establecer derechos administrativos para una partición](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




---
description: Un solicitante debe seleccionar un proveedor concreto solo si tiene información sobre los proveedores disponibles.
ms.assetid: 1a3bc938-2754-4fa2-bd7f-e9b3e876bf6c
title: Selección de proveedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39435f8f34091ccef51a6cce85b2c596f0c687d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156101"
---
# <a name="selecting-providers"></a><span data-ttu-id="7935d-103">Selección de proveedores</span><span class="sxs-lookup"><span data-stu-id="7935d-103">Selecting Providers</span></span>

<span data-ttu-id="7935d-104">Un solicitante debe seleccionar un proveedor concreto solo si tiene información sobre los proveedores disponibles.</span><span class="sxs-lookup"><span data-stu-id="7935d-104">A requester should select a specific provider only if it has some information about the providers available.</span></span>

<span data-ttu-id="7935d-105">Dado que este no suele ser el caso, se recomienda que un solicitante suministre el GUID \_ null como un identificador de proveedor a [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset), que permite al sistema elegir un proveedor según el siguiente algoritmo:</span><span class="sxs-lookup"><span data-stu-id="7935d-105">Because this will not generally be the case, it is recommended that a requester supply GUID\_NULL as a provider ID to [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset), which allows the system to choose a provider according to the following algorithm:</span></span>

1.  <span data-ttu-id="7935d-106">Si hay disponible un proveedor de hardware que admita el volumen especificado, se selecciona.</span><span class="sxs-lookup"><span data-stu-id="7935d-106">If a hardware provider that supports the given volume is available, it is selected.</span></span>
2.  <span data-ttu-id="7935d-107">Si no hay ningún proveedor de hardware disponible, si hay algún proveedor de software específico para el volumen dado disponible, se selecciona.</span><span class="sxs-lookup"><span data-stu-id="7935d-107">If no hardware provider is available, then if any software provider specific to the given volume is available, it is selected.</span></span>
3.  <span data-ttu-id="7935d-108">Si no hay ningún proveedor de hardware y no hay ningún proveedor de software específico para los volúmenes disponibles, se seleccionará el proveedor del sistema.</span><span class="sxs-lookup"><span data-stu-id="7935d-108">If no hardware provider and no software provider specific to the volumes is available, the system provider is selected.</span></span>

<span data-ttu-id="7935d-109">Sin embargo, un solicitante puede obtener información sobre los proveedores disponibles mediante [**IVssBackupComponents:: query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span><span class="sxs-lookup"><span data-stu-id="7935d-109">However, a requester can obtain information about available providers by using [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span></span> <span data-ttu-id="7935d-110">Con esta información, y solo si la aplicación de copia de seguridad tiene una buena comprensión de los distintos proveedores, un solicitante puede proporcionar un identificador de proveedor válido a [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).</span><span class="sxs-lookup"><span data-stu-id="7935d-110">With this information, and only if the backup application has a good understanding of the various providers, a requester can supply a valid provider ID to [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).</span></span>

<span data-ttu-id="7935d-111">Tenga en cuenta que no es necesario que todos los volúmenes tengan el mismo proveedor.</span><span class="sxs-lookup"><span data-stu-id="7935d-111">Note that all volumes do not need to have the same provider.</span></span>

 

 




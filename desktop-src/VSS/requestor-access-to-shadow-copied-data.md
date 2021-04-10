---
description: Una vez completada la instantánea, el mecanismo más importante para obtener acceso a los datos de archivo que contiene es mediante el uso del objeto de dispositivo de la instantánea.
ms.assetid: 21efdbd6-a487-4e6f-8e3c-b9224bcf92da
title: Acceso del solicitante a los datos de copia sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6265586f70054277170b44f23efc52d56842e3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156112"
---
# <a name="requester-access-to-shadow-copied-data"></a><span data-ttu-id="76cae-103">Acceso del solicitante a los datos de copia sombra</span><span class="sxs-lookup"><span data-stu-id="76cae-103">Requester Access to Shadow Copied Data</span></span>

<span data-ttu-id="76cae-104">Una vez completada la instantánea, el mecanismo más importante para obtener acceso a los datos de archivo que contiene es mediante el uso del [*objeto de dispositivo*](vssgloss-d.md)de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="76cae-104">Once the shadow copy has completed, the most important mechanism for getting access to the file data it contains is through the use of the shadow copy's [*device object*](vssgloss-d.md).</span></span>

<span data-ttu-id="76cae-105">El miembro **m \_ pwszSnapshotDeviceObject** de una [**estructura \_ \_ prop de instantánea de VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) es una cadena que contiene un objeto de dispositivo de un volumen de copia sombra.</span><span class="sxs-lookup"><span data-stu-id="76cae-105">The **m\_pwszSnapshotDeviceObject** member of a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure is a string containing a shadow-copied volume's device object.</span></span> <span data-ttu-id="76cae-106">Un solicitante puede obtener el objeto de la instantánea de VSS de un volumen de copia sombra si conoce el **\_ identificador de VSS** del volumen (GUID de identificación) y lo pasa a [**IVssBackupComponents:: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties). **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="76cae-106">A requester can obtain a shadow-copied volume's **VSS\_SNAPSHOT\_PROP** object if it knows the volume's **VSS\_ID** (identifying GUID) and passes it to [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).</span></span>

<span data-ttu-id="76cae-107">Un solicitante también puede obtener información de la propiedad de instantáneas mediante el miembro **obj. Snap** de la estructura [**\_ \_ Prop del objeto de VSS**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (que es una estructura de instantánea de la [**\_ instantánea \_ de VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) ) obtenida mediante [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) para recorrer en iteración la lista de objetos devueltos por una llamada a [**IVssBackupComponents:: query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span><span class="sxs-lookup"><span data-stu-id="76cae-107">A requester can also obtain shadow copy property information by using the **Obj.Snap** member of the [**VSS\_OBJECT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) structure (which is a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure) obtained by using [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) to iterate over the list of objects returned by a call to [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span></span>

<span data-ttu-id="76cae-108">El objeto de dispositivo debe interpretarse como la raíz de un volumen de copia sombra.</span><span class="sxs-lookup"><span data-stu-id="76cae-108">The device object should be interpreted as the root of a shadow-copied volume.</span></span> <span data-ttu-id="76cae-109">Por esta razón, el objeto de dispositivo no contiene ninguna barra diagonal inversa (" \\ ").</span><span class="sxs-lookup"><span data-stu-id="76cae-109">For this reason, the device object contains no backslash ("\\").</span></span>

<span data-ttu-id="76cae-110">Las rutas de acceso en el volumen de la instantánea se obtienen reemplazando la raíz de la ruta de acceso original por el objeto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="76cae-110">Paths on the shadow copied volume are obtained by replacing the root of the original path with the device object.</span></span> <span data-ttu-id="76cae-111">Por ejemplo, dada una ruta de acceso en el volumen original de "C: \\ Database \\ \* . mdb" y una instancia de instantánea de la [**\_ instantánea \_ de VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) de snapProp, obtendría la ruta de acceso en el volumen de copia sombra concatenando snapPropm \_ pwszShadow copyDeviceObject, " \\ " y " \\ Database \\ \* . mdb".</span><span class="sxs-lookup"><span data-stu-id="76cae-111">For example, given a path on the original volume of "C:\\DATABASE\\\*.mdb" and a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) instance of snapProp, you would obtain the path on the shadow copied volume by concatenating snapPropm\_pwszShadow copyDeviceObject, "\\", and "\\DATABASE\\\*.mdb".</span></span>

<span data-ttu-id="76cae-112">Los conjuntos de archivos de VSS pueden tener caracteres comodín en los descriptores de archivo, por lo que obtener una lista completa de los archivos en una instantánea administrada por un componente podría requerir el uso de métodos como **FindFileFirst**, **FindFileFirstEx** y **FindNextFile**.</span><span class="sxs-lookup"><span data-stu-id="76cae-112">The VSS file sets might have wildcard characters in their file descriptors, so obtaining a full list of the files on a shadow copy managed by a component might require the use of methods such as **FindFileFirst**, **FindFileFirstEx**, and **FindNextFile**.</span></span>

 

 




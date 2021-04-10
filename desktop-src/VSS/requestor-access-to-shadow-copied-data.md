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
# <a name="requester-access-to-shadow-copied-data"></a>Acceso del solicitante a los datos de copia sombra

Una vez completada la instantánea, el mecanismo más importante para obtener acceso a los datos de archivo que contiene es mediante el uso del [*objeto de dispositivo*](vssgloss-d.md)de la instantánea.

El miembro **m \_ pwszSnapshotDeviceObject** de una [**estructura \_ \_ prop de instantánea de VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) es una cadena que contiene un objeto de dispositivo de un volumen de copia sombra. Un solicitante puede obtener el objeto de la instantánea de VSS de un volumen de copia sombra si conoce el **\_ identificador de VSS** del volumen (GUID de identificación) y lo pasa a [**IVssBackupComponents:: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties). **\_ \_**

Un solicitante también puede obtener información de la propiedad de instantáneas mediante el miembro **obj. Snap** de la estructura [**\_ \_ Prop del objeto de VSS**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (que es una estructura de instantánea de la [**\_ instantánea \_ de VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) ) obtenida mediante [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) para recorrer en iteración la lista de objetos devueltos por una llamada a [**IVssBackupComponents:: query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).

El objeto de dispositivo debe interpretarse como la raíz de un volumen de copia sombra. Por esta razón, el objeto de dispositivo no contiene ninguna barra diagonal inversa (" \\ ").

Las rutas de acceso en el volumen de la instantánea se obtienen reemplazando la raíz de la ruta de acceso original por el objeto de dispositivo. Por ejemplo, dada una ruta de acceso en el volumen original de "C: \\ Database \\ \* . mdb" y una instancia de instantánea de la [**\_ instantánea \_ de VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) de snapProp, obtendría la ruta de acceso en el volumen de copia sombra concatenando snapPropm \_ pwszShadow copyDeviceObject, " \\ " y " \\ Database \\ \* . mdb".

Los conjuntos de archivos de VSS pueden tener caracteres comodín en los descriptores de archivo, por lo que obtener una lista completa de los archivos en una instantánea administrada por un componente podría requerir el uso de métodos como **FindFileFirst**, **FindFileFirstEx** y **FindNextFile**.

 

 




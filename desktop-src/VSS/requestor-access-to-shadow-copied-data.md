---
description: Una vez completada la instantánea, el mecanismo más importante para obtener acceso a los datos de archivo que contiene es mediante el uso del objeto de dispositivo de la instantánea.
ms.assetid: 21efdbd6-a487-4e6f-8e3c-b9224bcf92da
title: Acceso del solicitante a los datos copiados en la sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6265586f70054277170b44f23efc52d56842e3d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473352"
---
# <a name="requester-access-to-shadow-copied-data"></a>Acceso del solicitante a los datos copiados en la sombra

Una vez completada la instantánea, el mecanismo más importante para obtener acceso a los datos de archivo que contiene es mediante el uso del objeto de dispositivo de [*la instantánea*](vssgloss-d.md).

El **miembro m \_ pwszSnapshotDeviceObject** de una estructura [**VSS SNAPSHOT \_ \_ PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) es una cadena que contiene el objeto de dispositivo de un volumen copiado en la sombra. Un solicitante puede obtener el objeto **VSS \_ SNAPSHOT \_ PROP** de un volumen instantánea si conoce el identificador **VSS \_** del volumen (identificador GUID de identificación) y lo pasa a [**IVssBackupComponents::GetSnapshotProperties.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties)

Un solicitante también puede obtener información de propiedades de instantáneas mediante el miembro **Obj.Snap** de la estructura PROP de [**VSS \_ \_ OBJECT**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (que es una estructura PROP de INSTANTÁNEA DE [**VSS) \_ \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) obtenida mediante [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) para recorrer en iteración la lista de objetos devueltos por una llamada a [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).

El objeto de dispositivo debe interpretarse como la raíz de un volumen de instantáneas. Por este motivo, el objeto de dispositivo no contiene ninguna barra diagonal inversa (" \\ ").

Las rutas de acceso del volumen copiado en la sombra se obtienen reemplazando la raíz de la ruta de acceso original por el objeto de dispositivo. Por ejemplo, dada una ruta de acceso en el volumen original de "C: DATABASE .mdb" y una instancia de VSS SNAPSHOT PROP de snapProp, obtendría la ruta de acceso en el volumen instantáneado \\ \\ \* concatenando snapPropm [**\_ \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) \_ pwszShadow copyDeviceObject, " " y \\ " DATABASE \\ \\ \* .mdb".

Los conjuntos de archivos VSS pueden tener caracteres comodín en sus descriptores de archivo, por lo que obtener una lista completa de los archivos de una instantánea administrada por un componente podría requerir el uso de métodos como **FindFileFirst,** **FindFileFirstEx** y **FindNextFile.**

 

 




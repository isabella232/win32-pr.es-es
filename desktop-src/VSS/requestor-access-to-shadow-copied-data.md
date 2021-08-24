---
description: Una vez completada la instantánea, el mecanismo más importante para obtener acceso a los datos de archivo que contiene es mediante el uso del objeto de dispositivo de la instantánea.
ms.assetid: 21efdbd6-a487-4e6f-8e3c-b9224bcf92da
title: Acceso del solicitante a los datos copiados en la sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779e3947adff28c8f3190026921c398677afc7efaa484903bf165250f41bc191
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767705"
---
# <a name="requester-access-to-shadow-copied-data"></a>Acceso del solicitante a los datos copiados en la sombra

Una vez completada la instantánea, el mecanismo más importante para obtener acceso a los datos de archivo que contiene es mediante el uso del objeto de dispositivo de [*la instantánea*](vssgloss-d.md).

El **miembro m \_ pwszSnapshotDeviceObject** de una estructura [**PROP de INSTANTÁNEA \_ \_ DE VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) es una cadena que contiene el objeto de dispositivo de un volumen instantánea. Un solicitante puede obtener el objeto **VSS \_ SNAPSHOT \_ PROP** de un volumen instantánea si conoce el identificador **vsS \_** del volumen (identificador GUID de identificación) y lo pasa a [**IVssBackupComponents::GetSnapshotProperties.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties)

Un solicitante también puede obtener información de propiedades de instantáneas mediante el miembro **Obj.Snap** de la estructura PROP de [**VSS \_ \_ OBJECT**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (que es una estructura PROP de [**INSTANTÁNEA \_ \_ DE VSS)**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) obtenida mediante [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) para recorrer en iteración la lista de objetos devueltos por una llamada a [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).

El objeto de dispositivo debe interpretarse como la raíz de un volumen sombreado. Por esta razón, el objeto de dispositivo no contiene ninguna barra diagonal inversa (" \\ ").

Las rutas de acceso del volumen copiado en la sombra se obtienen reemplazando la raíz de la ruta de acceso original por el objeto de dispositivo. Por ejemplo, dada una ruta de acceso en el volumen original de "C: DATABASE .mdb" y una instancia de VSS SNAPSHOT PROP de snapProp, obtendría la ruta de acceso en el volumen copiado en la sombra \\ \\ \* concatenando snapPropm [**\_ \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) \_ pwszShadow copyDeviceObject, " \\ y " DATABASE \\ \\ \* .mdb".

Los conjuntos de archivos VSS pueden tener caracteres comodín en sus descriptores de archivo, por lo que obtener una lista completa de los archivos de una instantánea administrada por un componente podría requerir el uso de métodos como **FindFileFirst**, **FindFileFirstEx** y **FindNextFile.**

 

 




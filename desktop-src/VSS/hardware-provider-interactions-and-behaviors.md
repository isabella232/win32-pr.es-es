---
description: Interacciones y comportamientos del proveedor de hardware
ms.assetid: 059968cf-43e5-4442-b757-80afdd66799f
title: Interacciones y comportamientos del proveedor de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa30add6b34a7f3a0c45c88346c32c43e99398e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276353"
---
# <a name="hardware-provider-interactions-and-behaviors"></a>Interacciones y comportamientos del proveedor de hardware

Los proveedores de hardware pueden admitir instantáneas de copia en escritura o de reflejo de copia completa (diferencial y/o Plex). La asignación de recursos para instantáneas debe seguir el contexto especificado por el solicitante en [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), enumerado por el [**\_ \_ \_ contexto de instantáneas de VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context), para el conjunto de instantáneas.

-   Si el solicitante especifica un contexto de instantánea compatible con el proveedor, el proveedor debe crear una instantánea con ese método.
-   Si el solicitante especifica un contexto de instantáneas que no es compatible con el proveedor, el proveedor no debe intentar crear la instantánea y devolver el **valor false** a través del parámetro *pbIsSupported* de [**IVssHardwareSnapshotProvider:: AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported).
-   Si el solicitante no especifica explícitamente un contexto de instantáneas, el proveedor debe usar un comportamiento predeterminado razonable para la creación de instantáneas.

Los proveedores de hardware asociados a los subsistemas RAID de SAN deben admitir instantáneas transportables para permitir el movimiento entre hosts en una red SAN.

No es necesario coordinar los proveedores de hardware que se ejecutan en varios equipos en una SAN y administrar el mismo subsistema RAID en una SAN. El Coordinador mantiene cualquier estado necesario. Se reconocen dos tipos de estado:

-   Estado necesario para admitir el acceso a los datos a los volúmenes contenidos en una instantánea de hardware. Esto incluye cualquier etiquetado de un volumen como de solo lectura u oculto. Este estado debe estar en el LUN de hardware y viajar con el LUN. Este estado se conserva entre el tiempo de arranque y/o la detección de dispositivos. VSS administra este estado durante la vigencia de la instantánea.
-   Estado necesario para reconocer un volumen específico como parte de un conjunto de instantáneas. VSS conserva este estado junto con el solicitante que creó originalmente el conjunto de instantáneas.

Para obtener más información, vea los temas siguientes:

-   [Proceso de creación de instantáneas](the-shadow-copy-creation-process.md)
-   [Comportamientos necesarios para los proveedores de instantáneas](required-behaviors-for-shadow-copy-providers.md)
-   [Transiciones de estado en proveedores de instantáneas](state-transitions-in-shadow-copy-providers.md)
-   [Control de errores en los proveedores de instantáneas](error-handling-in-shadow-copy-providers.md)

 

 




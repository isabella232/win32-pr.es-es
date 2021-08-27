---
description: Interacciones y comportamientos del proveedor de hardware
ms.assetid: 059968cf-43e5-4442-b757-80afdd66799f
title: Interacciones y comportamientos del proveedor de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7c8029b32ee3387b86519da8630d995820bf3dab5da79769ca26f618ef32660
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122064"
---
# <a name="hardware-provider-interactions-and-behaviors"></a>Interacciones y comportamientos del proveedor de hardware

Los proveedores de hardware pueden admitir instantáneas de copia en escritura o de reflejo de copia completa (diferencial o plex). La asignación de recursos para instantáneas debe seguir el contexto especificado por el solicitante en [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), enumerado por [**\_ VSS \_ SNAPSHOT \_ CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context), para el conjunto de instantáneas.

-   Si el solicitante especifica un contexto de instantánea compatible con el proveedor, el proveedor debe crear una instantánea con ese método.
-   Si el solicitante especifica un contexto de instantánea que no es compatible con el proveedor, el proveedor no debe intentar crear la instantánea y devolver **FALSE** a través del parámetro *pbIsSupported* en [**IVssHardwareSnapshotProvider::AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported).
-   Si el solicitante no especifica explícitamente un contexto de instantánea, el proveedor debe usar un comportamiento predeterminado razonable para la creación de instantáneas.

Los proveedores de hardware asociados con subsistemas RAID de SAN deben admitir instantáneas transportables para permitir el movimiento entre hosts en una SAN.

Los proveedores de hardware que se ejecutan en varias máquinas en una SAN y que aún administran el mismo subsistema RAID no necesitan coordinarse entre proveedores en una SAN. El coordinador mantiene cualquier estado necesario. Se reconocen dos tipos de estado:

-   Estado necesario para admitir el acceso de datos a los volúmenes contenidos en una instantánea de hardware. Esto incluye cualquier etiquetado de un volumen como de solo lectura u oculto. Este estado debe estar en el LUN de hardware y viajar con el LUN. Este estado se conserva en las épocas de arranque o en la detección de dispositivos. VSS administra este estado durante la vigencia de la instantánea.
-   Estado necesario para reconocer un volumen específico como parte de un conjunto de instantáneas. VSS conserva este estado junto con el solicitante que creó originalmente el conjunto de instantáneas.

Para obtener más información, vea los temas siguientes:

-   [El proceso de creación de instantáneas](the-shadow-copy-creation-process.md)
-   [Comportamientos necesarios para los proveedores de instantáneas](required-behaviors-for-shadow-copy-providers.md)
-   [Transiciones de estado en proveedores de instantáneas](state-transitions-in-shadow-copy-providers.md)
-   [Control de errores en proveedores de instantáneas](error-handling-in-shadow-copy-providers.md)

 

 




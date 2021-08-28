---
description: Un solicitante debe seleccionar un proveedor específico solo si tiene información sobre los proveedores disponibles.
ms.assetid: 1a3bc938-2754-4fa2-bd7f-e9b3e876bf6c
title: Selección de proveedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2451f172a569a23ba4799c16f8598ade4e6fb011f051b7ba7d948c7a366f22e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124505"
---
# <a name="selecting-providers"></a>Selección de proveedores

Un solicitante debe seleccionar un proveedor específico solo si tiene información sobre los proveedores disponibles.

Dado que este no suele ser el caso, se recomienda que un solicitante proporcione GUID NULL como identificador de proveedor \_ a [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset), lo que permite al sistema elegir un proveedor según el algoritmo siguiente:

1.  Si hay disponible un proveedor de hardware que admita el volumen determinado, se selecciona.
2.  Si no hay ningún proveedor de hardware disponible, si hay disponible algún proveedor de software específico para el volumen determinado, se selecciona.
3.  Si no hay ningún proveedor de hardware ni ningún proveedor de software específico para los volúmenes disponible, se selecciona el proveedor del sistema.

Sin embargo, un solicitante puede obtener información sobre los proveedores disponibles mediante [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query). Con esta información, y solo si la aplicación de copia de seguridad tiene una buena comprensión de los distintos proveedores, un solicitante puede proporcionar un identificador de proveedor válido a [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).

Tenga en cuenta que no es necesario que todos los volúmenes tengan el mismo proveedor.

 

 




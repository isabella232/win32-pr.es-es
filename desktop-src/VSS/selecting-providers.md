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
# <a name="selecting-providers"></a>Selección de proveedores

Un solicitante debe seleccionar un proveedor concreto solo si tiene información sobre los proveedores disponibles.

Dado que este no suele ser el caso, se recomienda que un solicitante suministre el GUID \_ null como un identificador de proveedor a [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset), que permite al sistema elegir un proveedor según el siguiente algoritmo:

1.  Si hay disponible un proveedor de hardware que admita el volumen especificado, se selecciona.
2.  Si no hay ningún proveedor de hardware disponible, si hay algún proveedor de software específico para el volumen dado disponible, se selecciona.
3.  Si no hay ningún proveedor de hardware y no hay ningún proveedor de software específico para los volúmenes disponibles, se seleccionará el proveedor del sistema.

Sin embargo, un solicitante puede obtener información sobre los proveedores disponibles mediante [**IVssBackupComponents:: query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query). Con esta información, y solo si la aplicación de copia de seguridad tiene una buena comprensión de los distintos proveedores, un solicitante puede proporcionar un identificador de proveedor válido a [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).

Tenga en cuenta que no es necesario que todos los volúmenes tengan el mismo proveedor.

 

 




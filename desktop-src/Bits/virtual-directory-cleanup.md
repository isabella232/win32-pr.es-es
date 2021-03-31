---
title: Limpieza del directorio virtual
description: BITS extiende los directorios virtuales de IIS para admitir cargas.
ms.assetid: 8214904e-8a95-4c4b-a1c5-91e84031587f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fb689bb3c797a311ec7c2ef8134eb51ffd6f1a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995423"
---
# <a name="virtual-directory-cleanup"></a>Limpieza del directorio virtual

BITS extiende los directorios virtuales de IIS para admitir cargas. Cada directorio virtual tiene una propiedad de tiempo de espera de la sesión (la propiedad de la metabase [BITSSessionTimeout](bits-iis-extension-properties.md) de IIS) que especifica el período de tiempo en el que el cliente de bits debe realizar el progreso en la carga del archivo. Si no se realiza ningún progreso durante ese período (el temporizador se restablece cuando se realiza el progreso), BITS cierra la sesión. El tiempo de espera predeterminado de la sesión es de 14 días.

BITS agrega un elemento de trabajo a la [programador de tareas](/windows/desktop/TaskSchd/task-scheduler-start-page) para cada directorio virtual que se crea y se habilita. El elemento de trabajo elimina los recursos asociados con las sesiones cerradas. De forma predeterminada, la limpieza se produce cada 12 horas. Si dos directorios virtuales apuntan al mismo directorio físico, el proceso de limpieza Iniciado por uno de los directorios elimina los recursos asociados a todas las sesiones cerradas en el directorio físico.

Use la pestaña extensión BITS o las interfaces [programador de tareas](/windows/desktop/TaskSchd/task-scheduler-start-page) para cambiar la programación de limpieza según sea necesario para la aplicación. También puede llamar al método [**IBITSExtensionSetup:: GetCleanupTask**](/windows/desktop/api/Bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptask) para recuperar un puntero de interfaz a la tarea de limpieza asociada al directorio virtual.

> [!Note]  
> Si el Programador de tareas está deshabilitado después de que se haya habilitado el directorio virtual, el proceso de limpieza del directorio virtual no funcionará.

 

 

 
---
title: Limpieza de directorios virtuales
description: BITS amplía los directorios virtuales de IIS para admitir cargas.
ms.assetid: 8214904e-8a95-4c4b-a1c5-91e84031587f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ce883bbd9f1af31bc7cafb10a2484f3a56ecbcffa7917a5a0e491a38da4701b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118422196"
---
# <a name="virtual-directory-cleanup"></a>Limpieza de directorios virtuales

BITS amplía los directorios virtuales de IIS para admitir cargas. Cada directorio virtual tiene una propiedad de tiempo de espera de sesión (la propiedad de metabase [BITSSessionTimeout](bits-iis-extension-properties.md) de IIS) que especifica el período de tiempo en el que el cliente BITS debe avanzar en la carga del archivo. Si no se realiza ningún progreso durante ese período (el temporizador se restablece cuando se realiza el progreso), BITS cierra la sesión. El tiempo de espera predeterminado de la sesión es de 14 días.

BITS agrega un elemento de trabajo al [Programador de tareas](/windows/desktop/TaskSchd/task-scheduler-start-page) para cada directorio virtual que cree y habilite. El elemento de trabajo elimina los recursos asociados a las sesiones cerradas. De forma predeterminada, la limpieza se produce cada 12 horas. Si dos directorios virtuales apuntan al mismo directorio físico, el proceso de limpieza iniciado por uno de los directorios elimina los recursos asociados a todas las sesiones cerradas en el directorio físico.

Use la pestaña Extensión bits o las [interfaces Programador de tareas](/windows/desktop/TaskSchd/task-scheduler-start-page) para cambiar la programación de limpieza según corresponda para la aplicación. También puede llamar al método [**IBITSExtensionSetup::GetCleanupTask**](/windows/desktop/api/Bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptask) para recuperar un puntero de interfaz a la tarea de limpieza asociada al directorio virtual.

> [!Note]  
> Si el Programador de tareas está deshabilitado después de habilitar el directorio virtual, el proceso de limpieza del directorio virtual no funcionará.

 

 

 
---
description: El sistema Active Directory escritura no requiere ninguna acción especial durante las operaciones de copia de seguridad.
ms.assetid: 66efd5e5-e6c9-4179-b119-1b5b977b0f9f
title: Copia de seguridad y restauración de VSS Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d4441a05e06e67c23467887857a0f7bbcde73f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068548"
---
# <a name="vss-backup-and-restore-of-the-active-directory"></a>Copia de seguridad y restauración de VSS Active Directory

El sistema Active Directory escritura no requiere ninguna acción especial durante las operaciones de copia de seguridad. El sistema de escritura proporcionará al solicitante información sobre el componente y el conjunto de archivos, y el solicitante usa esa información para decidir qué archivos copiar en los medios de copia de seguridad. No es necesario usar ninguna API especial para realizar una copia de seguridad del Active Directory.

La forma en que se realiza una restauración depende de si el Active Directory se restaura como parte de una operación de recuperación ante desastres, o si la restauración se realiza en un sistema en el que se ejecuta el Active Directory. Además, la antigüedad de la copia de seguridad del estado Active Directory de copia de seguridad puede ser un problema debido a Active Directory lápidas.

## <a name="active-directory-restoration-following-disaster-recovery"></a>Active Directory restauración después de la recuperación ante desastres

Después de un bloqueo que requiere recuperación ante desastres, Active Directory se puede restaurar como parte de la restauración del estado del sistema operativo.

Esta operación de restauración es básicamente una restauración sin escritura.

## <a name="active-directory-restoration-on-the-system-where-it-is-running"></a>Active Directory restauración en el sistema donde se ejecuta

El sistema debe reiniciarse en modo de restauración de servicios de directorio si el Active Directory se está ejecutando actualmente en el servidor.

A continuación, el sistema operativo se ejecuta sin el Active Directory y toda la validación del usuario se produce a través del Administrador de cuentas de seguridad (SAM) en el registro. Solo el administrador tiene permiso para recuperar el Active Directory.

Una vez en el modo de restauración del servicio de directorio, una restauración de VSS puede continuar con normalidad. No hay ninguna razón para usar las API de win32 que no son de VSS Active Directory para restaurar el Active Directory estado.

## <a name="active-directory-restores-and-active-directory-tombstones"></a>Active Directory restauraciones y Active Directory de desecho

Cualquier plan de recuperación debe asegurarse de que la antigüedad de la copia de seguridad no debe superar el Active Directory de tombstone (el valor predeterminado es 60 días).

La restauración de una copia de seguridad anterior al elemento de desecho hará que un controlador de dominio tenga objetos que no se replican en los demás servidores.

Los objetos que no se replican no se eliminarán automáticamente en ese controlador de dominio (restaurado) porque los objetos de los objetos de las otras réplicas ya se han eliminado.

Un administrador tendrá que eliminar manualmente cada uno de los objetos del controlador de dominio restaurado que no se replican. No se admiten copias de Active Directory incrementales de la base de datos. Se requiere una copia de seguridad completa.

 

 




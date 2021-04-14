---
description: El escritor de Active Directory no requiere ninguna acción especial durante las operaciones de copia de seguridad.
ms.assetid: 66efd5e5-e6c9-4179-b119-1b5b977b0f9f
title: Copia de seguridad y restauración de VSS del Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d4441a05e06e67c23467887857a0f7bbcde73f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541747"
---
# <a name="vss-backup-and-restore-of-the-active-directory"></a>Copia de seguridad y restauración de VSS del Active Directory

El escritor de Active Directory no requiere ninguna acción especial durante las operaciones de copia de seguridad. El escritor proporcionará al solicitante la información del componente y del conjunto de archivos, y el solicitante usará esa información para decidir qué archivos copiar en el medio de copia de seguridad. No es necesario usar ninguna API especial para realizar una copia de seguridad del Active Directory.

La forma en que se realice una restauración dependerá de si el Active Directory se restaura como parte de una operación de recuperación ante desastres o de si la restauración se realiza en un sistema en el que se ejecuta la Active Directory. Además, la antigüedad de la copia de seguridad del estado Active Directory puede ser un problema debido a Active Directory marcadores de exclusión.

## <a name="active-directory-restoration-following-disaster-recovery"></a>Active Directory restauración después de la recuperación ante desastres

Tras un bloqueo que requiere recuperación ante desastres, el Active Directory se puede restaurar como parte de la restauración del estado del sistema operativo.

Esta operación de restauración es esencialmente una restauración sin escritor.

## <a name="active-directory-restoration-on-the-system-where-it-is-running"></a>Active Directory restauración en el sistema donde se está ejecutando

El sistema debe reiniciarse en el modo de restauración de servicios de directorio si el Active Directory se está ejecutando actualmente en el servidor.

Después, el sistema operativo se ejecutará sin el Active Directory y toda la validación del usuario se realizará a través del administrador de cuentas de seguridad (SAM) en el registro. Solo el administrador tiene permiso para recuperar el Active Directory.

Una vez en el modo de restauración del servicio de directorio, una restauración de VSS puede continuar con normalidad. No hay ninguna razón para usar las API de Active Directory de Win32 que no son de VSS para restaurar el estado de Active Directory.

## <a name="active-directory-restores-and-active-directory-tombstones"></a>Active Directory restaura y Active Directory marcadores de exclusión

Cualquier plan de recuperación debe asegurarse de que la antigüedad de la copia de seguridad no debe superar la duración del desecho Active Directory (el valor predeterminado es 60 días).

La restauración de una copia de seguridad anterior al objeto de desecho hará que un controlador de dominio tenga objetos que no se repliquen en los otros servidores.

Los objetos que no se replican no se eliminarán automáticamente en el controlador de dominio (restaurado), ya que los marcadores de exclusión de esos objetos en las otras réplicas ya se han eliminado.

Un administrador tendrá que eliminar manualmente cada uno de los objetos del controlador de dominio restaurado que no se repliquen. No se admiten copias de seguridad incrementales del Active Directory; se requiere una copia de seguridad completa.

 

 




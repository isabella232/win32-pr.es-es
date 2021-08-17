---
description: El sistema Active Directory escritura no requiere ninguna acción especial durante las operaciones de copia de seguridad.
ms.assetid: 66efd5e5-e6c9-4179-b119-1b5b977b0f9f
title: Copia de seguridad y restauración de VSS del Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8312e974d705cd193eaaecdaa163a2d408836aedfb14c21ff97f72486efbf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751488"
---
# <a name="vss-backup-and-restore-of-the-active-directory"></a>Copia de seguridad y restauración de VSS del Active Directory

El sistema Active Directory escritura no requiere ninguna acción especial durante las operaciones de copia de seguridad. El sistema de escritura proporcionará al solicitante información sobre el componente y el conjunto de archivos, y el solicitante usa esa información para decidir qué archivos copiar en los medios de copia de seguridad. No es necesario usar ninguna API especial para realizar una copia de seguridad del Active Directory.

La forma en que se realiza una restauración depende de si el Active Directory se restaura como parte de una operación de recuperación ante desastres, o si la restauración se realiza en un sistema en el que se ejecuta Active Directory la copia de seguridad. Además, la antigüedad de la copia de seguridad del Active Directory estado puede ser un problema debido a Active Directory de desecho.

## <a name="active-directory-restoration-following-disaster-recovery"></a>Active Directory restauración después de la recuperación ante desastres

Después de un bloqueo que requiere recuperación ante desastres, el Active Directory se puede restaurar como parte de la restauración del estado del sistema operativo.

Esta operación de restauración es básicamente una restauración sin escritura.

## <a name="active-directory-restoration-on-the-system-where-it-is-running"></a>Active Directory restauración en el sistema donde se está ejecutando

El sistema debe reiniciarse en modo de restauración de servicios de directorio si el Active Directory se está ejecutando actualmente en el servidor.

A continuación, el sistema operativo se ejecuta sin la Active Directory y toda la validación del usuario se produce a través del Administrador de cuentas de seguridad (SAM) en el Registro. Solo el administrador tiene permiso para recuperar el Active Directory.

Una vez en el modo de restauración del servicio de directorio, una restauración de VSS puede continuar con normalidad. No hay ninguna razón para usar las API de win32 que no son de VSS Active Directory restaurar el Active Directory estado.

## <a name="active-directory-restores-and-active-directory-tombstones"></a>Active Directory restauraciones y Active Directory de desecho

Cualquier plan de recuperación debe asegurarse de que la antigüedad de la copia de seguridad no debe superar el Active Directory de tombstone (el valor predeterminado es 60 días).

La restauración de una copia de seguridad anterior al lápido hará que un controlador de dominio tenga objetos que no se replican en los demás servidores.

Los objetos que no se replican no se eliminarán automáticamente en ese controlador de dominio (restaurado) porque ya se han eliminado los elementos de eliminación de esos objetos en las otras réplicas.

Un administrador tendrá que eliminar manualmente cada uno de los objetos del controlador de dominio restaurado que no se replican. No se admiten las copias Active Directory incrementales de la base de datos. Se requiere una copia de seguridad completa.

 

 




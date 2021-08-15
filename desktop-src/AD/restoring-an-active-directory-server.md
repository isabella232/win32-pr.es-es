---
title: Restaurar un servidor Active Directory servidor
description: Active Directory deben restaurarse sin conexión.
ms.assetid: 91fbbdc1-0e84-4b89-8a38-4c8d0268992b
ms.tgt_platform: multiple
keywords:
- Restaurar Active Directory Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 865389b4ad80ad8c3009a86a881ff4cf291a4fc1b4606e78e8ecd01ceef7c893
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184298"
---
# <a name="restoring-an-active-directory-server"></a>Restaurar un servidor Active Directory servidor

Active Directory deben restaurarse sin conexión. El sistema debe reiniciarse en modo de restauración de servicios de directorio. En este modo, el sistema operativo se ejecuta sin Active Directory Domain Services y toda la validación del usuario se produce a través del Administrador de cuentas de seguridad (SAM) en el Registro. Para restaurar Active Directory Domain Services, use las credenciales de un administrador local en el controlador de dominio que se restaura.

El llamador de las funciones de restauración debe tener el **SE de acceso RESTORE \_ \_ NAME.** Use la [**función DsSetAuthIdentity para**](dssetauthidentity.md) establecer el contexto de seguridad en el que se llama a las funciones de copia de seguridad y restauración de directorios.

Tenga en cuenta que al restaurar Active Directory Domain Services, también debe restaurar los demás componentes de estado del sistema.

**Para restaurar Active Directory Domain Services**

1.  Llame a [**la función DsIsNTDSOnline**](dsisntdsonline.md) para determinar si Active Directory Domain Services se están ejecutando.
2.  Si Active Directory Domain Services en ejecución, se llama a la función [**DsRestorePrepare**](dsrestoreprepare.md) para inicializar la operación de restauración y obtener un identificador de contexto de copia de seguridad. Si Active Directory Domain Services en ejecución, no se puede restaurar y la aplicación de restauración debe producir un error en la operación de restauración. La **función DsRestorePrepare** requiere que el token de expiración se obtenga de la función [**DsBackupPrepare**](dsbackupprepare.md) durante la operación de copia de seguridad.
3.  Llame a [**la función DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) para determinar los directorios donde se van a restaurar los archivos. Si se produce un error en esta función, restaure los datos al directorio de origen de copia de seguridad original; que es el directorio desde el que se ha hecho una copia de seguridad de los datos.
4.  Llame a [**la función DsRestoreRegister**](dsrestoreregister.md) para preparar el servidor Active Directory para la operación de restauración y bloquear los directorios de restauración.
5.  Use las funciones estándar de Win32 para restaurar los archivos. En primer lugar, elimine todos los archivos del directorio de destino; a continuación, copie los archivos de copia de seguridad en el directorio de destino.
6.  Llame a [**la función DsRestoreRegisterComplete**](dsrestoreregistercomplete.md) para indicar que la restauración se ha completado.
7.  Llame a [**la función DsRestoreEnd**](dsrestoreend.md) para liberar los recursos asociados al contexto.

Después de una restauración en modo de restauración de Servicios de directorio, el controlador de dominio debe reiniciarse en modo normal. Cuando se inicia el servicio de directorio, el controlador de dominio realizará la comprobación de coherencia normal y el directorio restaurado estará en línea.

Tenga en cuenta que la restauración de Active Directory servidor es siempre una operación de dos partes. En primer lugar, restaure la base de datos a una hora en la que se haya realizado la copia de seguridad. En segundo lugar, replique el directorio, donde la DSA recién restaurada replica las actualizaciones posteriores a la copia de seguridad de otras DSA en el dominio y el bosque empresarial.

Un equipo que se ejecuta en Windows 2000 o Windows Server 2003, que contiene una réplica del servicio de directorio, es un controlador de dominio.

La [**función DsRestoreRegister**](dsrestoreregister.md) agrega datos al registro que deben sobrevivir al proceso de restauración del Registro para que la restauración funcione correctamente. Para asegurarse de que se conservan estos datos del Registro, restaure Active Directory Domain Services con las funciones **DsRestore \** _ antes de reiniciar el equipo después de llamar a la función [_ *RegReplaceKey.* *](/windows/desktop/api/winreg/nf-winreg-regreplacekeya) Este proceso funciona porque **RegReplaceKey** no reemplaza realmente el subárbol del Registro hasta que se reinicia el equipo y los datos del Registro agregados por la función **DsRestoreRegister** se excluyen específicamente de ser reemplazados durante una operación de restauración del Registro.

 

 
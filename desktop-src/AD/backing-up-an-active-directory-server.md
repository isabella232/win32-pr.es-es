---
title: Copia de seguridad de un servidor Active Directory
description: Una copia de seguridad de Active Directory Server requiere que realice una copia de seguridad de la base de datos y los registros de transacciones. En este tema se proporciona un tutorial sobre cómo una aplicación de copia de seguridad hace una copia de seguridad del servicio de directorio de Active Directory.
ms.assetid: 250b2f40-6d43-4aa5-a588-b0cd4839828d
ms.tgt_platform: multiple
keywords:
- copia de seguridad de Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5affde952ee543afe1bb9b794cce074a74382aa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075023"
---
# <a name="backing-up-an-active-directory-server"></a>Copia de seguridad de un servidor Active Directory

Una copia de seguridad de Active Directory Server requiere que realice una copia de seguridad de la base de datos y los registros de transacciones. En este tema se proporciona un tutorial sobre cómo una aplicación de copia de seguridad hace una copia de seguridad del servicio de directorio de Active Directory.

El autor de la llamada de estas funciones de copia de seguridad debe tener el privilegio de **\_ \_ nombre de copia de seguridad** de. Puede usar la función [**DsSetAuthIdentity**](dssetauthidentity.md) para establecer el contexto de seguridad en el que se llama a las funciones de copia de seguridad y restauración de directorios.

**Para realizar una copia de seguridad de un servidor de Active Directory, realice los pasos siguientes:**

1.  Llame a la función [**DsIsNTDSOnline**](dsisntdsonline.md) para determinar si Active Directory Domain Services se están ejecutando.
2.  Si Active Directory Domain Services se están ejecutando, llame a la función [**DsBackupPrepare**](dsbackupprepare.md) para inicializar un identificador de contexto de copia de seguridad. Si Active Directory Domain Services no se están ejecutando, no se puede realizar una copia de seguridad y la aplicación de copia de seguridad no debe realizar la operación de copia de seguridad.
3.  Llame a la función [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) para obtener una lista de archivos de los que se va a realizar la copia de seguridad. Para liberar la memoria devuelta por esta función, llame a la función [**DsBackupFree**](dsbackupfree.md) .
4.  Para cada nombre de la lista de archivos devuelta, llame a la función [**DsBackupOpenFile**](dsbackupopenfile.md) seguida de llamadas repetidas a la función [**DsBackupRead**](dsbackupread.md) hasta que se haya leído todo el archivo. Cuando haya terminado de leer el archivo, llame a la función [**DsBackupClose**](dsbackupclose.md) para cerrarlo.
5.  Una vez que haya realizado una copia de seguridad de todos los archivos de base de datos, llame a la función [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) para obtener una lista de registros de transacciones. Esta lista se trata como la lista de archivos de base de datos.
6.  Cuando haya terminado de realizar la copia de seguridad del registro de transacciones, llame a la función [**DsBackupTruncateLogs**](dsbackuptruncatelogs.md) para eliminar todos los registros de transacciones confirmados de los que se realizó una copia de seguridad.
7.  Guarde el contenido del token de expiración proporcionado por la función [**DsBackupPrepare**](dsbackupprepare.md) . Se puede guardar en un archivo o en otra memoria persistente. Este token se debe pasar a la función [**DsRestorePrepare**](dsrestoreprepare.md) para iniciar una operación de restauración.
8.  Libere la memoria para el token de expiración pasando el puntero de token a la función [**DsBackupFree**](dsbackupfree.md) .
9.  Por último, llame a la función [**DsBackupEnd**](dsbackupend.md) para liberar todos los recursos asociados al identificador de contexto de copia de seguridad.

 

 





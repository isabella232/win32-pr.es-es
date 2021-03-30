---
description: Los escritores de aplicaciones pueden realizar cambios leves en el código fuente para agregar operaciones del registro y archivos de transacciones mediante el administrador de transacciones de kernel (KTM).
ms.assetid: 356c66dc-5ddd-472f-835c-2e2cb019bcfd
title: Trabajar con transacciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 255e40fb38ca4bfb24acdce717f133dbcf0c76f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910390"
---
# <a name="working-with-transactions"></a>Trabajar con transacciones

Los escritores de aplicaciones pueden realizar cambios leves en el código fuente para agregar operaciones del registro y archivos de transacciones mediante el administrador de transacciones de kernel (KTM). Normalmente, esto implica la creación de una transacción y el paso del identificador a otras funciones proporcionadas por recursos transaccionales como [NTFS transaccional](/windows/desktop/FileIO/transactional-ntfs-portal) y el registro de transacción.

KTM proporciona mecanismos para que la aplicación participe en las transacciones, así como para escribir su propio administrador de recursos transaccional. Hay funciones que permiten crear, administrar y trabajar con cuatro clases de objetos de kernel: transacciones, administradores de transacciones, administradores de recursos e inscritos. Si simplemente usa transacciones, solo necesita trabajar con objetos de transacción y usar estas funciones:

-   [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)
-   [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)
-   [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)

Nunca suponga que una transacción está activa. Las transacciones se pueden revertir por muchos motivos y en cualquier momento.

Windows expone una interfaz basada en identificador a los recursos del sistema. Para trabajar con un objeto de sistema operativo, la aplicación solicita primero un identificador al objeto y, a continuación, usa este controlador en las siguientes llamadas de función para obtener acceso al objeto o modificarlo. Normalmente, un identificador se puede abrir en modos diferentes; el modo especificado afecta a la semántica de las llamadas de función subsiguientes. Por ejemplo, un identificador de archivo que se abre mediante una llamada a [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) con la marca *dwDesiredAccess* establecida **en \_ Read genérico** no se puede utilizar en llamadas que modifican el archivo.

Puede coordinar con [Coordinador de transacciones distribuidas](/previous-versions/windows/desktop/ms684146(v=vs.85)) recursos de modo de usuario como SQL o MSMQ y con recursos de modo kernel que usan el KTM. En primer lugar, cree una transacción DTC o un objeto [**System. Transactions**](/dotnet/api/system.transactions?view=dotnet-plat-ext-3.1) y, a continuación, llame al objeto [**IKernelTransaction**](/previous-versions/windows/desktop/aa344210(v=vs.85)) , desde el que puede obtener el identificador KTM. El objeto **IKernelTransaction** crea una transacción de KTM que está subordinada a la transacción DTC. Con este identificador, puede crear los objetos de transacción, pero indicar el resultado de la transacción mediante DTC o **System. Transactions**.

 

 

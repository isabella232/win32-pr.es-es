---
description: Los escritores de aplicaciones pueden realizar pequeños cambios en el código fuente para agregar operaciones de registro y archivo con transacciones mediante el Administrador de transacciones de kernel (KTM).
ms.assetid: 356c66dc-5ddd-472f-835c-2e2cb019bcfd
title: Trabajar con transacciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 255e40fb38ca4bfb24acdce717f133dbcf0c76f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160025"
---
# <a name="working-with-transactions"></a>Trabajar con transacciones

Los escritores de aplicaciones pueden realizar pequeños cambios en el código fuente para agregar operaciones de registro y archivo con transacciones mediante el Administrador de transacciones de kernel (KTM). Normalmente, esto implicará crear una transacción y pasar el identificador a otras funciones proporcionadas por recursos transaccionales, como [NTFS transaccional](/windows/desktop/FileIO/transactional-ntfs-portal) y el Registro de transacciones.

KTM proporciona mecanismos para que la aplicación participe en transacciones, así como para escribir su propio administrador de recursos transaccional. Hay funciones que permiten crear, administrar y trabajar con cuatro clases de objetos de kernel: transacciones, administradores de transacciones, administradores de recursos y inselecciones. Si simplemente usa transacciones, solo tiene que trabajar con objetos de transacción y usar estas funciones:

-   [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)
-   [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)
-   [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)

Nunca suponga que una transacción está activa. Las transacciones se pueden revertir por muchos motivos y en cualquier momento.

Windows expone una interfaz basada en identificadores a los recursos del sistema. Para trabajar con un objeto de sistema operativo, la aplicación solicita primero un identificador al objeto y, a continuación, usa este identificador en las llamadas de función posteriores para acceder al objeto o modificarlo. Normalmente, un identificador se puede abrir en distintos modos; el modo especificado afecta a la semántica de las llamadas de función posteriores. Por ejemplo, un identificador de archivo que se abre mediante una llamada a [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) con la marca *dwDesiredAccess* establecida en **GENERIC \_ READ** no se puede usar en las llamadas que modifican el archivo.

Puede coordinarse con [Coordinador de transacciones distribuidas](/previous-versions/windows/desktop/ms684146(v=vs.85)) en modo de usuario, como SQL o MSMQ, y con recursos en modo kernel que usan KTM. En primer lugar, cree una transacción DTC o un objeto [**System.Transactions**](/dotnet/api/system.transactions?view=dotnet-plat-ext-3.1) y, a continuación, llame al objeto [**IKernelTransaction,**](/previous-versions/windows/desktop/aa344210(v=vs.85)) del que puede obtener el identificador KTM. El **objeto IKernelTransaction** crea una transacción KTM que está subordinada a la transacción DTC. Con este identificador, puede crear los objetos de transacción, pero indicar el resultado de la transacción mediante DTC o **System.Transactions**.

 

 

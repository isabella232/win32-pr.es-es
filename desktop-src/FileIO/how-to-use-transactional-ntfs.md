---
description: Administrar identificadores de archivos de transacciones en NTFS transaccional.
ms.assetid: 29879a3f-14b4-462c-a001-46c3c3eb74d1
title: Cómo usar NTFS transaccional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43681f0d5b27f0db03d8b6c44564b792fce4b467
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688463"
---
# <a name="how-to-use-transactional-ntfs"></a>Cómo usar NTFS transaccional

## <a name="transacted-file-handles"></a>Identificadores de archivo de transacción

NTFS transaccional (TxF) enlaza un identificador de archivo a una transacción. En el caso de las operaciones que funcionan en un identificador (por ejemplo, las funciones [**readfile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) y [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) ), la llamada de función de API real no cambia. En el caso de las operaciones de archivo que toman un nombre, existen funciones de transacción explícitas para estas operaciones. Por ejemplo, en lugar de llamar a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), llame a [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda). Esto crea un identificador de archivo de transacción, que se puede usar para todas las operaciones de archivo que requieren un identificador. Todas las operaciones posteriores que usan este identificador son operaciones de transacción.

## <a name="basic-txf-usage"></a>Uso básico de TxF

La siguiente serie de pasos representa el uso más básico de TxF. También se admiten escenarios más complejos, a discreción del diseñador de aplicaciones.

1.  Cree una transacción mediante una llamada a la función KTM [**CreateTransaction**](/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction) o mediante la interfaz **IKernelTransaction** del [Coordinador de transacciones distribuidas](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator) (DTC).
2.  Obtiene los identificadores de archivo de transacción llamando a [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda).
3.  Modifique los archivos según sea necesario con los identificadores de archivo de transacción.
4.  Cierre todos los identificadores de archivo de transacciones asociados a la transacción creada en el paso 1.
5.  Confirme o anule la transacción mediante una llamada a la función KTM o DTC correspondiente.

## <a name="key-points-of-the-txf-programming-model"></a>Puntos clave del modelo de programación de TxF

El modelo de programación TxF tiene los siguientes puntos clave que se deben tener en cuenta al desarrollar una aplicación TxF:

-   Se recomienda encarecidamente que una aplicación cierre todos los identificadores de archivo de transacción antes de confirmar o revertir una transacción. El sistema invalida todos los identificadores de transacciones cuando finaliza una transacción. Cualquier operación, excepto Close, realizada en un identificador de transacción después de que finalice la transacción devuelve el siguiente error: el **identificador de error ya \_ \_ no \_ \_ es válido**.
-   Un archivo se ve como una unidad de almacenamiento. Se admiten las actualizaciones parciales y las sobrescrituras de archivos completadas. Varias transacciones no pueden modificar simultáneamente el mismo archivo.
-   La e/s asignada a la memoria es transparente y coherente con la e/s de archivos normal. Una aplicación debe vaciar y cerrar una sección abierta antes de confirmar una transacción. Si no lo hace, pueden producirse cambios parciales en el archivo asignado dentro de la transacción. Si no se hace, se produce un error en la reversión.

## <a name="common-programming-errors"></a>Errores comunes de programación

Pueden producirse los siguientes errores comunes al desarrollar aplicaciones con transacciones:

-   Usar un identificador de archivo una vez completada una transacción.
-   No se pueden cerrar los identificadores de los archivos y directorios eliminados antes de confirmar una transacción, lo que impedirá que se produzcan las operaciones de eliminación. Este evento se debe producir antes de realizar la confirmación para que la operación de eliminación se considere parte de la transacción. Esto se debe a que el sistema no elimina realmente un archivo hasta que se cierra el último identificador, incluso cuando la operación no se ha realizado con transacciones, como parte del subsistema de e/s de archivos de Windows.
-   No se tienen en cuenta las reversiones de transacciones iniciadas por el sistema, que pueden producirse en cualquier momento; por ejemplo, una transacción se revierte si se agotan los recursos del sistema.

 

 

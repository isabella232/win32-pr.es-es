---
description: Administración de identificadores de archivos con transacciones en NTFS transaccional.
ms.assetid: 29879a3f-14b4-462c-a001-46c3c3eb74d1
title: Uso de NTFS transaccional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43681f0d5b27f0db03d8b6c44564b792fce4b467
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069928"
---
# <a name="how-to-use-transactional-ntfs"></a>Uso de NTFS transaccional

## <a name="transacted-file-handles"></a>Identificadores de archivo con transacciones

NTFS transaccional (TxF) enlaza un identificador de archivo a una transacción. Para las operaciones que funcionan en un identificador (por ejemplo, las funciones [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) y [**WriteFile),**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) la llamada a función de API real no cambia. Para las operaciones de archivo que toman un nombre, hay funciones de transacción explícitas para estas operaciones. Por ejemplo, en lugar de llamar [**a CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), llame a [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda). Esto crea un identificador de archivo con transacciones, que se puede usar para todas las operaciones de archivo que requieren un identificador. Todas las operaciones posteriores que usan este identificador son operaciones de transacción.

## <a name="basic-txf-usage"></a>Uso básico de TxF

La siguiente serie de pasos representa el uso más básico de TxF. También se admiten escenarios más complejos, a discreción del diseñador de aplicaciones.

1.  Cree una transacción llamando a la función [**KTM CreateTransaction**](/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction) o mediante la **interfaz IKernelTransaction** del Coordinador de transacciones distribuidas (DTC). [](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator)
2.  Obtenga identificadores de archivo con transacciones llamando a [**CreateFileTransacted.**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
3.  Modifique los archivos según sea necesario mediante los identificadores de archivo con transacciones.
4.  Cierre todos los identificadores de archivo con transacción asociados a la transacción creada en el paso 1.
5.  Confirme o anule la transacción llamando a la función KTM o DTC correspondiente.

## <a name="key-points-of-the-txf-programming-model"></a>Puntos clave del modelo de programación TxF

El modelo de programación TxF tiene los siguientes puntos clave que debe tener en cuenta al desarrollar una aplicación TxF:

-   Se recomienda encarecidamente que una aplicación cierre todos los identificadores de archivos con transacciones antes de confirmar o revertir una transacción. El sistema invalida todos los identificadores de transacción cuando finaliza una transacción. Cualquier operación, excepto close, realizada en un identificador de transacción una vez que finaliza la transacción devuelve el siguiente error: **ERROR HANDLE NO LONGER \_ \_ \_ \_ VALID**.
-   Un archivo se ve como una unidad de almacenamiento. Se admiten actualizaciones parciales y sobrescrituras de archivos completas. Varias transacciones no pueden modificar simultáneamente el mismo archivo.
-   La E/S asignada a memoria es transparente y coherente con la E/S de archivo normal. Una aplicación debe vaciar y cerrar una sección abierta antes de confirmar una transacción. Si no lo hace, puede producir cambios parciales en el archivo asignado dentro de la transacción. Se produce un error en una reversión si no se hace.

## <a name="common-programming-errors"></a>Errores comunes de programación

Pueden producirse los siguientes errores comunes al desarrollar aplicaciones con transacciones:

-   Usar un identificador de archivo una vez completada una transacción.
-   No se pueden cerrar los identificadores de los archivos y directorios eliminados antes de confirmar una transacción, lo que impedirá que se produzcan las operaciones de eliminación. Este evento debe producirse antes de realizar la confirmación para que la operación de eliminación se considere parte de la transacción. Esto se debe a que el sistema no elimina realmente un archivo hasta que se cierra el último identificador, incluso cuando la operación no se realiza, como parte del subsistema de E/S de Windows archivo.
-   No se puede tener en cuenta la reversión de transacciones iniciadas por el sistema, lo que puede ocurrir en cualquier momento. Por ejemplo, se revierte una transacción si se agotan los recursos del sistema.

 

 

---
description: Use NTFS transaccional para mantener la integridad de los datos.
ms.assetid: 886d6075-57e8-47db-aec5-77660d0a53f9
title: Cuándo usar NTFS transaccional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022f7a67fe6960a8754f768956457afbd04a509bbf9a3c18360b4651e4d9ccda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830135"
---
# <a name="when-to-use-transactional-ntfs"></a>Cuándo usar NTFS transaccional

Una aplicación puede usar NTFS transaccional (TxF) para conservar la integridad de los datos en el disco durante condiciones de error inesperadas. En general, una aplicación debe considerar el uso de TxF si la aplicación vacíe archivos y use otras técnicas para mantener la integridad de los datos. TxF puede funcionar mejor y simplificar el código de control de errores de la aplicación a la vez que mejora la confiabilidad y la recuperación de errores. En las secciones siguientes de este tema se proporcionan ejemplos de escenarios para usar TxF.

## <a name="updating-a-file"></a>Actualizar un archivo

La actualización de un archivo es una operación común y normalmente sencilla. Sin embargo, si se produce un error en el sistema o la aplicación mientras una aplicación actualiza información en un disco, el resultado puede ser catastrófico, ya que los datos del usuario pueden estar dañados por una operación de actualización de archivos que se ha completado parcialmente. Las aplicaciones sólidas a menudo realizan secuencias complejas de copias de archivos y nombres de archivo para asegurarse de que los datos no se dañan si se produce un error en un sistema.

TxF facilita que una aplicación proteja las operaciones de actualización de archivos frente a errores del sistema o de la aplicación. Para actualizar un archivo de forma segura, la aplicación abre el archivo en modo de transacción, realiza las actualizaciones necesarias y, a continuación, confirma la transacción. Si se produce un error en el sistema o la aplicación durante la actualización de archivos, TxF restaura automáticamente el archivo al estado que tenía antes de que se iniciara la actualización de archivos, lo que evita daños en los archivos.

## <a name="multi-file-updates"></a>Actualizaciones de varios archivos

TxF es incluso más importante cuando una sola operación lógica afecta a varios archivos. Por ejemplo, si desea usar una herramienta para cambiar el nombre de una de las páginas HTML o ASP de un sitio web, una herramienta bien diseñada también corregiría todos los vínculos para usar el nuevo nombre de archivo. Sin embargo, un error durante esta operación deja el sitio web en un estado incoherente, con algunos de los vínculos que siguen haciendo referencia al nombre de archivo antiguo. Al convertir la operación de cambio de nombre de archivo y la operación de corrección de vínculos en una sola transacción, TxF garantiza que el cambio de nombre de archivo y la corrección del vínculo se realizarán correctamente o se producirán errores como una sola operación.

## <a name="consistent-concurrent-updates"></a>Actualizaciones simultáneas coherentes

TxF aísla las transacciones simultáneas. Si una aplicación abre un archivo para una lectura transaccional mientras otra aplicación tiene el mismo archivo abierto para una actualización transaccional, TxF aísla los efectos de las dos transacciones entre sí. En otras palabras, el lector transaccional siempre ve una versión única y coherente del archivo, aunque ese archivo esté en proceso de ser actualizado por otra transacción.

Una aplicación puede usar esta funcionalidad para permitir a los clientes ver archivos mientras otros clientes hacen actualizaciones. Por ejemplo, un servidor web transaccional puede proporcionar una vista única y coherente de los archivos, mientras que otra herramienta actualiza simultáneamente esos archivos.

> [!Note]  
> TxF no admite actualizaciones simultáneas de varios escritores en transacciones diferentes. TxF solo admite un único escritor con varios lectores simultáneos y coherentes.

 

## <a name="coordinating-with-other-transacted-resource-managers"></a>Coordinación con otros administradores de recursos con transacciones

Las transacciones usadas con sistemas de archivos con transacciones también se pueden usar con el registro de transacciones. Las actualizaciones del archivo y del Registro se coordinan con una única transacción.

Mediante el [Coordinador de transacciones distribuidas](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator) (DTC) o System.Transactions, las actualizaciones realizadas en SQL, MSMQ y otros recursos transaccionales se pueden coordinar con actualizaciones de archivos con transacciones. Para obtener más información, vea [IKernelTransaction](/previous-versions/windows/desktop/aa344210(v=vs.85))de DTC.

## <a name="unsupported-scenarios"></a>Escenarios no admitidos

TxF no admite los siguientes escenarios de transacción:

-   Transacciones en volúmenes de red, por ejemplo, en recursos compartidos de archivos. Los protocolos CIFS/SMB no admiten TxF.
-   Transacciones en cualquier sistema de archivos que no sea NTFS.
-   Operaciones de transacción en archivos almacenados en caché mediante el almacenamiento en caché del lado cliente.
-   Acceso a archivos mediante los iDs de objeto.
-   Cualquier escenario de escritor compartido.
-   Cualquier situación en la que un archivo se abra durante un período prolongado de tiempo (días o semanas).

 

 

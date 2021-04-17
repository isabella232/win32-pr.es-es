---
description: Utilice NTFS transaccional para mantener la integridad de los datos.
ms.assetid: 886d6075-57e8-47db-aec5-77660d0a53f9
title: Cuándo usar NTFS transaccional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28c0a134a8cb5824337022fedf14fe3db3c6f76c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667690"
---
# <a name="when-to-use-transactional-ntfs"></a>Cuándo usar NTFS transaccional

Una aplicación puede usar NTFS transaccional (TxF) para conservar la integridad de los datos en el disco durante las condiciones de error inesperadas. En general, una aplicación debería considerar el uso de TxF si la aplicación está vaciando archivos y utiliza otras técnicas para mantener la integridad de los datos. TxF puede mejorar y simplificar el código de control de errores de la aplicación a la vez que mejora la confiabilidad y la recuperación de errores. En las siguientes secciones de este tema se proporcionan ejemplos de escenarios para usar TxF.

## <a name="updating-a-file"></a>Actualización de un archivo

La actualización de un archivo es una operación común y normalmente simple. Sin embargo, si se produce un error en el sistema o la aplicación mientras una aplicación actualiza la información de un disco, el resultado puede ser catastrófico, ya que los datos de usuario pueden estar dañados mediante una operación de actualización de archivos que se ha completado parcialmente. Las aplicaciones sólidas a menudo realizan secuencias complejas de copias de archivos y de cambio de nombre para garantizar que los datos no están dañados si se produce un error en un sistema.

TxF facilita a una aplicación la protección de las operaciones de actualización de archivos del error del sistema o de la aplicación. Para actualizar un archivo de forma segura, la aplicación abre el archivo en modo de transacción, realiza las actualizaciones necesarias y, a continuación, confirma la transacción. Si se produce un error en el sistema o la aplicación durante la actualización del archivo, TxF restaura automáticamente el archivo al estado que tenía antes de que comenzara la actualización del archivo, lo que evita daños en los archivos.

## <a name="multi-file-updates"></a>Actualizaciones de varios archivos

TxF es aún más importante cuando una única operación lógica afecta a varios archivos. Por ejemplo, si desea utilizar una herramienta para cambiar el nombre de una de las páginas HTML o ASP de un sitio web, una herramienta bien diseñada también corregiría todos los vínculos para usar el nuevo nombre de archivo. Sin embargo, un error durante esta operación deja el sitio web en un estado incoherente, con algunos de los vínculos que siguen haciendo referencia al nombre de archivo antiguo. Al hacer que la operación de cambio de nombre del archivo y la operación de corrección de vínculos se realicen en una sola transacción, TxF garantiza que la corrección del vínculo y el cambio de nombre del archivo se realiza correctamente o no como una sola operación.

## <a name="consistent-concurrent-updates"></a>Actualizaciones simultáneas coherentes

TxF aísla las transacciones simultáneas. Si una aplicación abre un archivo para una lectura transaccional mientras otra aplicación tiene el mismo archivo abierto para una actualización transaccional, el TxF aísla los efectos de las dos transacciones entre sí. En otras palabras, el lector transaccional siempre ve una única versión coherente del archivo, incluso mientras el archivo está en proceso de ser actualizado por otra transacción.

Una aplicación puede usar esta funcionalidad para que los clientes puedan ver los archivos mientras otros clientes realizan actualizaciones. Por ejemplo, un servidor web transaccional puede proporcionar una vista única y coherente de los archivos mientras otra herramienta los actualiza simultáneamente.

> [!Note]  
> TxF no admite actualizaciones simultáneas por varios escritores en transacciones diferentes. TxF solo admite un único escritor con varios lectores simultáneos y coherentes.

 

## <a name="coordinating-with-other-transacted-resource-managers"></a>Coordinación con otros administradores de recursos con transacciones

Las transacciones que se usan con sistemas de archivos de transacciones también se pueden usar con el registro de transacciones. Las actualizaciones del archivo y del registro se coordinan con una sola transacción.

Mediante el uso de transacciones de [Coordinador de transacciones distribuidas](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator) (DTC) o System. Transactions, las actualizaciones realizadas en SQL, MSMQ y otros recursos transaccionales se pueden coordinar con las actualizaciones de archivos de transacciones. Para obtener más información, vea [IKernelTransaction](/previous-versions/windows/desktop/aa344210(v=vs.85))de DTC.

## <a name="unsupported-scenarios"></a>Escenarios no admitidos

TxF no admite los siguientes escenarios de transacción:

-   Transacciones en volúmenes de red, por ejemplo, en recursos compartidos de archivos. TxF no es compatible con los protocolos CIFS/SMB.
-   Transacciones en cualquier sistema de archivos distinto de NTFS.
-   Operaciones de transacción en los archivos almacenados en caché del lado cliente.
-   Acceso a archivos con identificadores de objeto.
-   Cualquier escenario de escritor compartido.
-   Cualquier situación en la que un archivo se abre durante un período de tiempo prolongado (días o semanas).

 

 

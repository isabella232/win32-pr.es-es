---
title: Interfaces DO
description: Utilice las siguientes interfaces de optimización de entrega (DO) para transferir archivos y supervisar trabajos en la cola de transferencia.
ms.assetid: 20203CCD-86CC-4551-BA4F-0A5999F8C956
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0359328f189c1a5b5d9649d8300dc59a80df4480
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695638"
---
# <a name="do-interfaces"></a>Interfaces DO

Utilice las siguientes interfaces de optimización de entrega (DO) para transferir archivos y supervisar trabajos en la cola de transferencia.

| Interfaz | Descripción |
|-|-|
| [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) | Los clientes implementan la interfaz [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) para recibir la notificación de que un trabajo se ha completado, se ha modificado o tiene un error. |
| [**IBackgroundCopyError**](ibackgroundcopyerror.md) | Recupera los detalles de un error de trabajo. |
| [**IBackgroundCopyFile**](ibackgroundcopyfile.md) | Recupera los nombres de archivo local y remoto de una solicitud de transferencia de archivos en el trabajo y su progreso. |
| [**IBackgroundCopyFile2**](ibackgroundcopyfile2.md) | Especifica un nuevo nombre remoto para el archivo y recupera la lista de intervalos que se van a descargar. |
| [**IBackgroundCopyFile5**](ibackgroundcopyfile5.md) | Proporciona métodos GET y set de propiedad genéricos para las propiedades BackgroundCopyFile. |
| [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) | Agrega archivos al trabajo, establece el nivel de prioridad del trabajo, determina el estado del trabajo e inicia y detiene el trabajo. |
| [**IBackgroundCopyJob5**](ibackgroundcopyjob5.md) | Consulta o establece varios comportamientos opcionales de un trabajo. |
| [**IBackgroundCopyManager**](ibackgroundcopymanager.md) | Crea trabajos de transferencia, recupera un objeto de enumerador de trabajos en la cola y recupera trabajos individuales de la cola. |
| [**IDeliveryOptimizationJob**](ideliveryoptimizationjob.md) | Use para descargar intervalos de un archivo. |
| [**IDeliveryOptimizationFile**](ideliveryoptimizationfile.md) | Se usa para identificar el estado de un archivo específico. |
| [**IDODownload**](./do/nn-do-idodownload.md) | Se usa para iniciar y administrar una descarga. |
| [**IDODownloadInternal**](./dodownloadinternal/nn-dodownloadinternal-idodownloadinternal.md) | Se usa para obtener o establecer las propiedades de descarga extendida. |
| [**IDODownloadStatusCallback**](./do/nn-do-idodownloadstatuscallback.md) | Se usa para recibir notificaciones sobre una descarga. |
| [**IDOManager**](./do/nn-do-idomanager.md) | Se usa para crear una nueva descarga y para enumerar las descargas existentes. |
| [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) | Enumera los archivos del trabajo. |
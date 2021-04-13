---
description: Para habilitar la transferencia de archivos de aplicación, COMREPL administra automáticamente los conjuntos de carpetas del sistema de archivos en el origen y el destino. Todas estas carpetas COMREPL tienen la raíz en% systemdir% de la \\ \\ replicación com.
ms.assetid: 8c59577b-34ea-4675-aaea-a2732fd5ce14
title: Administración de archivos (servicios de componentes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e785b8fd39d94bcf623810bca950862d22ec8762
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538722"
---
# <a name="file-management"></a>Administración de archivos

Para habilitar la transferencia de archivos de aplicación, COMREPL administra automáticamente los conjuntos de carpetas del sistema de archivos en el origen y el destino. Todas estas carpetas COMREPL tienen la raíz en% systemdir% de la \\ \\ replicación com.

## <a name="source-folders"></a>Carpetas de origen



| Carpeta                   | Propósito                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReplicaSource<br/> | Las aplicaciones exportadas durante la fase de preparación se almacenan aquí.<br/> Esta carpeta se sobrescribe cada vez que se ejecuta la fase de preparación en un determinado equipo de origen. Esta carpeta nunca se elimina explícitamente, por lo que la replicación en destinos puede tener lugar en cualquier momento después de preparar el origen.<br/> Cada aplicación se almacena en su propia subcarpeta denominada <appName> + <appID> .<br/> |



 

## <a name="target-folders"></a>Carpetas de destino



| Carpeta                    | Propósito                                                                                                                                                                                                                                                                                                                                      |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReplicaNew<br/>     | La fase de copia copia todos los archivos y subcarpetas de ReplicaSource del origen en ReplicaNew en el destino. Cualquier contenido anterior de ReplicaNew se elimina cada vez que se ejecuta la fase de copia en un destino determinado.<br/> Esta carpeta solo existe mientras se ejecuta el proceso de replicación. (Consulte ReplicaCurrent).<br/>           |
| ReplicaCurrent<br/> | Las aplicaciones replicadas actualmente instaladas en el destino se almacenan aquí.<br/> Cuando se inicia la fase de instalación, se cambia el nombre de la carpeta ReplicaNew a ReplicaCurrent. Si hay una carpeta ReplicaCurrent existente, se le cambia el nombre a ReplicaOld. Si hay una carpeta ReplicaOld existente, se elimina su contenido.<br/> |
| ReplicaOld<br/>     | Guarda los archivos de aplicación instalados durante el siguiente a la última replicación. Estos archivos se guardan solo con fines de copia de seguridad.<br/>                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro e informes de errores](logging-and-error-reporting.md)
</dt> <dt>

[Fases de replicación](replication-phases.md)
</dt> <dt>

[Usar COMREPL](using-comrepl.md)
</dt> <dt>

[Lo que se replica](what-gets-replicated.md)
</dt> </dl>

 

 





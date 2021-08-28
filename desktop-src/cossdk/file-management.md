---
description: Para habilitar la transferencia de archivos de aplicación, COMREPL administra automáticamente conjuntos de carpetas del sistema de archivos en el origen y el destino. Todas estas carpetas COMREPL se basan en la replicación %systemdir% \\ \\ com.
ms.assetid: 8c59577b-34ea-4675-aaea-a2732fd5ce14
title: Administración de archivos (Servicios de componentes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936375060b43e8abfd99f2d282e1cc05aada0d0e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882550"
---
# <a name="file-management"></a>Administración de archivos

Para habilitar la transferencia de archivos de aplicación, COMREPL administra automáticamente conjuntos de carpetas del sistema de archivos en el origen y el destino. Todas estas carpetas COMREPL se basan en la replicación %systemdir% \\ \\ com.

## <a name="source-folders"></a>Carpetas de origen



| Carpeta                   | Propósito                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReplicaSource<br/> | Las aplicaciones exportadas durante la fase de preparación se almacenan aquí.<br/> Esta carpeta se sobrescribe cada vez que se ejecuta la fase de preparación en un equipo de origen determinado. Esta carpeta nunca se elimina explícitamente, por lo que la replicación en los destinos puede realizarse en cualquier momento después de preparar el origen.<br/> Cada aplicación se almacena en su propia subcarpeta denominada &lt; appName &gt; + &lt; &gt; appID.<br/> |



 

## <a name="target-folders"></a>Carpetas de destino



| Carpeta                    | Propósito                                                                                                                                                                                                                                                                                                                                      |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReplicaNew<br/>     | La fase de copia copia todos los archivos y subcarpetas de ReplicaSource en el origen a ReplicaNew en el destino. Todos los contenidos anteriores de ReplicaNew se eliminan cada vez que se ejecuta la fase de copia en un destino determinado.<br/> Esta carpeta solo existe mientras se ejecuta el proceso de replicación. (Vea ReplicaCurrent).<br/>           |
| ReplicaCurrent<br/> | Las aplicaciones replicadas instaladas actualmente en el destino se almacenan aquí.<br/> Cuando se inicia la fase de instalación, se cambia el nombre de la carpeta ReplicaNew a ReplicaCurrent. Si hay una carpeta ReplicaCurrent existente, se cambia el nombre a ReplicaOld. Si hay una carpeta ReplicaOld existente, se elimina su contenido.<br/> |
| ReplicaOld<br/>     | Guarda los archivos de aplicación instalados durante la siguiente a la última replicación. Estos archivos solo se guardan con fines de copia de seguridad.<br/>                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro e informes de errores](logging-and-error-reporting.md)
</dt> <dt>

[Fases de replicación](replication-phases.md)
</dt> <dt>

[Uso de COMREPL](using-comrepl.md)
</dt> <dt>

[Qué se replica](what-gets-replicated.md)
</dt> </dl>

 

 





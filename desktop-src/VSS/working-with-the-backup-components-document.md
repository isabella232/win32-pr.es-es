---
description: Un solicitante crea un documento de componentes de copia de seguridad al inicio de la realización de una copia de seguridad.
ms.assetid: 5e40e45d-6afa-401a-a6b4-7bec460cb9ec
title: Trabajar con el documento componentes de copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40d5d3c97696b85d589501f6d3af0b6c7d0e6d47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696425"
---
# <a name="working-with-the-backup-components-document"></a>Trabajar con el documento componentes de copia de seguridad

Un solicitante crea un documento de componentes de copia de seguridad al inicio de la realización de una copia de seguridad. El documento contiene inicialmente solo una descripción del estado de la operación de copia de seguridad. Durante la restauración, el documento debe proporcionar instrucciones sobre el modo en que un solicitante debe continuar en la copia de archivos de nuevo en el disco. En el transcurso de la operación de restauración, se modifica el documento componentes de copia de seguridad y contiene el estado de esa operación.

A diferencia del documento de metadatos del escritor, que es de solo lectura, hay una ventana en la que el documento componentes de copia de seguridad puede ser modificado por los solicitantes y los escritores. El documento puede actualizarse hasta la generación de un evento [*BackupComplete*](vssgloss-b.md) o [*BackupShutdown*](vssgloss-b.md) durante las operaciones de copia de seguridad y hasta un evento [*postrestore*](vssgloss-p.md) durante la restauración.

Para usar el documento componentes de copia de seguridad del solicitante, es necesario conocer los temas siguientes:

-   [Ciclo de vida de documentos de componentes de copia de seguridad](backup-components-document-life-cycle.md)
-   [Contenido del documento componentes de copia de seguridad](backup-components-document-contents.md)

 

 




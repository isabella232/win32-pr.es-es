---
description: Tanto los escritores como los solicitantes mantienen la información necesaria para una operación de copia de seguridad o restauración en sus propios documentos de metadatos.
ms.assetid: 1ce56374-cfbf-4ee4-b942-8a7391911a38
title: Metadatos de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e718d3fb0290f8610944180c079e4d615124eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696463"
---
# <a name="vss-metadata"></a>Metadatos de VSS

Tanto los escritores como los solicitantes mantienen la información necesaria para una operación de copia de seguridad o restauración en sus propios documentos de metadatos.

Estos documentos, el [*documento de metadatos de escritor*](vssgloss-w.md) y el [*documento de componentes de copia de seguridad*](vssgloss-b.md), respectivamente, se usan como base para la comunicación del escritor y el solicitante y la coordinación durante las actividades de copia de seguridad y restauración.

Los metadatos se representan en formato XML con un esquema de propiedad. Los metadatos se pueden copiar en disco, en cinta o en cualquier otro dispositivo de almacenamiento masivo. Siempre debe guardarse en el medio de copia de seguridad durante una operación de copia de seguridad y tendrá que recuperarse de ese medio en el transcurso de una operación de restauración.

**PRECAUCIÓN:** Los detalles específicos del formato y del esquema son solo para uso del sistema. Los desarrolladores no deben intentar modificar o usar directamente la representación XML de los metadatos.

Los escritores y solicitantes se proporcionan con una variedad de métodos de consulta y de conjunto para obtener acceso y modificar los componentes de copia de seguridad y los documentos de metadatos del escritor:

-   [Trabajar con el documento de metadatos del escritor](working-with-the-writer-metadata-document.md)
-   [Trabajar con el documento componentes de copia de seguridad](working-with-the-backup-components-document.md)
-   [Componentes de metadatos de VSS](vss-metadata-components.md)

 

 




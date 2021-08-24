---
description: Tanto los escritores como los solicitantes mantienen la información necesaria para una operación de copia de seguridad o restauración en sus propios documentos de metadatos.
ms.assetid: 1ce56374-cfbf-4ee4-b942-8a7391911a38
title: Metadatos de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e69d0a40bbbce2d231573d187843c14bd83fea419a7024940d0fd618838500b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986585"
---
# <a name="vss-metadata"></a>Metadatos de VSS

Tanto los escritores como los solicitantes mantienen la información necesaria para una operación de copia de seguridad o restauración en sus propios documentos de metadatos.

Estos documentos, [](vssgloss-w.md) el documento de metadatos del escritor y el documento de componentes de copia de [*seguridad,*](vssgloss-b.md)respectivamente, se usan como base para la comunicación y coordinación entre escritores y solicitantes durante las actividades de copia de seguridad y restauración.

Los metadatos se representan en formato XML mediante un esquema propietario. Los metadatos se pueden copiar en disco, cinta o cualquier otro dispositivo de almacenamiento masivo. Siempre debe guardarse en el medio de copia de seguridad durante una operación de copia de seguridad y deberá recuperarse de ese medio en el transcurso de una operación de restauración.

**Precaución:** Los detalles específicos del formato y el esquema son solo para uso del sistema. Los desarrolladores no deben intentar modificar ni usar directamente la representación XML de los metadatos.

Los escritores y solicitantes se proporcionan con una variedad de consultas y establecen métodos para acceder a los documentos Componentes de copia de seguridad y Metadatos del escritor y modificarlos:

-   [Trabajar con el documento de metadatos del escritor](working-with-the-writer-metadata-document.md)
-   [Trabajar con el documento componentes de copia de seguridad](working-with-the-backup-components-document.md)
-   [Componentes de metadatos de VSS](vss-metadata-components.md)

 

 




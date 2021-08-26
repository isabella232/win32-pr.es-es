---
description: Los autores deben ejecutar la validación en todos los módulos de combinación nuevos o modificados recientemente antes de intentar combinar el módulo en una base de datos de instalación por primera vez.
ms.assetid: 8d6794af-403a-416e-8ace-1af3f193414b
title: Validación de módulos de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af5a226f72e35ce4ee76599444e86ef80bd71a8866ca80eef2a5da04a87fb79a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995805"
---
# <a name="validating-merge-modules"></a>Validación de módulos de combinación

Los autores deben ejecutar la validación en todos los módulos de combinación nuevos o modificados recientemente antes de intentar combinar el módulo en una base de datos de instalación por primera vez. La validación del módulo de [](package-validation.md) mezcla funciona de la misma manera que la validación de [paquetes,](internal-consistency-evaluators-ices.md) pero usa un conjunto diferente de evaluadores de coherencia interna (CIE) específicos de los módulos de combinación. Para obtener más información sobre estos ICE del módulo de mezcla, vea [Referencia de ICE del módulo de mezcla](merge-module-ice-reference.md).

Los ICE del módulo de mezcla se almacenan en el archivo .uu. del módulo de mezcla, Mergemod.uu. La instalación de la herramienta Orca o msival2 también proporciona los archivos Logo.rev, Darice.rev y Mergemod.audio.

Para obtener más información, vea [Referencia de ICE del módulo de mezcla](merge-module-ice-reference.md).

 

 




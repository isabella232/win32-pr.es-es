---
description: Aprenda a admitir diferentes versiones de Print Schema Framework. Este tema no está al día. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: fc89dd2d-9a5d-400b-aee9-a1e4cf7d83da
title: Admitir versiones de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0af6b3116115a4ce302a006311e7f85afc63cd9e5c415d2135cc2d88d948f574
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470117"
---
# <a name="supporting-schema-versions"></a>Admitir versiones de esquema

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El marco de esquema de impresión está sujeto a cambios en el futuro a medida que surjan nuevas necesidades. Se espera que estos cambios sean muy poco frecuentes, ya que el cambio más común es la introducción de nuevos nombres de instancia. Este cambio no afecta a la estructura del marco de trabajo y debe ser transparente para los clientes y proveedores. Los cambios en la estructura y la organización del marco de esquema de impresión se identificarán mediante incrementos en su número de versión. No se identificarán las adiciones a las palabras clave de esquema de impresión. Los proveedores de PrintTicket deben ser capaces de admitir la versión actual de Print Schema Framework, así como cualquier versión anterior. La versión de Print Schema Framework se identifica mediante el atributo XML: Version que aparece en el elemento raíz de PrintTicket.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




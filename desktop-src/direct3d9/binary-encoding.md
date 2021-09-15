---
description: En esta sección se detalla la versión binaria del formato de archivo DirectX (.x), tal como se introdujo con la versión de DirectX 3.0.
ms.assetid: d1b6698f-72bd-40a4-a501-c2093cd940f6
title: Codificación binaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56937b54be82e36d6ff18aab2a2349be6d59cc12
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569961"
---
# <a name="binary-encoding"></a>Codificación binaria

En esta sección se detalla la versión binaria del formato de archivo DirectX (.x), tal como se introdujo con la versión de DirectX 3.0.

El formato binario es una representación con tokens del formato de texto. Los tokens pueden ser independientes o ir acompañados de registros de datos primitivos. Los tokens independientes dan una estructura gramatical y los tokens que tienen registros suministran los datos necesarios.

Tenga en cuenta que todos los datos se almacenan en formato little-endian. Un flujo de datos binario válido consta de un encabezado seguido de plantillas o objetos de datos.

En esta sección se analizan los siguientes componentes del formato de archivo binario y se proporciona una plantilla de ejemplo y un objeto de datos binarios.

-   [Header](header.md)
-   [Tokens](tokens.md)
-   [Registros de token](token-records.md)
-   [Templates](dx9-graphics-reference-x-file-binaryencoding-templates.md) (Plantillas [C++])
-   [Data](dx9-graphics-reference-x-file-binaryencoding-data.md)
-   [Ejemplos](examples.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de formato de archivo X](dx9-graphics-reference-x-file-format.md)
</dt> </dl>

 

 




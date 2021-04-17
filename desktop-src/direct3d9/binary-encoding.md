---
description: En esta sección se detallan las versiones binarias del formato de archivo de DirectX (. x) que se introdujeron con la versión de DirectX 3,0.
ms.assetid: d1b6698f-72bd-40a4-a501-c2093cd940f6
title: Codificación binaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56937b54be82e36d6ff18aab2a2349be6d59cc12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714784"
---
# <a name="binary-encoding"></a>Codificación binaria

En esta sección se detallan las versiones binarias del formato de archivo de DirectX (. x) que se introdujeron con la versión de DirectX 3,0.

El formato binario es una representación con tokens del formato de texto. Los tokens pueden ser independientes o acompañados de registros de datos primitivos. Los tokens independientes proporcionan una estructura gramatical y los tokens del cojinete de registros proporcionan los datos necesarios.

Tenga en cuenta que todos los datos se almacenan en formato Little-Endian. Un flujo de datos binario válido está formado por un encabezado seguido por plantillas u objetos de datos.

En esta sección se describen los siguientes componentes del formato de archivo binario y se proporciona una plantilla de ejemplo y un objeto de datos binarios.

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

 

 




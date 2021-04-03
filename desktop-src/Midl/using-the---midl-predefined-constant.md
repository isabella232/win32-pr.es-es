---
title: Usar la constante predefinida __midl
description: Cuando el compilador MIDL procesa los archivos IDL y ACF de entrada, \_ \_ se define MIDL de forma predeterminada y se usa para la compilación condicional con el fin de lograr la coherencia en toda la compilación.
ms.assetid: ba9557f8-d398-4c87-993d-f4e545894cdd
keywords:
- MIDL del compilador MIDL mediante la _midl constante predefinida
- _midl la constante MIDL predefinida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae49675b38dcc3cab2d3d41e4f48cd0637d78523
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075799"
---
# <a name="using-the-__midl-predefined-constant"></a>Usar la \_ \_ constante predefinida MIDL

Cuando el compilador MIDL procesa los archivos IDL y ACF de entrada, \_ \_ se define MIDL de forma predeterminada y se usa para la compilación condicional con el fin de lograr la coherencia en toda la compilación. En este caso, se usa la instrucción define en los archivos de encabezado, como la **\_ fase MIDL Pass**, y se reemplazan por una marca coherente. El valor de la \_ \_ constante MIDL indica la versión del compilador *Major. minor* según la fórmula *principal* \* 100 + *Minor*; por ejemplo, MIDL ver. 6.0. x tiene el \_ \_ MIDL definido como 600.

Si lo desea, puede invalidar este valor predeterminado si especifica lo siguiente en la línea de comandos: **/u \_ \_ MIDL**. Para obtener más información, consulte [**/u**](-u.md).

 

 





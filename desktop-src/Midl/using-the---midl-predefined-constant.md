---
title: Usar la __midl predefinida
description: Cuando el compilador MIDL procesa los archivos IDL y ACF de entrada, midl se define de forma predeterminada y se usa para que la compilación condicional alcance la coherencia a lo largo \_ \_ de la compilación.
ms.assetid: ba9557f8-d398-4c87-993d-f4e545894cdd
keywords:
- MIDL del compilador MIDL , mediante la _midl constante predefinida
- _midl MIDL constante predefinida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60fbc111ad07839d891f7bdffaf7ecaae83fbf277a0fc2c93fc483f526f9dda5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382835"
---
# <a name="using-the-__midl-predefined-constant"></a>Uso de \_ \_ la constante predefinida midl

Cuando el compilador MIDL procesa los archivos IDL y ACF de entrada, midl se define de forma predeterminada y se usa para que la compilación condicional alcance la coherencia a lo largo \_ \_ de la compilación. Esto elimina por fases el uso de instrucciones define en los archivos de encabezado, como **MIDL \_ PASS** y las reemplaza por una marca coherente. El valor de la constante midl indica la versión del compilador major.minor según la fórmula \_ \_ *major*  \* 100 + *minor;* por ejemplo, MIDL ver. 6.0.x tiene \_ \_ el valor midl definido como 600.

Si lo elige, puede invalidar este valor predeterminado especificando lo siguiente en la línea de comandos: **/U \_ \_ midl**. Para obtener más información, vea [**/U**](-u.md).

 

 





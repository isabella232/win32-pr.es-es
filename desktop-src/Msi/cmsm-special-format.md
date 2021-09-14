---
description: Algunos valores usados con módulos de combinación configurables requieren un control de texto especial.
ms.assetid: b9d41400-f3b5-4f85-8728-56f9b90a50ca
title: Formato especial de CMSM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9b6fa0bc5e84f125d0872a2937db7701f70820
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158894"
---
# <a name="cmsm-special-format"></a>Formato especial de CMSM

Algunos valores usados con módulos de combinación configurables requieren un control de texto especial. Una cadena de texto descrita como en "Formato especial de CMSM" trata el punto y coma (;) y es igual a (=) caracteres como caracteres reservados que usa la herramienta de combinación de cliente o Mergemod.dll.

El formato especial de CMSM se usa actualmente en las siguientes ubicaciones:

-   Columna Row de la [tabla ModuleSubstitution](modulesubstitution-table.md).
-   Columna Value de la [tabla ModuleSubstitution](modulesubstitution-table.md).
-   Columna ContextData de la [tabla ModuleConfiguration cuando](moduleconfiguration-table.md) Bitfield es el valor de la columna Formato.
-   Columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md) cuando Text es el valor de la columna Format y Enum es el valor de la columna Type.
-   Columna DefaultValue de la [tabla ModuleConfiguration](moduleconfiguration-table.md) cuando Key es el valor de la columna Format.
-   Elementos configurables en el formato de clave utilizado por [**el método ProvideTextData**](configuremodule-providetextdata.md).

Para escribir punto y coma literal o caracteres iguales en un valor en formato especial de CMSM, antefipe el carácter con un carácter de barra diagonal inversa (' \\ '). Una barra diagonal inversa literal se puede representar mediante dos barras diagonales inversas. Un solo carácter precedido por una sola barra diagonal inversa se traduce en un solo carácter, incluso si no es necesario escapar el carácter.

Si un carácter de punto y coma o igual no está precedido por una barra diagonal inversa pero no tiene un comportamiento definido en el contexto del valor, la cadena resultante no está definida. Por ejemplo, la columna DefaultValue de la tabla ModuleConfiguration tiene un formato especial cmsm para todos los elementos clave porque el carácter de punto y coma es el delimitador de columna. Aunque el carácter igual no tiene ningún significado especial en esta cadena, los caracteres literales iguales deben seguir siendo caracteres de escape en esta cadena.

 

 




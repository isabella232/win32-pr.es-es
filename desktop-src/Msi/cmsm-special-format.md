---
description: Ciertos valores usados con módulos de combinación configurables requieren un control de texto especial.
ms.assetid: b9d41400-f3b5-4f85-8728-56f9b90a50ca
title: Formato especial de CMSM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8521c422d62980da0d222f8a8fc8395afa40b68bfd65c5600298372b1035f97d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119252145"
---
# <a name="cmsm-special-format"></a>Formato especial de CMSM

Ciertos valores usados con módulos de combinación configurables requieren un control de texto especial. Una cadena de texto descrita como en "formato especial cmsm" trata el punto y coma (;) y es igual a (=) caracteres como caracteres reservados usados por la herramienta de combinación de cliente o Mergemod.dll.

El formato especial de CMSM se usa actualmente en las siguientes ubicaciones:

-   Columna Row de la [tabla ModuleSubstitution](modulesubstitution-table.md).
-   Columna Valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).
-   Columna ContextData de la [tabla ModuleConfiguration cuando](moduleconfiguration-table.md) Bitfield es el valor de la columna Formato.
-   Columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md) cuando Text es el valor de la columna Format y Enum es el valor de la columna Type.
-   Columna DefaultValue de la [tabla ModuleConfiguration cuando](moduleconfiguration-table.md) Key es el valor de la columna Formato.
-   Elementos configurables en el formato de clave utilizado por [**el método ProvideTextData**](configuremodule-providetextdata.md).

Para escribir puntos y coma literales o caracteres iguales en un valor en formato especial de CMSM, antefise el carácter con un carácter de barra diagonal inversa (' \\ '). Una barra diagonal inversa literal se puede representar mediante dos barras diagonales inversas. Un solo carácter precedido por una sola barra diagonal inversa se convierte en el carácter único, incluso si no es necesario escapar el carácter.

Si un carácter de punto y coma o igual no está precedido por una barra diagonal inversa pero no tiene un comportamiento definido en el contexto del valor, la cadena resultante no está definida. Por ejemplo, la columna DefaultValue de la tabla ModuleConfiguration tiene un formato especial cmsm para todos los elementos clave porque el carácter de punto y coma es el delimitador de columna. Aunque el carácter igual no tiene ningún significado especial en esta cadena, los caracteres literales iguales deben seguir siendo caracteres de escape en esta cadena.

 

 




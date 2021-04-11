---
description: Algunos valores usados con los módulos de combinación configurables requieren un tratamiento de texto especial.
ms.assetid: b9d41400-f3b5-4f85-8728-56f9b90a50ca
title: Formato especial de CMSM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9b6fa0bc5e84f125d0872a2937db7701f70820
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276170"
---
# <a name="cmsm-special-format"></a>Formato especial de CMSM

Algunos valores usados con los módulos de combinación configurables requieren un tratamiento de texto especial. Una cadena de texto que se describe como "formato especial de CMSM" trata el punto y coma (;) y es igual a (=) caracteres como caracteres reservados usados por la herramienta de combinación de cliente o Mergemod.dll.

El formato especial de CMSM se usa actualmente en las siguientes ubicaciones:

-   Columna de filas de la [tabla ModuleSubstitution](modulesubstitution-table.md).
-   La columna de valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).
-   La columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md) cuando el campo de bits es el valor de la columna formato.
-   La columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md) cuando el texto es el valor de la columna formato y enum es el valor de la columna tipo.
-   La columna DefaultValue de la [tabla ModuleConfiguration](moduleconfiguration-table.md) cuando Key es el valor de la columna Format.
-   Elementos configurables en el formato de clave que usa el [**método ProvideTextData**](configuremodule-providetextdata.md).

Para especificar signos de punto y coma literales o caracteres iguales en un valor en formato especial de CMSM, anteponga al carácter un carácter de barra diagonal inversa (' \\ '). Una barra diagonal inversa literal se puede representar mediante dos barras diagonales inversas. Un único carácter precedido por una sola barra diagonal inversa se convierte en el carácter único, aunque no sea necesario escapar el carácter.

Si un carácter de punto y coma o igual no tiene un prefijo de una barra diagonal inversa todavía no tiene un comportamiento definido en el contexto del valor, la cadena resultante es indefinida. Por ejemplo, la columna DefaultValue de la tabla ModuleConfiguration tiene el formato especial CMSM para todos los elementos clave, ya que el carácter de punto y coma es el delimitador de columna. Aunque el carácter igual no tiene ningún significado especial en esta cadena, los caracteres equivalentes a los literales deben seguir estando en esta cadena.

 

 




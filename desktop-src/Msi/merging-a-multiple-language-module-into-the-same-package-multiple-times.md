---
description: Cuando un módulo admite varios idiomas, puede combinarlo en la misma base de datos Windows Installer varias veces, pero asegúrese de que cada combinación usa un idioma diferente.
ms.assetid: 816b1f52-1ca2-4332-9a9b-462ea372c3bb
title: Combinar un módulo de varios idiomas en el mismo paquete varias veces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52552a68643d52c6aad97ed666b7dc1ae4043fd9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261287"
---
# <a name="merging-a-multiple-language-module-into-the-same-package-multiple-times"></a>Combinar un módulo de varios idiomas en el mismo paquete varias veces

Cuando un módulo admite varios idiomas, puede combinarlo en la misma base de datos Windows Installer varias veces, pero asegúrese de que cada combinación usa un idioma diferente. Antes de cada combinación, solicite un idioma diferente del módulo. A continuación, .msi base de datos resultante tiene un registro en [la tabla ModuleSignature para](modulesignature-table.md) cada combinación del módulo. Los componentes que se comparten entre idiomas solo existen una vez en la tabla de componentes [,](component-table.md)pero están asociados a cada idioma de la [tabla ModuleComponents](modulecomponents-table.md).

Al combinar varios idiomas de un módulo en el mismo paquete, cada combinación debe cumplir las mismas restricciones en las páginas de códigos que los módulos de un solo idioma. Los módulos no pueden contener cadenas en páginas de códigos diferentes.

Al combinar un módulo varias veces en un único archivo .msi, es posible que [](file-table.md) tenga que modificar el orden de los archivos de la tabla de archivos para usar el .cab existente del módulo directamente en la instalación. El orden de los archivos de la tabla de archivos debe coincidir con el orden de los archivos del .cab. Al combinar un módulo varias veces en una base de datos de instalación, se puede modificar la secuencia, ya que los archivos compartidos entre los idiomas pueden existir en el módulo desde una combinación anterior y tienen un número de secuencia relativo diferente.

 

 




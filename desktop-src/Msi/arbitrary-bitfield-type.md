---
description: El &\# 0034; Bitfield&0034; escriba sin solicitudes de contexto que el usuario proporcione un entero cuyo valor se usa para establecer uno o varios bits en un \# campo de bits. Este texto puede estar en cualquier idioma compatible con la página de códigos de la base de datos.
ms.assetid: 28e1bdb9-a42d-46ce-ad24-71bc22e2d92a
title: Tipo de campo de bits arbitrario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521889ffb1677bed249a92f757556a2fdbe36768
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159106"
---
# <a name="arbitrary-bitfield-type"></a>Tipo de campo de bits arbitrario

El tipo "Bitfield" sin solicitudes de contexto que el usuario proporcione un entero cuyo valor se usa para establecer uno o varios bits en un campo de bits. Este texto puede estar en cualquier idioma compatible con la página de códigos de la base de datos.

El tipo de campo de bits arbitrario [de tipo semántico](semantic-types.md) es uno de los tipos de campo de bits. Este tipo consta de un entero elegido por el usuario a partir de un conjunto de opciones. La herramienta de combinación sustituye el entero seleccionado en las plantillas especificadas en la columna Valor de la [tabla ModuleSubstitution](modulesubstitution-table.md). Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del elemento en la columna Nombre, escribir "3" en la columna Formato, dejar la columna Tipo en blanco y escribir la lista de posibles enteros en la columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md).

La columna Tipo está reservada y debe ser NULL. La entrada de la columna ContextData para todos los tipos de formato de campo de bits debe tener el formato " &lt; mask &gt; ; &lt; Valor &gt; = &lt; de nombre &gt; ; &lt; Valor &gt; = &lt; de &gt; nombre ....", &lt; &gt; &lt; &gt; &lt; donde mask &gt; es un valor entero que indica los bits de interés, Name es un nombre para mostrar localizable para la elección y value es un valor entero decimal. La columna de contexto está en uso el [formato especial de CMSM y](cmsm-special-format.md) para todos los tipos de campo de bits. Se puede especificar un carácter literal "=" o ";" en el campo Nombre si se le antepeda con un carácter de barra diagonal inversa &lt; &gt; (' \\ ').

 

 




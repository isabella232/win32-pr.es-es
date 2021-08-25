---
title: Error de rol de contenedor de ARIA
description: Error de rol de contenedor de ARIA
ms.assetid: AF207293-1172-43D0-B92C-C3070876DF54
keywords:
- AriaContainerRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507f094a5f7270565de0426b50afd6aef699607d857ef1ba7ed3d6c8bb1a1a2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759835"
---
# <a name="aria-container-role-error"></a>Error de rol de contenedor de ARIA

## <a name="text"></a>Texto

El elemento **con el descendiente** activo definido no tiene un rol de contenedor **(cuadro** **combinado,** cuadrícula , **cuadro** de **lista,** **menú,** barra de menús, grupo de **radios,** árbol, **treegrid,** **tablist,** **fila**).

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a los elementos que tienen el **atributo aria-activedescendant.**

Un elemento parece ser un contenedor que tiene el conjunto de atributos **aria-activedescendant,** pero el atributo role del elemento no tiene un valor que sea válido para un contenedor.

Para corregir este error, establezca el atributo de rol en un valor de rol Iniciativa de accesibilidad web: aplicaciones de Internet enriquecidas accesibles (SI-ARIA) que sea válido para un elemento contenedor: **cuadro** combinado, **cuadrícula,** **cuadro** de **lista,** **menú,** barra de menús, grupo  de **radios,** **lista** de pestañas, árbol o  **treegrid.**

## <a name="example"></a>Ejemplo


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1">
  <div role="option" id="listbox1-1" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
  ...
<div>
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Error de rol de ARIA](aria-role-invalid.md)
</dt> </dl>

 

 





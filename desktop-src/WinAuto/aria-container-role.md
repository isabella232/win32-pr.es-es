---
title: Error de rol de contenedor de ARIA
description: Error de rol de contenedor de ARIA
ms.assetid: AF207293-1172-43D0-B92C-C3070876DF54
keywords:
- AriaContainerRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02554c868816c05981fa9f008c8f79f0a3eb0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994536"
---
# <a name="aria-container-role-error"></a>Error de rol de contenedor de ARIA

## <a name="text"></a>Texto

El elemento con el **descendiente activo** definido no tiene un rol de contenedor (**ComboBox**, **Grid**, **ListBox**, **Menu**, **MenuBar**, **RadioGroup**, **Tree**, **treegrid**, **Tablist**, **Row**).

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a los elementos que tienen el atributo **Aria-activedescendant** .

Un elemento parece ser un contenedor que tiene establecido el atributo **Aria-activedescendant** , pero el atributo role del elemento no tiene un valor válido para un contenedor.

Para corregir este error, establezca el atributo **role** en un valor de rol de aplicaciones de Internet enriquecidas accesible desde una iniciativa de accesibilidad web (WAI-ARIA) que sea válido para un elemento contenedor: **ComboBox**, **Grid**, **ListBox**, **Menu**, **MenuBar**, **RadioGroup**, **Tablist**, **Tree** o **treegrid**.

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

 

 





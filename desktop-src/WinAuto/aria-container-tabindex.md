---
title: Error de tabindex del contenedor de ARIA
description: Error de tabindex del contenedor de ARIA
ms.assetid: CCEA9490-903D-423D-B9FD-641E8B7D3E0B
keywords:
- AriaContainerTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ff7149a82ddf45abb50175202ba2ea2ef8be854eef307643b207e796ab26cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899585"
---
# <a name="aria-container-tabindex-error"></a>Error de tabindex del contenedor de ARIA

## <a name="text"></a>Texto

Element es un contenedor que se puede centrar con descendientes activos definidos pero sin un **valor tabindex** mayor o igual que 0.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a los elementos que tienen el atributo **aria-activedescendant,** no están deshabilitados y no tienen el atributo **tabindex** establecido en un valor mayor o igual que 0. Estos elementos deben estar en orden de tabulación porque son responsables de controlar los eventos de teclado de sus elementos secundarios.

Para corregir este error, establezca el atributo **tabindex** en un valor mayor o igual que 0.

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

[Error de tabindex del rol de contenedor ARIA (sin descendiente activo)](aria-container--no-active-descendant--tabindex.md)
</dt> </dl>

 

 





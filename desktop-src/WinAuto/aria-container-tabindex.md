---
title: Error de tabIndex del contenedor de ARIA
description: Error de tabIndex del contenedor de ARIA
ms.assetid: CCEA9490-903D-423D-B9FD-641E8B7D3E0B
keywords:
- AriaContainerTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6af684b401627181aaef656215240a312393f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419067"
---
# <a name="aria-container-tabindex-error"></a>Error de tabIndex del contenedor de ARIA

## <a name="text"></a>Texto

El elemento es un contenedor enfocable con descendientes activos definidos pero sin el valor de **TabIndex** mayor o igual que 0.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a los elementos que tienen el atributo **Aria-activedescendant** , no se deshabilitan y no tienen el atributo **TabIndex** establecido en un valor mayor o igual que 0. Estos elementos deben estar en el orden de tabulación porque son responsables de controlar los eventos de teclado de sus elementos secundarios.

Para corregir este error, establezca el atributo **TabIndex** en un valor que sea mayor o igual que 0.

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

[Error de tabIndex del rol de contenedor de ARIA (sin activos descendientes)](aria-container--no-active-descendant--tabindex.md)
</dt> </dl>

 

 





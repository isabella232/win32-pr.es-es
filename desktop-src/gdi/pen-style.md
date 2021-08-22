---
description: El atributo style especifica el patrón de línea que aparece cuando se usa un lápiz geométrico o un lápiz geométrico determinado. Hay ocho estilos de lápiz predefinidos. En la ilustración siguiente se muestran los siete estilos definidos por el sistema.
ms.assetid: a9aaa999-529c-46e1-9a3f-b6fdcbeb5b51
title: Estilo de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42cc82510c58d36cec76039488ecc13c826609a0870b929f18d82282a87ba8cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666515"
---
# <a name="pen-style"></a>Estilo de lápiz

El atributo style especifica el patrón de línea que aparece cuando se usa un lápiz geométrico o un lápiz geométrico determinado. Hay ocho estilos de lápiz predefinidos. En la ilustración siguiente se muestran los siete estilos definidos por el sistema.

![ilustración que muestra siete líneas, cada una dibujada con un estilo predefinido diferente](images/cspen-01.png)

El estilo dentro del marco es idéntico al estilo sólido para los lápices de color. Sin embargo, funciona de forma diferente cuando se usa con un lápiz geométrico. Si el lápiz geométrico es más ancho que un solo píxel y una función de dibujo usa el lápiz para dibujar un borde alrededor de un objeto relleno, el sistema dibuja el borde dentro del marco del objeto. Mediante el uso del estilo de marco interior, una aplicación puede asegurarse de que un objeto aparece completamente dentro de las dimensiones especificadas, independientemente del ancho del lápiz geométrico.

Además de los siete estilos definidos por el sistema, hay un octavo estilo definido por el usuario (o la aplicación). Un estilo definido por el usuario genera líneas con una serie personalizada de guiones y puntos.

Use la [**función CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)o [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) para crear un lápiz que tenga los estilos definidos por el sistema. Use la **función ExtCreatePen** para crear un lápiz con un estilo definido por el usuario.

 

 




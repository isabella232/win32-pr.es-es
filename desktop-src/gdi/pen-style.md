---
description: El atributo de estilo especifica el patrón de línea que aparece cuando se usa un lápiz cosmético o geométrico determinado. Hay ocho estilos de lápiz predefinidos. En la ilustración siguiente se muestran los siete estilos definidos por el sistema.
ms.assetid: a9aaa999-529c-46e1-9a3f-b6fdcbeb5b51
title: Estilo de pluma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f447839627f97d7662fdef35bd7088ef7b0dcba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001518"
---
# <a name="pen-style"></a>Estilo de pluma

El atributo de estilo especifica el patrón de línea que aparece cuando se usa un lápiz cosmético o geométrico determinado. Hay ocho estilos de lápiz predefinidos. En la ilustración siguiente se muestran los siete estilos definidos por el sistema.

![Ilustración que muestra siete líneas, cada una dibujada con un estilo predefinido diferente](images/cspen-01.png)

El estilo interior-Frame es idéntico al estilo sólido para los lápices estéticos. Sin embargo, funciona de forma diferente cuando se usa con un lápiz geométrico. Si el lápiz geométrico es más ancho que un solo píxel y una función de dibujo usa el lápiz para dibujar un borde alrededor de un objeto relleno, el sistema dibuja el borde dentro del marco del objeto. Con el estilo interior-Frame, una aplicación puede asegurarse de que un objeto aparece completamente dentro de las dimensiones especificadas, independientemente del ancho del lápiz geométrico.

Además de los siete estilos definidos por el sistema, hay un octavo estilo definido por el usuario (o aplicación). Un estilo definido por el usuario genera líneas con una serie personalizada de guiones y puntos.

Use la función [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)o [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) para crear un lápiz que tenga los estilos definidos por el sistema. Utilice la función **ExtCreatePen** para crear un lápiz que tenga un estilo definido por el usuario.

 

 




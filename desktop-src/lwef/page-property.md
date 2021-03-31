---
title: Propiedad de página
description: Propiedad de página
ms.assetid: c3cf07e9-a324-443b-a0c0-2fb80463548f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c51f55e4d1e9c7d2d23713810412060d915c7af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418684"
---
# <a name="page-property"></a>Propiedad de página

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece la página mostrada en la ventana de la hoja de propiedades del agente de Microsoft.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintáctica** 
</dt> <dd>

*agente * * *.* *  \[  =  *Cadena* PropertySheet.Page\]



| Parte     | Descripción                                                                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *string* | Expresión de cadena con uno de los valores siguientes. **"Voz"** Muestra la página de entrada de voz.<br/> **"Output"** Muestra la página de salida.<br/> **"Copyright"** Muestra la página de copyright.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si no hay instalado ningún motor de voz, el establecimiento de la **Página** en **"voz"** no tiene ningún efecto. Además, la propiedad **visible** de la ventana debe establecerse en **true** para que el usuario vea la página.

> [!Note]  
> El usuario puede invalidar esta propiedad.

 

 

 






---
title: Propiedad Page
description: Propiedad Page
ms.assetid: c3cf07e9-a324-443b-a0c0-2fb80463548f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ca14a4f68c326d1b231aa106450fefc7607857576f817ffaa255fa27f2249b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601015"
---
# <a name="page-property"></a>Propiedad Page

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece la página que se muestra en la ventana de hoja de propiedades de Microsoft Agent.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxis** 
</dt> <dd>

*agent!". PropertySheet.Page* *  \[  =  *cadena*\]



| Parte     | Descripción                                                                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *string* | Expresión de cadena con uno de los valores siguientes. **"Voz"** Muestra la página Entrada de voz.<br/> **"Salida"** Muestra la página Salida.<br/> **"Copyright"** Muestra la página Copyright.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si no hay ningún motor de voz instalado, la **configuración de Página** en **"Voz"** no tiene ningún efecto. Además, la propiedad Visible de la **ventana** debe establecerse en **True** para que el usuario vea la página.

> [!Note]  
> El usuario puede invalidar esta propiedad.

 

 

 






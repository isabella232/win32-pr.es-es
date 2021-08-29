---
title: Propiedad FontName (objeto Balloon)
description: Obtenga información sobre la propiedad de objeto FontName Balloon. Microsoft Agent está en desuso a partir Windows 7.
ms.assetid: a84a19a4-9e0e-4736-b401-286e6618bc19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17ac59e1e11575ddf4144c90d122096c24542ee28130552eff0ba53ed4af17ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349253"
---
# <a name="fontname-property-balloon-object"></a>Propiedad FontName (objeto Balloon)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece la fuente utilizada en el globo de palabras para el carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent.***Caracteres("**_CharacterID_*_"). Fuente Balloon.FontName_ *  \[  =  \]



| Parte   | Descripción                                      |
|--------|--------------------------------------------------|
| *Fuente* | Valor de cadena correspondiente al nombre de la fuente. |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

La [**propiedad FontName**](fontname-property.md) define la fuente utilizada para mostrar texto en la ventana de globo de palabras de una cadena. El valor predeterminado de la configuración de fuente del globo de palabras de un carácter se establece en el Editor de caracteres de Microsoft Agent. Además, el usuario puede invalidar la configuración de fuente de todos los caracteres de la hoja de propiedades de Microsoft Agent.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

> [!Note]  
> Si usa un carácter que no compiló, compruebe las propiedades [**FontName**](fontname-property.md) y [**FontCharSet**](fontcharset-property.md) del carácter para determinar si son adecuadas para la configuración regional. Es posible que tenga que establecer estos valores antes de usar el [**método Speak**](speak-method.md) para asegurarse de que se muestra el texto adecuado en el globo de palabras.

 

 

 





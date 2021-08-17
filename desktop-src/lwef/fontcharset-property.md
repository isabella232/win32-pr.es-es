---
title: Propiedad FontCharSet
description: Propiedad FontCharSet
ms.assetid: 2f23a242-d620-4766-8f59-cf158aa55969
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca702bb1ff9dfe020f7fdb43b57a74fd1e5e46a14caff8735f21170ed8e2f1b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479333"
---
# <a name="fontcharset-property"></a>Propiedad FontCharSet

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece el juego de caracteres para la fuente que se muestra en el globo de palabras del carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Valor de Balloon.FontCharSet_ *  \[  =  \]



| Parte    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *value* | Valor entero que especifica el juego de caracteres utilizado por la fuente. A continuación se muestra una configuración común para value: 0 Standard Windows characters (ANSI).<br/> 1 Juego de caracteres predeterminado.<br/> 2 Juego de caracteres de símbolo.<br/> Juego de caracteres de doble byte (DBCS) de 128 bytes único para la versión japonesa de Windows.<br/> Juego de caracteres de doble byte (DBCS) de 129 bytes único para la versión en coreano de Windows.<br/> Juego de caracteres de doble byte (DBCS) de 134 bytes único para la versión en chino simplificado de Windows.<br/> Juego de caracteres de doble byte (DBCS) de 136 bytes único para la versión en chino tradicional de Windows.<br/> 255 Caracteres extendidos que normalmente muestran las aplicaciones MS-DOS de Microsoft.<br/> Para otros valores de juego de caracteres, consulte la documentación del SDK de plataforma.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

El valor predeterminado del juego de caracteres del globo de palabras de un carácter se establece en el Editor de caracteres de Microsoft Agent. Además, el usuario puede invalidar la configuración del juego de caracteres para todos los caracteres de la hoja de propiedades de Microsoft Agent.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

> [!Note]  
> Si usa un carácter que no compiló, compruebe las propiedades [**FontName**](fontname-property.md) y **FontCharSet** del carácter para determinar si son adecuadas para la configuración regional. Es posible que tenga que establecer estos valores antes de usar el [**método Speak**](speak-method.md) para asegurarse de que se muestra el texto adecuado dentro del globo de palabras.

 

## <a name="see-also"></a>Consulte también

[**Propiedad FontName**](fontname-property.md)


 

 






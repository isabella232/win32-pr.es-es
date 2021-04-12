---
title: Propiedad FontCharSet
description: Propiedad FontCharSet
ms.assetid: 2f23a242-d620-4766-8f59-cf158aa55969
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4561de9af823b4213266a93b7bfa2e29588c3c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357591"
---
# <a name="fontcharset-property"></a>Propiedad FontCharSet

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece el juego de caracteres de la fuente que se muestra en el globo de palabras del carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("*** CharacterID * *"). Balloon. FontCharSet* *  \[  =  *valor*\]



| Parte    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *value* | Valor entero que especifica el juego de caracteres utilizado por la fuente. A continuación se muestran algunos valores de configuración comunes para el valor: 0 caracteres estándar de Windows (ANSI).<br/> 1 juego de caracteres predeterminado.<br/> 2 el juego de caracteres de símbolos.<br/> 128 juego de caracteres de doble byte (DBCS) único para la versión en japonés de Windows.<br/> 129 juego de caracteres de doble byte (DBCS) único para la versión coreana de Windows.<br/> 134 juego de caracteres de doble byte (DBCS) único para la versión de chino simplificado de Windows.<br/> 136 juego de caracteres de doble byte (DBCS) único para la versión en chino tradicional de Windows.<br/> 255 caracteres extendidos que se muestran normalmente en aplicaciones de Microsoft MS-DOS.<br/> Para otros valores de juego de caracteres, consulte la documentación del SDK de la plataforma.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

El valor predeterminado para el juego de caracteres del globo de palabras de un carácter se establece en el editor de caracteres del agente de Microsoft. Además, el usuario puede invalidar la configuración del juego de caracteres para todos los caracteres de la hoja de propiedades del agente de Microsoft.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

> [!Note]  
> Si usa un carácter que no ha compilado, compruebe las propiedades [**FontName**](fontname-property.md) y **FontCharSet** del carácter para determinar si son adecuados para la configuración regional. Es posible que tenga que establecer estos valores antes de usar el método [**Speak**](speak-method.md) para asegurarse de que el texto se muestre correctamente en el globo de palabras.

 

## <a name="see-also"></a>Consulte también

[**FontName (propiedad)**](fontname-property.md)


 

 






---
title: Propiedad FontName (objeto Commands)
description: Obtenga información sobre la propiedad de objeto FontName Commands. Microsoft Agent está en desuso a partir Windows 7.
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1f8c9c66e7d205e79a3ac9b076fa4e01852df358657761f8792d42b764b270
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725715"
---
# <a name="fontname-property-commands-object"></a>Propiedad FontName (objeto Commands)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece la fuente utilizada en el menú emergente del carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Commands.FontName_ *  \[  =  *Font*\]



| Parte   | Descripción                                      |
|--------|--------------------------------------------------|
| *Fuente* | Valor de cadena correspondiente al nombre de la fuente. |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **propiedad FontName** define la fuente utilizada para mostrar texto en el menú emergente del carácter. El valor predeterminado de la configuración de fuente se basa en la configuración de fuente del menú para la configuración de **LanguageID** del carácter o, si no se establece, en la configuración del identificador de idioma predeterminado del usuario.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

 

 





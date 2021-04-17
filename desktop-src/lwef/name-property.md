---
title: Propiedad Name (objeto Characters)
description: Propiedad Name
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e7b4a8872952cce0ae68445ec22a5599891674
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488729"
---
# <a name="name-property-characters-object"></a>Propiedad Name (objeto Characters)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece una cadena que especifica el nombre predeterminado del carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("**_CharacterID_*_")._ *  \[  =  *Cadena* de nombre\]



| Parte     | Descripción                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| *string* | Valor de cadena que corresponde al nombre del carácter (en la configuración de idioma actual). |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **nombre** de un carácter puede depender del valor de [**LanguageID**](languageid-property.md) del carácter. El nombre de un carácter en un idioma puede ser diferente o utilizar caracteres distintos a los de otro. El **nombre** predeterminado del carácter para un idioma específico se define cuando el carácter se compila con el editor de caracteres del agente de Microsoft.

Evite cambiar el nombre de un carácter, especialmente cuando se usa en un escenario en el que otras aplicaciones cliente pueden utilizar el mismo carácter. Además, el agente usa el **nombre** del carácter para crear automáticamente comandos para ocultar y mostrar el carácter.

 

 





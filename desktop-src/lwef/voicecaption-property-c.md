---
title: Propiedad VoiceCaption (objeto Command)
description: Propiedad VoiceCaption
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1077c8d65a52bc8f0cfa329fdceb740e30e6784
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105714520"
---
# <a name="voicecaption-property-command-object"></a>Propiedad VoiceCaption (objeto Command)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Establece o devuelve el texto que se muestra para el objeto de [**comando**](/windows/desktop/lwef/the-command-object) en la ventana comandos de voz.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*Caracteres Agent. ***("**_CharacterID_*_"). Comandos ("_*_Name_*_")._ *  \[  =  *Cadena* VoiceCaption\]



| Parte     | Descripción                                               |
|----------|-----------------------------------------------------------|
| *string* | Expresión de cadena que se evalúa como el texto que se muestra. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si define un objeto de [**comando**](/windows/desktop/lwef/the-command-object) en una colección de [**comandos**](https://www.bing.com/search?q=**Commands**) y establece su propiedad [**Voice**](voice-property.md) , normalmente también establecerá su propiedad [**VoiceCaption**](voicecaption-property.md) . Este texto aparecerá en la ventana comandos de voz cuando la aplicación cliente sea de entrada-activa y el carácter esté visible. Si no se establece esta propiedad, el valor de la propiedad [**Caption**](caption-property.md) determina el texto que se muestra. Cuando no se establece la propiedad **VoiceCaption** ni **Caption** , el comando no aparece en la ventana comandos de voz.

### <a name="see-also"></a>Consulte también

[**Propiedad Caption**](caption-property.md)


 

 

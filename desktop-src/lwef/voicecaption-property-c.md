---
title: Propiedad VoiceCaption (objeto Command)
description: Obtenga información sobre la propiedad VoiceCaption del objeto Command, que establece o devuelve el texto que se muestra para el objeto Command en la ventana Comandos de voz.
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1e911a4351483aeeea9258679d4321110b49c3d0c51fc49282701b027d27e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665055"
---
# <a name="voicecaption-property-command-object"></a>Propiedad VoiceCaption (objeto Command)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Establece o devuelve el texto que se muestra para el [**objeto Command**](/windows/desktop/lwef/the-command-object) en la ventana Comandos de voz.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Commands("_*_Name_*_"). Cadena VoiceCaption_ *  \[  =  \]



| Parte     | Descripción                                               |
|----------|-----------------------------------------------------------|
| *string* | Expresión de cadena que se evalúa como el texto mostrado. |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si define un objeto [**Command**](/windows/desktop/lwef/the-command-object) en una [**colección Commands**](https://www.bing.com/search?q=**Commands**) y establece su propiedad [**Voice,**](voice-property.md) normalmente también establecerá su [**propiedad VoiceCaption.**](voicecaption-property.md) Este texto aparecerá en la ventana Comandos de voz cuando la aplicación cliente esté activa en la entrada y el carácter esté visible. Si no se establece esta propiedad, la configuración de la [**propiedad Caption**](caption-property.md) determina el texto mostrado. Cuando no se **establece la propiedad VoiceCaption** ni **Caption,** el comando no aparece en la ventana Comandos de voz.

### <a name="see-also"></a>Consulte también

[**Propiedad Caption**](caption-property.md)


 

 

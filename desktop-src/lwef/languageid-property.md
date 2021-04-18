---
title: LanguageID (propiedad)
description: LanguageID (propiedad)
ms.assetid: f57b0fa1-b3b8-49c8-b441-2a40e564d6ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7a10e6b16f9e35b223bada728871d253685538
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357602"
---
# <a name="languageid-property"></a>LanguageID (propiedad)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece el identificador de idioma del carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

Caracteres del agente *. * * ** *  **("***CharacterID***"). LanguageID** \[  =  *LanguageID*\]



Parte

Descripción

LanguageID

Entero largo que especifica el identificador de idioma del carácter. El identificador de idioma (LANGID) de un carácter es un valor de 16 bits definido por Windows, que consta de un identificador de idioma principal y un identificador de idioma secundario. Los ejemplos siguientes son valores de idiomas admitidos por el agente de Microsoft. Para determinar el valor de otros lenguajes, consulte la *documentación del SDK* de la plataforma.

 

Árabe

&H0401

Italiano

&H0410

 

Vasco

&H042D

Japonés

&H0411

 

Chino (simplificado)

&H0804

Coreano

&H0412

 

Chino (tradicional)

&H0404

Noruego

&H0414

 

Croata

&H041A

Polaco

&H0415

 

Checo

&H0405

Portugués (Portugal)

&H0816

 

Danés

&H0406

Portugués (Brasil)

&H0416

 

Neerlandés

&H0413

Rumano

&H0418

 

Inglés (Gran Bretaña)

&H0809

Ruso

&H0419

 

Inglés (EE.UU.)

&H0409

Eslovaco

&H041B

 

Finés

&H040B

Esloveno

&H0424

 

Francés

&H040C

Español

&H0C0A

 

Alemán

&H0407

Sueco

&H041D

 

Griego

&H0408

Tailandés

&H041E

 

Hebreo

&H040D

Turco

&H041F

 

Húngaro

&H040E

 

 



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si no establece el **iddeidioma** para el carácter, su identificador de idioma será el identificador de idioma del sistema actual si se instala la dll de idioma correspondiente del agente; de lo contrario, el idioma del carácter será inglés (EE. UU.).

Esta propiedad también determina el idioma del texto del globo de palabras, los comandos del menú emergente del carácter y el motor de reconocimiento de voz. También determina el idioma predeterminado para la salida de TTS.

Si intenta establecer el **LanguageID** para un carácter y el archivo DLL del idioma del agente para ese idioma no está instalado o si no hay disponible una fuente de presentación para el ID. de idioma, el agente genera un error y se mantiene el valor **LanguageID** en la última configuración.

Si se establece esta propiedad, no se produce un error si no hay ningún motor de voz coincidente para el idioma. Para determinar si hay un motor de voz compatible disponible para el **iddeidioma**, consulte [**SRModeID**](srmodeid-property.md) o [**TTSModeID**](ttsmodeid-property.md). Si no establece **LanguageID**, se establecerá en la configuración de ID. de idioma predeterminado del usuario.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

> [!Note]  
> Si establece **LanguageID** en un idioma que admite texto bidireccional (como el árabe o el hebreo), pero el sistema que ejecuta la aplicación no tiene instalada la compatibilidad bidireccional, el texto del globo de palabras aparecerá en lugar lógico en lugar de mostrarse en orden.

 

## <a name="see-also"></a>Consulte también

[**Propiedad SRModeID**](srmodeid-property.md), [ **propiedad TTSModeID**](ttsmodeid-property.md)


 

 





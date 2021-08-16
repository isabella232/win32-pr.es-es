---
title: Propiedad LanguageID
description: Propiedad LanguageID
ms.assetid: f57b0fa1-b3b8-49c8-b441-2a40e564d6ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13af9f7a508732444be83fd56cce2fad6c7d7a5c148e196e2c466db102d2e6e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748703"
---
# <a name="languageid-property"></a>Propiedad LanguageID

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece el identificador de idioma del carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent.:Caracteres* *  **("**_CharacterID_*_"). LanguageID_* \[  =  *LanguageID*\]



Parte

Descripción

LanguageID

Entero Long que especifica el identificador de idioma del carácter. El identificador de idioma (LANGID) de un carácter es un valor de 16 bits definido por Windows, que consta de un identificador de idioma principal y un identificador de idioma secundario. Los ejemplos siguientes son valores para los idiomas admitidos por Microsoft Agent. Para determinar el valor de otros lenguajes, consulte la documentación *de Platform SDK*.

 

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

## <a name="remarks"></a>Comentarios

Si no establece el valor de **LanguageID** para el carácter, su identificador de idioma será el identificador de idioma del sistema actual si está instalado el archivo DLL de idioma del Agente correspondiente; de lo contrario, el idioma del carácter será inglés (EE. UU.).

Esta propiedad también determina el idioma del texto del globo de palabras, los comandos del menú emergente del carácter y el motor de reconocimiento de voz. También determina el idioma predeterminado para la salida de TTS.

Si intenta establecer **languageID** para un carácter y el archivo DLL de idioma del Agente para ese idioma no está instalado o no hay disponible una fuente de presentación para el identificador de idioma, el Agente genera un error y **LanguageID** permanece en su última configuración.

Al establecer esta propiedad no se produce un error si no hay motores de voz que coincidan con el idioma. Para determinar si hay un motor de voz compatible disponible para **LanguageID,** compruebe [**SRModeID**](srmodeid-property.md) [**o TTSModeID**](ttsmodeid-property.md). Si no establece **LanguageID**, se establecerá en la configuración predeterminada del identificador de idioma del usuario.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

> [!Note]  
> Si establece **LanguageID** en un idioma que admita texto bidireccional (como árabe o hebreo), pero el sistema que ejecuta la aplicación no tiene instalada la compatibilidad bidireccional, el texto del globo de palabras aparecerá en orden lógico en lugar de mostrarse.

 

## <a name="see-also"></a>Consulte también

[**Propiedad SRModeID**](srmodeid-property.md), [ **propiedad TTSModeID**](ttsmodeid-property.md)


 

 





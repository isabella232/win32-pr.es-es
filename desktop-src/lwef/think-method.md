---
title: Método Think
description: Método Think
ms.assetid: a188dd47-6af1-429d-af0a-69451f6b495e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c535912962a51961ae3f88f5cca412a55ecfa27506442aa78274fe697f2d7a26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975515"
---
# <a name="think-method"></a>Método Think

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Muestra el texto especificado para el carácter especificado en un globo de palabras "pensado".

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Think_ *  \[ *Text*\]



| Parte   | Descripción                                                       |
|--------|-------------------------------------------------------------------|
| *Texto* | Opcional. Cadena que especifica la salida de reflexión del carácter. |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Al igual [**que el método Speak,**](speak-method.md) el método **Think** es una solicitud  en cola que muestra texto en un globo de palabras, salvo que el globo de palabras think difiere visualmente. Además, el globo solo admite la etiqueta de control de voz Bookmark **\\ (Mrk**) y omite cualquier otra etiqueta de control de voz. A **diferencia de Speak**, el método **Think** no cambia el estado de animación del carácter.

Las [**propiedades del**](/windows/desktop/lwef/the-balloon-object) objeto Balloon afectan a la salida de los métodos [**Speak**](speak-method.md) **y Think.** Por ejemplo, la **propiedad Enabled** del objeto [**Balloon**](enabled-property.md) debe ser **True** para que se muestre el texto.

Si declara una referencia de objeto y la establece en este método, devuelve un [**objeto Request.**](/windows/desktop/lwef/the-request-object) Además, si el archivo no se ha  cargado, el [](status-property.md) servidor establece la propiedad Status del objeto Request en "failed" con un número de código de error adecuado.

La separación automática de palabras del agente en el globo de palabras interrumpe las palabras mediante caracteres de espacio en blanco (por ejemplo, espacio o tabulación). Sin embargo, si no es posible, puede interrumpir una palabra para ajustarse al globo. En idiomas como japonés, chino y tailandés, donde no se usan espacios para interrumpir palabras, inserte un carácter de espacio de ancho cero Unicode (0x200B) entre caracteres para definir saltos de palabras lógicos.

> [!Note]  
> Establezca el identificador de idioma del carácter antes de usar el [**método Speak**](speak-method.md) para asegurarse de que se muestra el texto adecuado en el globo de palabras.

 

 

 
---
title: Método de reflexión
description: Método de reflexión
ms.assetid: a188dd47-6af1-429d-af0a-69451f6b495e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a896c499e11aeaf50bfe9adc82a8330e61fc693
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904557"
---
# <a name="think-method"></a>Método de reflexión

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Muestra el texto especificado para el carácter especificado en un globo de palabra "pensamiento".

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("*** CharacterID * *").* *  \[ *Texto* de reflexión\]



| Parte   | Descripción                                                       |
|--------|-------------------------------------------------------------------|
| *Texto* | Opcional. Cadena que especifica la salida de pensamiento del carácter. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al igual que el método [**Speak**](speak-method.md) , el método de **reflexión** es una solicitud en cola que muestra texto en un globo de palabras, con la salvedad de que el globo de palabras de **reflexión** difiere visualmente. Además, el globo solo admite la etiqueta de control de voz de marcador (**\\ MRK**) y omite cualquier otra etiqueta de control de voz. A diferencia de **Speak**, el método de **reflexión** no cambia el estado de animación del carácter.

Las propiedades del objeto [**Balloon**](/windows/desktop/lwef/the-balloon-object) afectan a la salida de los métodos [**Speak**](speak-method.md) y **opina** . Por ejemplo, la propiedad [**Enabled**](enabled-property.md) del objeto **Balloon** debe ser **true** para que el texto se muestre.

Si declara una referencia de objeto y la establece en este método, devuelve un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) . Además, si no se ha cargado el archivo, el servidor establece la propiedad [**status**](status-property.md) del objeto **request** en "Failed" con un número de código de error adecuado.

La separación de palabras automática del agente en el globo de palabras rompe las palabras mediante caracteres de espacio en blanco (por ejemplo, espacio o tabulación). Sin embargo, si no es posible, puede romper una palabra para ajustarse al globo. En idiomas como el japonés, el chino y el tailandés, en los que no se usan espacios para romper palabras, inserte un carácter de espacio de cero (0x200B) de Unicode entre caracteres para definir saltos de palabra lógicos.

> [!Note]  
> Establezca el identificador de idioma del carácter antes de usar el método [**Speak**](speak-method.md) para asegurarse de que el texto se muestre correctamente en el globo de palabras.

 

 

 
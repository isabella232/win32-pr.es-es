---
description: Describe cómo se usan los ámbitos de entrada para el reconocimiento.
ms.assetid: 9faf6d22-b80d-4020-ac74-ee40b31ae9d4
title: Ámbitos de entrada y Factoids
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bbb46e21a0524f806daa4eed789fde31e285109
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279180"
---
# <a name="input-scopes-and-factoids"></a>Ámbitos de entrada y Factoids

Un ámbito de entrada es un conjunto definido de palabras, números, signos de puntuación y órdenes sintácticas que se permiten en un modelo de lenguaje determinado. Las aplicaciones pueden usar los ámbitos de entrada para restringir el modelo de lenguaje utilizado por el reconocedor a un contexto específico. Por ejemplo, un ámbito de entrada de es \_ SMTPEMAILADDRESS de correo electrónico \_ influye en los resultados de reconocimiento indicando que un campo específico es una dirección de correo electrónico. Por lo tanto, es probable que el campo contenga caracteres como " @" and " \_ " y que no contenga caracteres como " \* " y espacios.

> [!Note]  
> Otras tecnologías de Microsoft también usan ámbitos de entrada. Este artículo se centra en el uso de contexto para mejorar la precisión de los motores de reconocimiento de escritura a mano para aplicaciones de Tablet PC.

 

Las versiones anteriores de la API de tecnología de Tablet PC usaban Factoids para definir el contexto. A efectos prácticos, un Factoid es lo mismo que un ámbito de entrada. La versión uno de la plataforma del SDK de Tablet PC definía un conjunto de valores de Factoid en el objeto [**Factoid**](factoid-constants.md) . Estos valores se utilizaron para establecer el contexto e influir en los resultados del reconocimiento cuando se usa el objeto [**RecognizerContext**](inkrecognizercontext-class.md) para el reconocimiento. En el caso de los reconocedores de scripts latinos a partir de Windows XP Tablet PC Edition 2005, siga usando la propiedad [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) del objeto **RecognizerContext** para establecer el contexto, pero debe pasar un valor de ámbito de entrada, lista de frases o expresión regular de escritura a mano en lugar de uno de los valores de la versión uno Factoid. Los reconocedores de Microsoft de los caracteres de Asia oriental no admiten el uso de los valores enumerados del ámbito de entrada. Debe seguir usando los valores de Factoid para los reconocedores de los caracteres de Asia oriental.

Los ámbitos de entrada y Factoids son restricciones en los alternativos de nivel de palabra; los suplentes de caracteres pueden estar fuera del ámbito de entrada especificado incluso cuando se establece la marca de **coerción** .

Cuando la marca de **coerción** se establece con un Factoid restrictivo, puede suceder que el Reconocedor no pueda producir una respuesta que coincida con la tinta y satisfaga el valor de Factoid. Otro escenario en el que el reconocedor puede no producir ninguna respuesta satisfactoria es cuando el idioma del reconocedor no coincide con el idioma de la tinta (por ejemplo, el reconocedor de Inglés de EE. UU. y los caracteres de tinta en chino).

Cuando el reconocedor de escritura a mano no puede reconocer la tinta de una palabra o un carácter determinados, puede devolver una lista alternativa vacía o una lista alternativa en la que la primera opción es el punto de código 0xFFFF (carácter sin definir). Esto es especialmente útil en los modos de entrada de la guía de conversión boxing, donde se espera que cada cuadro con tinta tenga una lista no vacía de alternativas. A continuación, la aplicación puede mostrar este carácter no definido de cualquier manera que elija (por ejemplo, "???").

> [!Note]  
> Los valores de Factoid continúan funcionando con los reconocedores de alfabeto latino por compatibilidad con versiones anteriores.

 

Para obtener más información sobre Factoids, vea [establecer el contexto para los controles de Ink-Enabled](setting-context-for-ink-enabled-controls.md).

Para obtener información sobre los Factoids de Asia oriental, consulte [Factoids admitido de la versión 1](supported-factoids-from-version-1.md).

 

 




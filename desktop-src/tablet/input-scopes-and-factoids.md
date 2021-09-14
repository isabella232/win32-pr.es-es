---
description: Describe cómo se usan los ámbitos de entrada para el reconocimiento.
ms.assetid: 9faf6d22-b80d-4020-ac74-ee40b31ae9d4
title: Ámbitos de entrada y factoids
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bbb46e21a0524f806daa4eed789fde31e285109
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247755"
---
# <a name="input-scopes-and-factoids"></a>Ámbitos de entrada y factoids

Un ámbito de entrada es un conjunto definido de palabras, números, puntuación y ordenaciones sintácticas que se permiten dentro de un modelo de lenguaje determinado. Las aplicaciones pueden usar los ámbitos de entrada para restringir el modelo de lenguaje utilizado por el reconocedor a un contexto específico. Por ejemplo, un ámbito de entrada de IS \_ EMAIL SMTPEMAILADDRESS influye en los resultados del reconocimiento indicando que un campo específico \_ es una dirección de correo electrónico. Por lo tanto, es probable que el campo contenga caracteres como " ", y puede que no contenga caracteres @" and " \_ como " " " \* y espacios.

> [!Note]  
> Otras tecnologías de Microsoft también usan ámbitos de entrada. Este artículo se centra en el uso del contexto para mejorar la precisión de los motores de reconocimiento de escritura a mano para aplicaciones de tablet PC.

 

Las versiones anteriores de Tablet PC Technology API usaban factoids para definir el contexto. Para fines prácticos, un factoid es lo mismo que un ámbito de entrada. La versión uno de la plataforma del SDK de Tablet PC definió un conjunto de valores factoid en el [**objeto Factoid.**](factoid-constants.md) Estos valores se usaron para establecer el contexto e influir en los resultados del reconocimiento al usar el objeto [**RecognizerContext**](inkrecognizercontext-class.md) para el reconocimiento. Para los reconocedores de script latino a partir de Windows XP Tablet PC Edition 2005, sigue utilizando la propiedad [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) del objeto **RecognizerContext** para establecer el contexto, pero debe pasar un ámbito de entrada, una lista de frases o un valor de expresión regular de escritura a mano en lugar de uno de los valores factoid de la versión uno. Los reconocedores de Microsoft de caracteres de Este de Asia no admiten el uso de los valores enumerados del ámbito de entrada. Debe seguir usando valores factoid para reconocedores de caracteres de Este de Asia.

Los ámbitos de entrada y factoids son restricciones en las alternativas de nivel de palabra; Las alternativas de caracteres pueden estar fuera del ámbito de entrada especificado incluso cuando se establece la marca **COERCE.**

Cuando la **marca COERCE** se establece con un factoid restrictivo, puede ocurrir que el reconocedor no pueda generar una respuesta que coincida con la entrada de lápiz y satisfaga el factoid. Otro escenario en el que es posible que el reconocedor no produzca ninguna respuesta satisfactoria es cuando el idioma del reconocedor no coincide con el idioma de la entrada de lápiz (por ejemplo, el reconocedor de inglés de EE. UU. y los caracteres de lápiz chino).

Cuando el reconocedor de escritura a mano no puede reconocer la entrada de lápiz de una palabra o un carácter determinados, puede devolver una lista alternativa vacía o una lista alternativa en la que la primera opción sea el punto de código 0xffff (carácter no definido). Esto es especialmente útil en los modos de entrada de guía con caja, donde se espera que cada cuadro con entrada manuscrita tenga una lista no vacía de alternativas. A continuación, la aplicación puede mostrar este carácter indefinido de la manera que elija (por ejemplo, "???").

> [!Note]  
> Los valores factoid siguen funcionando con reconocedores de script latino por compatibilidad con versiones anteriores.

 

Para obtener más información sobre factoids, vea [Setting Context for Ink-Enabled Controls](setting-context-for-ink-enabled-controls.md).

Para obtener información sobre los factoids de Asia Oriental, vea [Supported Factoids from Version 1 ( Factoids admitidos de la versión 1).](supported-factoids-from-version-1.md)

 

 




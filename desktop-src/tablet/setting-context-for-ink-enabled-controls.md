---
description: Todo el reconocimiento de los controles habilitados para entrada de lápiz se produce a través de un objeto RecognizerContext. Las API de tecnología de Tablet PC permiten establecer la propiedad Factoid en un objeto RecognizerContext.
ms.assetid: 453993a7-f055-4d84-870c-256d1ec17731
title: Establecer contexto para Ink-Enabled controles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6776978834f030353a84c04f03e5ecf05ba060cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362962"
---
# <a name="setting-context-for-ink-enabled-controls"></a>Establecer contexto para Ink-Enabled controles

Todo el reconocimiento de los controles habilitados para entrada de lápiz se produce a través de [**un objeto RecognizerContext.**](inkrecognizercontext-class.md) Las API de tecnología de Tablet PC permiten establecer la [**propiedad Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) en un **objeto RecognizerContext.**

Si va a crear una aplicación habilitada para entrada de lápiz, use las propiedades [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) y [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) del objeto [**RecognizerContext**](inkrecognizercontext-class.md) para establecer contextos.

Puede pasar los valores de cadena de los nombres de los ámbitos de entrada definidos en la enumeración [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) a la [**propiedad Factoid,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) delimitada con una apertura (! y un cierre de ). Por ejemplo, para establecer el contexto de un objeto [**RecognizerContext**](inkrecognizercontext-class.md) en sesgo hacia los caracteres usados en una dirección URL, use la sintaxis que se muestra en los siguientes ejemplos de \# C:


```C++
theRecoContext.Factoid = "(!IS_URL)";
```



> [!Note]  
> Los ámbitos de entrada tal y como se definen en la enumeración [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) reemplazan a los factoids que estaban disponibles en versiones anteriores del SDK de la edición de PC para tabletas de Windows XP, aunque estos factoids seguirán funcionando para proporcionar compatibilidad con versiones anteriores.

 

En el siguiente ejemplo de C \# se establece la propiedad [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) para los códigos postales:


```C++
theRecognizerContext.Factoid = "(!IS_ADDRESS_POSTALCODE)";
```



Puede combinar ámbitos de entrada mediante la sintaxis de expresiones regulares de escritura a mano. Para obtener más información sobre el uso de la sintaxis de expresiones regulares, vea [Ámbitos de entrada personalizados con expresiones regulares.](custom-input-scopes-with-regular-expressions.md)

Puede establecer marcas de reconocimiento en el [**objeto RecognizerContext**](inkrecognizercontext-class.md) para que afecten al comportamiento del reconocedor. Una de estas marcas es **la marca Coerce** en la [**enumeración InkRecognitionModes**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes) de **RecognizerContext**. La **marca Coerce** obliga al reconocedor a devolver un resultado que coincida con la definición del factoid establecido. Por ejemplo, si tiene un formulario que requiere que el usuario escriba una cantidad numérica, puede ser útil establecer el factoid **IS \_ NUMBER** y establecer también la propiedad [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) en **Coerce**. En ese caso, la **marca Coerce** garantiza que el reconocedor devuelve solo números.

En el ejemplo de C \# siguiente se establece la propiedad [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) en **Coerce**:


```C++
theRecognizerContext.RecognitionFlags = RecognitionModes.Coerce;
```



Sin embargo, tenga cuidado al decidir establecer la **marca Coerce.** La marca fuerza al reconocedor a coincidir solo con la definición del factoid. Por ejemplo, si establece el ámbito de entrada IS TELEPHONE FULLTELEPHONENUMBER y la marca Coerce, el reconocedor devuelve resultados que coinciden exactamente con la definición del ámbito de entrada \_ \_ IS TELEPHONE  \_ \_ FULLTELEPHONENUMBER. Si un usuario escribe "911" con el ámbito de entrada IS TELEPHONE FULLTELEPHONENUMBER y la marca Coerce establecida, el reconocedor puede devolver una cadena vacía o una cadena aleatoria con el formato \_ \_ (XXX)  XXX-XXXX (donde X es un dígito). El formato xxx no coincide con la definición del factoid IS \_ TELEPHONE \_ FULLTELEPHONENUMBER, aunque sea un número de teléfono válido.

Para obtener listas de los formatos admitidos para cada ámbito de entrada, consulte la [**referencia inputScope.**](/windows/win32/api/inputscope/ne-inputscope-inputscope)

Para devolver un campo a la configuración predeterminada del reconocedor, establezca factoid en IS DEFAULT , como en \_ el ejemplo de C \# siguiente:


```C++
theRecgonizerContext.Factoid = "(!IS_DEFAULT)";
```



Para las aplicaciones que usan el control [InkEdit,](inkedit-control-reference.md) establezca el tipo factoid para el control especificando:


```C++
InkEdit1.Factoid = "(!IS_INPUTSCOPE)"
```



Donde `IS_INPUTSCOPE` es el nombre del ámbito de entrada que desea aplicar.

El control [InkEdit](inkedit-control-reference.md) no expone un [**objeto RecognizerContext.**](inkrecognizercontext-class.md) Todavía puede asignar contexto mediante la [**propiedad Factoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid) del control InkEdit, pero no puede establecer la **marca WORDMODE.**

 

 

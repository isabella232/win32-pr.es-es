---
description: Todo el reconocimiento de controles habilitados para tinta se produce a través de un objeto RecognizerContext. Las API de tecnología de Tablet PC permiten establecer la propiedad Factoid en un objeto RecognizerContext.
ms.assetid: 453993a7-f055-4d84-870c-256d1ec17731
title: Establecer el contexto para los controles de Ink-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6776978834f030353a84c04f03e5ecf05ba060cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361324"
---
# <a name="setting-context-for-ink-enabled-controls"></a>Establecer el contexto para los controles de Ink-Enabled

Todo el reconocimiento de controles habilitados para tinta se produce a través de un objeto [**RecognizerContext**](inkrecognizercontext-class.md) . Las API de tecnología de Tablet PC permiten establecer la propiedad [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) en un objeto **RecognizerContext** .

Si va a crear una aplicación habilitada para tinta, utilice las propiedades [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) y de la definición de [**palabras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) del objeto [**RecognizerContext**](inkrecognizercontext-class.md) para establecer contextos.

Puede pasar los valores de cadena de los nombres de los ámbitos de entrada definidos en la enumeración [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) a la propiedad [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) , delimitados por un carácter de apertura (! y un cierre). Por ejemplo, para establecer que el contexto de un objeto [**RecognizerContext**](inkrecognizercontext-class.md) se desvíe hacia los caracteres utilizados en una dirección URL, use la sintaxis que se muestra en los siguientes ejemplos de C \# :


```C++
theRecoContext.Factoid = "(!IS_URL)";
```



> [!Note]  
> Los ámbitos de entrada que se definen en la enumeración [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) reemplazan a los Factoids que estaban disponibles en versiones anteriores del SDK de Windows XP Tablet PC Edition, aunque estos Factoids seguirán funcionando para proporcionar compatibilidad con versiones anteriores.

 

En el siguiente ejemplo de C se \# establece la propiedad [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) para los códigos postales:


```C++
theRecognizerContext.Factoid = "(!IS_ADDRESS_POSTALCODE)";
```



Puede combinar ámbitos de entrada mediante la sintaxis de expresiones regulares de escritura a mano. Para obtener más información sobre el uso de la sintaxis de expresiones regulares, vea [ámbitos de entrada personalizados con expresiones regulares](custom-input-scopes-with-regular-expressions.md).

Puede establecer marcas de reconocimiento en el objeto [**RecognizerContext**](inkrecognizercontext-class.md) para que afecten al comportamiento del reconocedor. Una marca de este tipo es la marca de **coerción** en la enumeración [**InkRecognitionModes**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes) del **RecognizerContext**. La marca **coerción** obliga al reconocedor a devolver un resultado que coincide con la definición de Factoid que se establece. Por ejemplo, si tiene un formulario que requiere que el usuario escriba una cantidad numérica, puede que le resulte útil establecer el **\_ número** Factoid y también establecer la propiedad [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) en **forzar**. En esa instancia, la marca **forzar** garantiza que el reconocedor devuelva solo números.

En el siguiente \# ejemplo de C se establece la propiedad [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) en **coerción**:


```C++
theRecognizerContext.RecognitionFlags = RecognitionModes.Coerce;
```



Sin embargo, tenga cuidado al decidir establecer la marca de **coerción** . La marca fuerza al reconocedor a que solo coincida con la definición de Factoid. Por ejemplo, si establece el ámbito de \_ entrada de teléfono \_ FULLTELEPHONENUMBER y la marca de **coerción** , el reconocedor devuelve resultados que coinciden exactamente con la definición \_ del \_ solo ámbito de entrada de teléfono FULLTELEPHONENUMBER. Si un usuario escribe "911" con el \_ ámbito de entrada is Phone \_ FULLTELEPHONENUMBER y el indicador de **coerción** establecido, el reconocedor puede devolver una cadena vacía o una cadena aleatoria con el formato (XXX) XXX-XXXX (donde X es un dígito). El formato de XXX no coincide con la definición del \_ teléfono \_ FULLTELEPHONENUMBER Factoid, aunque es un número de teléfono válido.

Para obtener una lista de los formatos admitidos para cada ámbito de entrada, vea la referencia [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) .

Para devolver un campo a la configuración predeterminada del reconocedor, establezca Factoid en es el \_ valor predeterminado, como en el siguiente \# ejemplo de C:


```C++
theRecgonizerContext.Factoid = "(!IS_DEFAULT)";
```



En el caso de las aplicaciones que utilizan el control [InkEdit](inkedit-control-reference.md) , establezca el tipo Factoid para el control especificando:


```C++
InkEdit1.Factoid = "(!IS_INPUTSCOPE)"
```



Donde `IS_INPUTSCOPE` es el nombre del ámbito de entrada que desea aplicar.

El control [InkEdit](inkedit-control-reference.md) no expone un objeto [**RecognizerContext**](inkrecognizercontext-class.md) . Todavía puede asignar el contexto mediante la propiedad [**Factoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid) del control InkEdit, pero no puede establecer la marca **WORDMODE** .

 

 

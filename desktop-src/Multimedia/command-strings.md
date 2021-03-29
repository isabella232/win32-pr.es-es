---
title: Cadenas de comandos
description: Cadenas de comandos
ms.assetid: ca9ca153-f2bf-45ed-84e6-44e86e8efaed
keywords:
- Cadenas de comandos MCI, acerca de
- Cadenas de comandos MCI, sintaxis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b62013abff091f668a3b045e9f3ca2e8745f0d9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420549"
---
# <a name="command-strings"></a>Cadenas de comandos

Para enviar un comando de cadena a un dispositivo MCI, utilice la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) , que incluye los parámetros para el comando de cadena y un búfer para cualquier información devuelta.

La función **mciSendString** devuelve cero si es correcto. Si se produce un error en la función, la palabra de orden inferior del valor devuelto contiene un código de error. Este código de error se puede pasar a la función [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) para obtener una descripción de texto del error.

## <a name="syntax-of-command-strings"></a>Sintaxis de las cadenas de comandos

Las cadenas de comandos MCI usan una sintaxis de verbo-objeto-modificador coherente. Cada cadena de comandos incluye un comando, un identificador de dispositivo y argumentos de comando. Los argumentos son opcionales para algunos comandos y son necesarios para otros.

Una cadena de comandos tiene el formato siguiente:

*argumentos de identificador de dispositivo de comandos \_*

Estos componentes contienen la siguiente información:

-   El *comando* especifica un comando MCI, como [**abrir**](open.md), [**cerrar**](close.md)o [**reproducir**](play.md).
-   El *\_ identificador de dispositivo* identifica una instancia de un controlador MCI. El *\_ identificador de dispositivo* se crea al abrir el dispositivo.
-   Los *argumentos* especifican las marcas y las variables que usa el comando. Las marcas son palabras clave que se reconocen con el comando MCI. Las variables son números o cadenas que se aplican al comando MCI o a la marca.

    Por ejemplo, el comando **Play** usa los argumentos "from *Position* " y "to *Position* " para indicar las posiciones en las que iniciar y finalizar la reproducción. Puede enumerar las marcas que se usan con un comando en cualquier orden. Cuando se usa una marca que tiene una variable asociada, se debe proporcionar un valor para la variable.

    Los argumentos de comando no especificados (y opcionales) suponen un valor predeterminado.

La función de ejemplo siguiente envía el comando [**Play**](play.md) con las marcas "from" y "to".


```C++
BOOL PlayFromTo(LPTSTR lpstrAlias, DWORD dwFrom, DWORD dwTo) 
{ 
    TCHAR achCommandBuff[128]; 
    int result;
    MCIERROR err;

    // Form the command string.
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("play %s from %u to %u"), 
        lpstrAlias, dwFrom, dwTo); 

    if (result == -1)
    {
        return FALSE;
    }

    // Send the command string.
    err = mciSendString(achCommandBuff, NULL, 0, NULL); 
    if (err != 0)
    {
        return FALSE;
    }

    return TRUE;
} 
```



## <a name="data-types-for-command-variables"></a>Tipos de datos para variables de comando

Puede usar los siguientes tipos de datos para las variables de una cadena de comandos.



| **Tipo de datos**        | **Descripción**                                                                                                                                                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cadenas              | Los tipos de datos de cadena se delimitan mediante espacios en blanco y Comillas iniciales y finales. MCI quita las comillas simples de una cadena. Para colocar una comilla en una cadena, utilice un conjunto de dos comillas en las que desee insertar comillas. Para usar una cadena vacía, use dos comillas separadas por espacios en blanco iniciales y finales. |
| Enteros largos con signo | Los tipos de datos de entero largo con signo se delimitan mediante espacios en blanco iniciales y finales. A menos que se especifique lo contrario, los enteros pueden ser positivos o negativos. Si usa números enteros negativos, no debe separar el signo menos y el primer dígito con un espacio.                                                                                                    |
| Rectángulos           | Los tipos de datos de rectángulo son una lista ordenada de cuatro valores cortos firmados. El espacio en blanco delimita este tipo de datos y separa cada entero de la lista.                                                                                                                                                                                                              |



 

 

 
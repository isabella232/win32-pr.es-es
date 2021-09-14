---
title: Cadenas de comandos
description: Cadenas de comandos
ms.assetid: ca9ca153-f2bf-45ed-84e6-44e86e8efaed
keywords:
- Cadenas de comandos de MCI, acerca de
- Cadenas de comandos de MCI, sintaxis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b62013abff091f668a3b045e9f3ca2e8745f0d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069556"
---
# <a name="command-strings"></a>Cadenas de comandos

Para enviar un comando de cadena a un dispositivo MCI, use la función [**mciSendString,**](/previous-versions//dd757161(v=vs.85)) que incluye parámetros para el comando de cadena y un búfer para cualquier información devuelta.

La **función mciSendString** devuelve cero si se realiza correctamente. Si se produce un error en la función, la palabra de orden bajo del valor devuelto contiene un código de error. Puede pasar este código de error a la [**función mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) para obtener una descripción de texto del error.

## <a name="syntax-of-command-strings"></a>Sintaxis de cadenas de comandos

Las cadenas de comandos de MCI usan una sintaxis coherente de modificador de objeto verbo. Cada cadena de comando incluye un comando, un identificador de dispositivo y argumentos de comando. Los argumentos son opcionales para algunos comandos y son necesarios para otros.

Una cadena de comando tiene el formato siguiente:

*argumentos de \_ identificador de dispositivo de comando*

Estos componentes contienen la siguiente información:

-   El *comando* especifica un comando MCI, como [**abrir**](open.md), [**cerrar**](close.md)o [**reproducir**](play.md).
-   El *identificador \_ de dispositivo* identifica una instancia de un controlador MCI. El *identificador \_ de* dispositivo se crea cuando se abre el dispositivo.
-   Los *argumentos* especifican las marcas y variables utilizadas por el comando. Las marcas son palabras clave reconocidas con el comando MCI. Las variables son números o cadenas que se aplican al comando o marca MCI.

    Por ejemplo, el **comando play** usa los argumentos "from *position"* y "to *position"* para indicar las posiciones en las que se va a iniciar y finalizar la reproducción. Puede enumerar las marcas usadas con un comando en cualquier orden. Cuando se usa una marca que tiene una variable asociada, debe proporcionar un valor para la variable.

    Los argumentos de comando no especificados (y opcionales) asumen un valor predeterminado.

La siguiente función de ejemplo envía [**el comando play**](play.md) con las marcas "from" y "to".


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

Puede usar los siguientes tipos de datos para las variables de una cadena de comando.



| **Tipo de datos**        | **Descripción**                                                                                                                                                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cadenas              | Los tipos de datos de cadena se delimitan mediante comillas y espacios en blanco iniciales y finales. MCI quita las comillas simples de una cadena. Para colocar una comilla en una cadena, use un conjunto de dos comillas donde quiera insertar las comillas. Para usar una cadena vacía, use dos comillas delimitadas por espacios en blanco iniciales y finales. |
| Enteros largos con signo | Los tipos de datos enteros largos con signo se delimitan mediante espacios en blanco iniciales y finales. A menos que se especifique lo contrario, los enteros pueden ser positivos o negativos. Si usa enteros negativos, no debe separar el signo menos y el primer dígito con un espacio.                                                                                                    |
| Rectángulos           | Los tipos de datos rectangle son una lista ordenada de cuatro valores cortos con firma. El espacio en blanco delimita este tipo de datos y separa cada entero de la lista.                                                                                                                                                                                                              |



 

 

 
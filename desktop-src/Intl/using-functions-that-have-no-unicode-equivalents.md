---
description: Las funciones que no se han implementado con una versión Unicode normalmente se han reemplazado por funciones más eficaces o extendidas que admiten Unicode.
ms.assetid: 9e02c8fe-4fed-4b77-9b09-35850350859a
title: Usar funciones que no tienen equivalentes de Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0850eea442b98c81918c7c6733da65f730936be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279498"
---
# <a name="using-functions-that-have-no-unicode-equivalents"></a>Usar funciones que no tienen equivalentes de Unicode

Las funciones que no se han implementado con una versión [Unicode](unicode.md) normalmente se han reemplazado por funciones más eficaces o extendidas que admiten Unicode. Por ejemplo, si va a trasladar código que llama a la función [**OpenFile**](/windows/win32/api/winbase/nf-winbase-openfile) , la aplicación puede admitir Unicode mediante la función [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) en su lugar.

Si una función no tiene ningún equivalente Unicode, la aplicación puede asignar caracteres a y desde juegos de caracteres de 8 bits antes y después de la llamada de función. Por ejemplo, las funciones de formato de números **atoi** y **itoa** solo usan los dígitos del 0 al 9. Normalmente, la asignación de Unicode a caracteres de 8 bits provoca la pérdida de datos, pero esto se puede evitar haciendo que el tipo de código sea independiente y haga que las expresiones sean condicionales. Las instrucciones del ejemplo siguiente, escritas para caracteres de 8 bits, son dependientes del tipo y deben cambiarse para admitir Unicode.


```C++
char str[4] = "137";

int num = atoi(str);
```



Estas instrucciones se pueden volver a escribir de la siguiente manera para que sean independientes del tipo.


```C++
TCHAR tstr[4] = TEXT("137");

#ifdef UNICODE
size_t cCharsConverted;
CHAR strTmp[SIZE]; // SIZE equals (2*(sizeof(tstr)+1)). This ensures enough
                   // room for the multibyte characters if they are two 
                   // bytes long and a terminating null character. See Security 
                   // Alert below. 

wcstombs_s(&cCharsConverted, strTmp, sizeof(strTmp), (const wchar_t *)tstr, sizeof(strTmp));
num = atoi(strTmp);

#else

int num = atoi(tstr);

#endif 
```



En este ejemplo, la función de la biblioteca estándar de C **wcstombs** traduce Unicode a ASCII. El ejemplo se basa en el hecho de que los dígitos del 0 al 9 siempre se pueden traducir de Unicode a ASCII, incluso si parte del texto circundante no puede. La función **atoi** se detiene en cualquier carácter que no sea un dígito.

La aplicación puede utilizar la función de compatibilidad con National Language support (NLS) [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) para procesar texto que incluye los [dígitos nativos](digit-shapes.md) proporcionados para algunos de los scripts de Unicode.

> [!Caution]  
> El uso incorrecto de la función **wcstombs** puede poner en peligro la seguridad de la aplicación. Asegúrese de que el búfer de aplicación para la cadena de caracteres de 8 bits sea al menos de tamaño \* 2 *( \_ longitud de char* + 1), donde la *\_ longitud de char* representa la longitud de la cadena Unicode. Esta restricción se realiza porque, con [juegos de caracteres de doble byte](double-byte-character-sets.md) (DBCS), cada carácter Unicode se puede asignar a dos caracteres de 8 bits consecutivos. Si el búfer no contiene toda la cadena, la cadena de resultado no termina en null, lo que plantea un riesgo de seguridad. Para obtener más información acerca de la seguridad de las aplicaciones, vea [consideraciones de seguridad: características internacionales](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar Unicode y juegos de caracteres](using-unicode-and-character-sets.md)
</dt> </dl>

 

 

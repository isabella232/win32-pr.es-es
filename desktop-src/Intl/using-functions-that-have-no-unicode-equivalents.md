---
description: Las funciones que no se han implementado con una versión Unicode normalmente se han reemplazado por funciones más eficaces o extendidas que admiten Unicode.
ms.assetid: 9e02c8fe-4fed-4b77-9b09-35850350859a
title: Usar funciones que no tienen equivalentes Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e00781db9bce98c335c4a9071b9643ef5fdcb3716478cbffe12a5b53b33e2313
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787885"
---
# <a name="using-functions-that-have-no-unicode-equivalents"></a>Usar funciones que no tienen equivalentes Unicode

Las funciones que no se han implementado con una [versión Unicode](unicode.md) normalmente se han reemplazado por funciones más eficaces o extendidas que admiten Unicode. Por ejemplo, si va a portear código que llama a la función [**OpenFile,**](/windows/win32/api/winbase/nf-winbase-openfile) la aplicación puede admitir Unicode mediante la [**función CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) en su lugar.

Si una función no tiene ningún equivalente Unicode, la aplicación puede asignar caracteres a y desde juegos de caracteres de 8 bits antes y después de la llamada a la función. Por ejemplo, las funciones de formato numérico **atoi** e **itoa** solo usan los dígitos del 0 al 9. Normalmente, la asignación de Unicode a caracteres de 8 bits provoca la pérdida de datos, pero esto se puede evitar haciendo que el código sea independiente del tipo y que las expresiones sean condicionales. Las instrucciones del ejemplo siguiente, escritas para caracteres de 8 bits, dependen del tipo y deben cambiarse para admitir Unicode.


```C++
char str[4] = "137";

int num = atoi(str);
```



Estas instrucciones se pueden reescribir como se muestra a continuación para que sean independientes del tipo.


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



En este ejemplo, la función estándar de la biblioteca de C **wcstombs** traduce Unicode a ASCII. El ejemplo se basa en el hecho de que los dígitos del 0 al 9 siempre se pueden traducir de Unicode a ASCII, incluso si parte del texto circundante no puede. La **función atoi** se detiene en cualquier carácter que no sea un dígito.

La aplicación puede usar la función [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) de National Language [](digit-shapes.md) Support (NLS) para procesar texto que incluye los dígitos nativos proporcionados para algunos de los scripts en Unicode.

> [!Caution]  
> El uso incorrecto de la función **wcstombs** puede poner en peligro la seguridad de la aplicación. Asegúrese de que el búfer de aplicación para la cadena de caracteres de 8 bits tiene al menos el tamaño 2 (longitud de carácter +1), donde la longitud de char representa la longitud de la \* cadena Unicode.*\_* *\_* Esta restricción se realiza porque, con los juegos de caracteres de doble [byte](double-byte-character-sets.md) (DBCS), cada carácter Unicode se puede asignar a dos caracteres consecutivos de 8 bits. Si el búfer no contiene toda la cadena, la cadena de resultado no termina en NULL, lo que supone un riesgo de seguridad. Para obtener más información sobre la seguridad de las aplicaciones, vea [Security Considerations: International Features](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Unicode y juegos de caracteres](using-unicode-and-character-sets.md)
</dt> </dl>

 

 

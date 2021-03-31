---
description: Un valor del registro puede almacenar datos en varios formatos.
ms.assetid: 5fd828d6-4d62-4823-a2f1-15782b5cd28c
title: Tipos de valor del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adc653e69c514bc77323704485e88f0a57eebaae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910318"
---
# <a name="registry-value-types"></a>Tipos de valor del registro

Un valor del registro puede almacenar datos en varios formatos. Al almacenar datos en un valor del registro, por ejemplo, mediante una llamada a la función [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) , puede especificar uno de los valores siguientes para indicar el tipo de datos que se almacenan. Al recuperar un valor del registro, las funciones como [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) usan estos valores para indicar el tipo de datos recuperados.

Los siguientes tipos de valor del registro se definen en Winnt. h.



| Value                                 | Tipo                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_binario de reg<br/>                | Datos binarios en cualquier formato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| \_valor DWORD reg<br/>                 | Número de 32 bits.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| REG \_ DWORD \_ Little \_ endian<br/> | Número de 32 bits en formato Little-Endian.<br/> Windows está diseñado para ejecutarse en arquitecturas de equipos Little-Endian. Por lo tanto, este valor se define como REG \_ DWORD en los archivos de encabezado de Windows.<br/>                                                                                                                                                                                                                          |
| REG \_ DWORD \_ Big \_ endian<br/>    | Número de 32 bits en formato Big-Endian.<br/> Algunos sistemas UNIX admiten arquitecturas big-endian.<br/>                                                                                                                                                                                                                                                                                                                         |
| REG \_ expandir \_ SZ<br/>            | Una cadena terminada en null que contiene referencias no expandidas a variables de entorno (por ejemplo, "% PATH%"). Será una cadena ANSI o Unicode en función de si se utilizan las funciones Unicode o ANSI. Para expandir las referencias a variables de entorno, utilice la función [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) .<br/>                                                                                 |
| \_vínculo reg<br/>                  | Una cadena Unicode terminada en null que contiene la ruta de acceso de destino de un vínculo simbólico que se creó mediante una llamada a la función [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) con la \_ opción reg \_ Create \_ Link.<br/>                                                                                                                                                                                                                          |
| REG \_ multi \_ SZ<br/>             | Secuencia de cadenas terminadas en null, terminada en una cadena vacía ( \\ 0).<br/> A continuación se muestra un ejemplo:<br/> *Cadena1* \\ 0 *cadena2* \\ 0 *String3* \\ 0 *LastString* \\ 0 \\ 0<br/> El primer \\ 0 finaliza la primera cadena, el segundo en el último \\ 0 finaliza la última cadena y el \\ 0 final finaliza la secuencia. Tenga en cuenta que el terminador final se debe factorizar en la longitud de la cadena.<br/> |
| REG \_ ninguno<br/>                  | No hay ningún tipo de valor definido.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| QWord de REG \_<br/>                 | Número de 64 bits.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| REG \_ QWord \_ Little \_ endian<br/> | Número de 64 bits en formato Little-Endian.<br/> Windows está diseñado para ejecutarse en arquitecturas de equipos Little-Endian. Por lo tanto, este valor se define como REG \_ QWord en los archivos de encabezado de Windows.<br/>                                                                                                                                                                                                                          |
| Registro \_ SZ<br/>                    | Una cadena terminada en null. Será una cadena Unicode o ANSI, en función de si se utilizan las funciones Unicode o ANSI.<br/>                                                                                                                                                                                                                                                                                       |



 

## <a name="string-values"></a>Valores de cadena

Si los datos tienen el \_ tipo REG SZ, REG \_ multi \_ SZ o REG \_ Expand \_ Type, es posible que la cadena no se haya almacenado con los caracteres nulos de terminación correctos. Por lo tanto, al leer una cadena del registro, debe asegurarse de que la cadena se termina correctamente antes de usarla. de lo contrario, puede sobrescribir un búfer. (Tenga en cuenta que REG \_ Las \_ cadenas de varios SZ deben tener dos caracteres nulos de terminación).

Al escribir una cadena en el registro, debe especificar la longitud de la cadena, incluido el carácter nulo de terminación ( \\ 0). Un error común es usar la función **strlen** para determinar la longitud de la cadena, pero para olvidar que **strlen** devuelve solo el número de caracteres de la cadena, sin incluir el carácter null de terminación. Por lo tanto, la longitud de la cadena debe calcularse de la siguiente manera: `strlen( string ) + 1`

Una \_ cadena reg multi \_ SZ termina con una cadena de longitud 0. Por lo tanto, no es posible incluir una cadena de longitud cero en la secuencia. Una secuencia vacía se definiría de la siguiente manera: \\ 0.

En el ejemplo siguiente se recorre una \_ cadena de tipo REG multi \_ .


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

void SampleSzz(PTSTR pszz)
{
   _tprintf(_TEXT("\tBegin multi-sz string\n"));
   while (*pszz) 
   {
      _tprintf(_TEXT("\t\t%s\n"), pszz);
      pszz = pszz + _tcslen(pszz) + 1;
   }
   _tprintf(_TEXT("\tEnd multi-sz\n"));
}

int __cdecl main(int argc, char **argv)
{
   // Because the compiler adds a \0 at the end of quoted strings, 
   // there are two \0 terminators at the end. 

   _tprintf(_TEXT("Conventional multi-sz string:\n"));  
   SampleSzz(_TEXT("String1\0String2\0String3\0LastString\0"));

   _tprintf(_TEXT("\nTest case with no strings:\n"));  
   SampleSzz(_TEXT(""));

   return 0;
}
```



## <a name="byte-formats"></a>Formatos de bytes

En el *formato Little-Endian*, se almacena un valor de varios bytes en la memoria desde el byte más bajo (el "pequeño extremo") hasta el byte más alto. Por ejemplo, el valor 0x12345678 se almacena como (0x78 0x56 0x34 0X12) en formato Little-Endian.

En el *formato Big-Endian*, se almacena un valor de varios bytes en la memoria desde el byte más alto (el "Big end") hasta el byte más bajo. Por ejemplo, el valor 0x12345678 se almacena como (0X12 0x34 0x56 0x78) en formato Big-Endian.

 


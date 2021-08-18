---
description: Un valor del Registro puede almacenar datos en varios formatos.
ms.assetid: 5fd828d6-4d62-4823-a2f1-15782b5cd28c
title: Tipos de valor del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed2bc73e03d9aab8d39bdda31ab308af1749f22315a262ceb4ae28ec743c8c69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885022"
---
# <a name="registry-value-types"></a>Tipos de valor del Registro

Un valor del Registro puede almacenar datos en varios formatos. Al almacenar datos en un valor del Registro, por ejemplo, mediante una llamada a la función [**RegSetValueEx,**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) puede especificar uno de los valores siguientes para indicar el tipo de datos que se almacenan. Cuando se recupera un valor del Registro, funciones como [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) usan estos valores para indicar el tipo de datos recuperados.

Los siguientes tipos de valor del Registro se definen en Winnt.h.



| Valor                                 | Tipo                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| REG \_ BINARY<br/>                | Datos binarios en cualquier formato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| REG \_ DWORD<br/>                 | Número de 32 bits.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| REG \_ DWORD \_ LITTLE \_ ENDIAN<br/> | Número de 32 bits en formato little-endian.<br/> Windows está diseñado para ejecutarse en arquitecturas de equipos little-endian. Por lo tanto, este valor se define como REG \_ DWORD en los Windows de encabezado.<br/>                                                                                                                                                                                                                          |
| REG \_ DWORD \_ BIG \_ ENDIAN<br/>    | Número de 32 bits en formato big-endian.<br/> Algunos UNIX admiten arquitecturas big-endian.<br/>                                                                                                                                                                                                                                                                                                                         |
| REG \_ EXPAND \_ SZ<br/>            | Cadena terminada en NULL que contiene referencias sin explorar a variables de entorno (por ejemplo, "%PATH%"). Será una cadena Unicode o ANSI en función de si se usan las funciones Unicode o ANSI. Para expandir las referencias de variables de entorno, use [**la función ExpandEnvironmentStrings.**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa)<br/>                                                                                 |
| REG \_ LINK<br/>                  | Cadena Unicode terminada en NULL que contiene la ruta de acceso de destino de un vínculo simbólico que se creó mediante una llamada a la [**función RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) con REG \_ OPTION CREATE \_ \_ LINK.<br/>                                                                                                                                                                                                                          |
| REG \_ MULTI \_ SZ<br/>             | Secuencia de cadenas terminadas en NULL, terminadas por una cadena vacía ( \\ 0).<br/> A continuación se muestra un ejemplo:<br/> *String1* \\ 0 *String2* \\ 0 *String3* \\ 0 *LastString* \\ 0 \\ 0<br/> El primer 0 finaliza la primera cadena, el segundo hasta el último 0 finaliza la última cadena y el \\ \\ 0 final \\ finaliza la secuencia. Tenga en cuenta que el terminador final debe tenerse en cuenta en la longitud de la cadena.<br/> |
| REG \_ NONE<br/>                  | No hay ningún tipo de valor definido.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| REG \_ QWORD<br/>                 | Número de 64 bits.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| REG \_ QWORD \_ LITTLE \_ ENDIAN<br/> | Número de 64 bits en formato little-endian.<br/> Windows está diseñado para ejecutarse en arquitecturas de equipos little-endian. Por lo tanto, este valor se define como REG \_ QWORD en los archivos Windows encabezado.<br/>                                                                                                                                                                                                                          |
| REG \_ SZ<br/>                    | Una cadena terminada en null. Se trata de una cadena Unicode o ANSI, en función de si se usan las funciones Unicode o ANSI.<br/>                                                                                                                                                                                                                                                                                       |



 

## <a name="string-values"></a>Valores de cadena

Si los datos tienen el tipo REG SZ, REG MULTI SZ o REG EXPAND SZ, es posible que la cadena no se haya almacenado con los caracteres \_ \_ NULL de \_ \_ \_ terminación adecuados. Por lo tanto, al leer una cadena del Registro, debe asegurarse de que la cadena se termina correctamente antes de usarlo. De lo contrario, puede sobrescribir un búfer. (Tenga en cuenta que REG \_ Las cadenas MULTI \_ SZ deben tener dos caracteres nulos de terminación).

Al escribir una cadena en el Registro, debe especificar la longitud de la cadena, incluido el carácter nulo de terminación ( \\ 0). Un error común es usar la función **strlen** para determinar la longitud de la cadena, pero olvidar que **strlen** devuelve solo el número de caracteres de la cadena, sin incluir el valor NULL final. Por lo tanto, la longitud de la cadena debe calcularse de la siguiente manera: `strlen( string ) + 1`

Una cadena REG \_ MULTI SZ termina con una cadena de longitud \_ 0. Por lo tanto, no es posible incluir una cadena de longitud cero en la secuencia. Una secuencia vacía se definiría de la siguiente manera: \\ 0.

En el ejemplo siguiente se recorre una \_ cadena REG MULTI \_ SZ.


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

En *formato little-endian,* un valor de varios bytes se almacena en memoria desde el byte más bajo (el "pequeño extremo") hasta el byte más alto. Por ejemplo, el valor 0x12345678 se almacena como (0x78 0x56 0x34 0x12) en formato little-endian.

En *formato big-endian,* un valor de varios bytes se almacena en memoria desde el byte más alto (el "big end") hasta el byte más bajo. Por ejemplo, el valor 0x12345678 se almacena como (0x12 0x34 0x56 0x78) en formato big-endian.

 


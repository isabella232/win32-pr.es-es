---
description: Proporciona una lista de scripts usados en la cadena Unicode especificada.
ms.assetid: 3ad23613-8d0c-432a-b352-637c373a0980
title: Función DownlevelGetStringScripts (Idndl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetStringScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: bc5a9fdaf3beb9e1c401943f923fa48bd9d4b44c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274695"
---
# <a name="downlevelgetstringscripts-function"></a>Función DownlevelGetStringScripts

Proporciona una lista de scripts usados en la cadena Unicode especificada.

> [!Note]  
> Esta función solo la usan las aplicaciones que se ejecutan en sistemas operativos Windows Vista. Su uso requiere el paquete de descarga. Las aplicaciones que solo se ejecutan Windows Vista y versiones posteriores deben llamar [**a GetStringScripts.**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)

 

## <a name="syntax"></a>Sintaxis


```C++
int DownlevelGetStringScripts(
  _In_  DWORD   dwFlags,
  _In_  LPCWSTR lpString,
  _In_  int     cchString,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Marcas que especifican opciones para la recuperación de scripts.



| Value                                                                                                                                                                                                  | Significado                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GSS_ALLOW_INHERITED_COMMON"></span><span id="gss_allow_inherited_common"></span><dl> <dt>**GSS \_ ALLOW \_ INHERITED \_ COMMON**</dt> </dl> | Recupere la información de script "Qaii" (INHERITED) y "Zyyy" (COMMON). Este valor no afecta al procesamiento de caracteres sin signo. Estos caracteres de la cadena de entrada siempre hacen que aparezca un "Zzzz" (script UNASSIGNED) en la cadena de script.<br/> |



 

> [!Note]  
> De forma predeterminada, esta función omite los caracteres heredados o comunes de la cadena Unicode de entrada. Si GSS ALLOW INHERITED COMMON no está establecido, ni \_ \_ "Qaii" ni "Zyyy" aparecerán en la cadena de script, incluso si la cadena de entrada contiene dichos \_ caracteres. Si GSS ALLOW INHERITED COMMON está establecido y la cadena de entrada contiene caracteres heredados o \_ \_ \_ comunes, "Qaii" o "Zyyy" aparecen en la cadena de script. Consulte la sección Comentarios.

 

</dd> <dt>

*lpString* \[ En\]
</dt> <dd>

Puntero a la cadena Unicode que se analizará.

</dd> <dt>

*cchString* \[ En\]
</dt> <dd>

Tamaño, en caracteres, de la cadena Unicode indicada por *lpString*. La aplicación establece este parámetro en -1 si la cadena termina en NULL. Si la aplicación establece este parámetro en 0, la función recupera una cadena Unicode nula (L" \\ 0") en *lpScripts* y devuelve 1.

</dd> <dt>

*lpScripts* \[ out\]
</dt> <dd>

Puntero a un búfer en el que esta función recupera una cadena terminada en NULL que representa una lista de scripts, utilizando la notación de 4 caracteres usada en [ISO 15924.](https://www.unicode.org/iso15924/iso15924-codes.html) Cada nombre de script consta de cuatro caracteres latinos y los nombres se recuperan en orden alfabético. Cada nombre, incluido el último, va seguido de un punto y coma.

Como alternativa, este parámetro puede contener **NULL si** *cchScripts* se establece en 0. En este caso, la función devuelve el tamaño necesario para el búfer de script.

</dd> <dt>

*cchScripts* \[ En\]
</dt> <dd>

Tamaño, en caracteres, para el búfer de script indicado por *lpScripts*.

Como alternativa, la aplicación puede establecer este parámetro en 0. En este caso, la función recupera **NULL en** *lpScripts* y devuelve el tamaño necesario para el búfer de script.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de caracteres recuperados en el búfer de salida, incluido un carácter nulo final, si se realiza correctamente y *cchScripts* se establece en un valor distinto de cero. La función devuelve 1 para indicar que no se ha encontrado ningún script, por ejemplo, cuando la cadena de entrada solo contiene caracteres COMMON o INHERITED y GSS ALLOW INHERITED COMMON no \_ \_ está \_ establecido. Dado que cada script encontrado agrega cinco caracteres (cuatro caracteres + delimitador), una operación matemática simple proporciona el recuento de scripts como (código de \_ retorno - 1) / 5.

Si la función se realiza correctamente y el valor de *cchScripts* es 0, el valor devuelto es el tamaño necesario, en caracteres incluido un carácter nulo de terminación, para el búfer de script. El número de scripts es el descrito anteriormente.

La función devuelve 0 si no se realiza correctamente. Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:

-   ERROR \_ BADDB. La función no pudo acceder a los datos. Normalmente, esta situación no debería producirse y suele indicar una instalación no correcta, un problema de disco o similar.
-   ERROR \_ BÚFER \_ INSUFICIENTE. Un tamaño de búfer proporcionado no era lo suficientemente grande o se estableció incorrectamente en **NULL.**
-   ERROR \_ MARCAS NO \_ VÁLIDAS. Los valores proporcionados para las marcas no eran válidos.
-   ERROR \_ PARÁMETRO \_ NO VÁLIDO. Cualquiera de los valores de parámetro no era válido.

## <a name="remarks"></a>Observaciones

Esta función es útil como parte de una estrategia para mitigar los problemas de seguridad relacionados con los nombres de [dominio internacionalizados (IDN).](handling-internationalized-domain-names--idns.md)

La determinación del script se basa en los valores de script publicados por Unicode Consortium en , salvo que los caracteres sin signo tienen el valor <https://www.unicode.org/Public/4.1.0/ucd/Scripts.txt> "Zzzz" (UNASSIGNED) en lugar de "Zyyy" (COMMON).

Estos son algunos ejemplos del comportamiento de esta función:



Cadena de entrada

*dwFlags*

*lpScripts*

Scripts

Microsoft.com

0

Latn;

Latín

Microsoft.com

GSS \_ ALLOW \_ INHERITED \_ COMMON

Latn; Zyyy;

Latin + Common

${ROWSPAN2}$Ni eño${REMOVE}$  

004E 0069 0241 006F

${ROWSPAN2}$GSS ALLOW \_ \_ INHERITED \_ COMMON${REMOVE}$  

${ROWSPAN2}$Latn;${REMOVE}$  

${ROWSPAN2}$Latin${REMOVE}$  

Usa LATIN SMALL LETTER N WITH TILDE

${ROWSPAN2}$Ni eño${REMOVE}$  

004E 0069 006E 0303 006F

${ROWSPAN2}$GSS ALLOW \_ \_ INHERITED \_ COMMON${REMOVE}$  

${ROWSPAN2}$Latn; Qaii;${REMOVE}$  

${ROWSPAN2}$Latin + Inherited${REMOVE}$  

Usa LA TILDE COMBINING

${ROWSPAN2}$Sp ️f${REMOVE}$  

0053 0070 043e 043e 0066

${ROWSPAN2}$0${REMOVE}$  

${ROWSPAN2}$Latn; Cyrl;${REMOVE}$  

${ROWSPAN2}$Latin + Cirílico${REMOVE}$  

Usa CYRILLIC SMALL LETTER O



U+f000

0

Zzzz;

Sin asignar



U+f000

GSS \_ ALLOW \_ INHERITED \_ COMMON

Zzzz;

Sin asignar



 

El archivo de encabezado y el archivo DLL necesarios forman parte de la descarga "Api de mitigación de nombres de dominio [internacionalizados (IDN)](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en%0A) de Microsoft", disponible en el Centro [de descarga de MSDN.](https://www.microsoft.com/?ref=go)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                                                                                 |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                                                                        |
| Redistribuible<br/>          | API de mitigación de nombres de dominio internacionalizados (IDN) de Microsoft en Windows XP (SP2 o posterior), Windows Server 2003 (SP1 o posterior) o Windows Vista<br/> |
| Encabezado<br/>                   | <dl> <dt>Idndl.h</dt> </dl>                                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Idndl.dll</dt> </dl>                                                                        |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Compatibilidad con idiomas nacionales](national-language-support.md)
</dt> <dt>

[Funciones de compatibilidad con idiomas nacionales](national-language-support-functions.md)
</dt> <dt>

[Control de nombres de dominio internacionalizados (IDN)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md)
</dt> <dt>

[**DownlevelVerifyScripts**](downlevelverifyscripts.md)
</dt> <dt>

[**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)
</dt> </dl>

 

 

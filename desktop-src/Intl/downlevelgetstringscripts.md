---
description: Proporciona una lista de los scripts usados en la cadena Unicode especificada.
ms.assetid: 3ad23613-8d0c-432a-b352-637c373a0980
title: Función DownlevelGetStringScripts (Idndl. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688346"
---
# <a name="downlevelgetstringscripts-function"></a>DownlevelGetStringScripts función)

Proporciona una lista de los scripts usados en la cadena Unicode especificada.

> [!Note]  
> Esta función solo la usan las aplicaciones que se ejecutan en sistemas operativos anteriores a Windows Vista. Su uso requiere el paquete de descarga. Las aplicaciones que solo se ejecutan en Windows Vista y versiones posteriores deben llamar a [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts).

 

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

*dwFlags* \[ de\]
</dt> <dd>

Marcas que especifican las opciones para la recuperación del script.



| Value                                                                                                                                                                                                  | Significado                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GSS_ALLOW_INHERITED_COMMON"></span><span id="gss_allow_inherited_common"></span><dl> <dt>**GSS \_ permitir \_ herencia \_ común**</dt> </dl> | Recupere la información de script "Qaii" (HEREDAda) y "Zyyy" (común). Este valor no afecta al procesamiento de caracteres sin asignar. Estos caracteres de la cadena de entrada siempre provocan que aparezca un "ZZZZ" (script sin asignar) en la cadena de script.<br/> |



 

> [!Note]  
> De forma predeterminada, esta función omite cualquier carácter común o heredado en la cadena de entrada Unicode. Si \_ \_ no se establece GSS allow perherited \_ Common, no se mostrarán "Qaii" ni "Zyyy" en la cadena de script, aunque la cadena de entrada contenga dichos caracteres. Si \_ \_ se establece GSS allow perherited \_ Common, y si la cadena de entrada contiene caracteres heredados o comunes, "Qaii" y/o "Zyyy" aparecen en la cadena de script. Consulte la sección Comentarios.

 

</dd> <dt>

*lpString* \[ de\]
</dt> <dd>

Puntero a la cadena Unicode que se va a analizar.

</dd> <dt>

*cchString* \[ de\]
</dt> <dd>

Tamaño, en caracteres, de la cadena Unicode indicada por *lpString*. La aplicación establece este parámetro en-1 si la cadena termina en NULL. Si la aplicación establece este parámetro en 0, la función recupera una cadena Unicode nula (L " \\ 0") en *lpScripts* y devuelve 1.

</dd> <dt>

*lpScripts* \[ enuncia\]
</dt> <dd>

Puntero a un búfer en el que esta función recupera una cadena terminada en null que representa una lista de scripts, utilizando la notación de 4 caracteres utilizada en [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html). Cada nombre de script consta de cuatro caracteres latinos y los nombres se recuperan en orden alfabético. Cada nombre, incluido el último, va seguido de un punto y coma.

Como alternativa, este parámetro puede contener un **valor null** si *cchScripts* se establece en 0. En este caso, la función devuelve el tamaño necesario para el búfer de script.

</dd> <dt>

*cchScripts* \[ de\]
</dt> <dd>

Tamaño, en caracteres, para el búfer de script indicado por *lpScripts*.

Como alternativa, la aplicación puede establecer este parámetro en 0. En este caso, la función recupera **null** en *lpScripts* y devuelve el tamaño requerido para el búfer de script.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de caracteres recuperados en el búfer de salida, incluido un carácter nulo de terminación, si es correcto y *cchScripts* está establecido en un valor distinto de cero. La función devuelve 1 para indicar que no se ha encontrado ningún script, por ejemplo, cuando la cadena de entrada solo contiene caracteres comunes o HEREDAdos y \_ \_ no se ha establecido GSS allow perherited \_ Common. Dado que cada script encontrado agrega cinco caracteres (cuatro caracteres + delimitador), una operación matemática simple proporciona el número de scripts como (código devuelto \_ -1)/5.

Si la función se ejecuta correctamente y el valor de *cchScripts* es 0, el valor devuelto es el tamaño necesario, en caracteres que incluye un carácter nulo de terminación, para el búfer de script. El número de scripts es como se describió anteriormente.

La función devuelve 0 si no se realiza correctamente. Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:

-   ERROR \_ BADDB. La función no pudo obtener acceso a los datos. Esta situación no debería producirse normalmente y normalmente indica una instalación incorrecta, un problema de disco o un tipo similar.
-   ERROR \_ de \_ búfer insuficiente. Un tamaño de búfer proporcionado no era lo suficientemente grande o se estableció incorrectamente en **null**.
-   ERROR en \_ marcas no válidas \_ . Los valores proporcionados para marcas no eran válidos.
-   ERROR \_ de \_ parámetro no válido. Cualquiera de los valores de parámetro no era válido.

## <a name="remarks"></a>Observaciones

Esta función es útil como parte de una estrategia para mitigar los problemas de seguridad relacionados con [los nombres de dominio internacionalizados (IDN)](handling-internationalized-domain-names--idns.md).

La determinación del script se basa en los valores de script publicados por Unicode Consortium en <https://www.unicode.org/Public/4.1.0/ucd/Scripts.txt> , excepto en que los caracteres sin asignar tienen el valor "ZZZZ" (sin asignar) en lugar de "Zyyy" (común).

Estos son algunos ejemplos del comportamiento de esta función:



Cadena de entrada

*dwFlags*

*lpScripts*

Scripts

Microsoft.com

0

LATN

Latín

Microsoft.com

GSS \_ permitir \_ herencia \_ común

LATN Zyyy;

Latín + común

$ {ROWSPAN2} $Ni ño $ {REMOVE} $  

004E 0069 0241 006F

$ {ROWSPAN2} $GSS \_ permitir \_ \_ Common $ {Remove} $ heredado  

$ {ROWSPAN2} $Latn; $ {REMOVE} $  

$ {ROWSPAN2} $Latin $ {REMOVE} $  

Usa letra latina minúscula N con TILDE

$ {ROWSPAN2} $Ni ño $ {REMOVE} $  

004E 0069 006E 0303 006F

$ {ROWSPAN2} $GSS \_ permitir \_ \_ Common $ {Remove} $ heredado  

$ {ROWSPAN2} $Latn; Qaii; $ {REMOVE} $  

$ {ROWSPAN2} $Latin + heredado $ {REMOVE} $  

Usa TILDE de combinación

$ {ROWSPAN2} $Sp ооf $ {REMOVE} $  

0053 0070 043e 043e 0066

$ {ROWSPAN2} $0 $ {REMOVE} $  

$ {ROWSPAN2} $Latn; Cyrl; $ {REMOVE} $  

$ {ROWSPAN2} $Latin + cirílico $ {REMOVE} $  

Usa letra minúscula cirílica O



U + F000

0

ZZZZ

Sin asignar



U + F000

GSS \_ permitir \_ herencia \_ común

ZZZZ

Sin asignar



 

El archivo de encabezado y DLL necesarios forman parte de la descarga ["API de mitigación de nombres de dominio internacionalizados (IDN) de Microsoft"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en%0A) , disponible en el [centro de descarga de MSDN](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                                                                                 |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                                                                        |
| Redistribuible<br/>          | API de mitigación de nombres de dominio internacionalizados (IDN) de Microsoft en Windows XP (SP2 o posterior), Windows Server 2003 (SP1 o posterior) o Windows Vista<br/> |
| Encabezado<br/>                   | <dl> <dt>Idndl. h</dt> </dl>                                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Idndl.dll</dt> </dl>                                                                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con National Language](national-language-support.md)
</dt> <dt>

[Funciones de soporte de National Language](national-language-support-functions.md)
</dt> <dt>

[Administrar nombres de dominio internacionalizados (IDN)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md)
</dt> <dt>

[**DownlevelVerifyScripts**](downlevelverifyscripts.md)
</dt> <dt>

[**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)
</dt> </dl>

 

 

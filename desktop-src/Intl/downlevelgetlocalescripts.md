---
description: Proporciona una lista de scripts para la configuración regional especificada.
ms.assetid: 0cedcf6c-bab4-4e0f-ab8f-04aa8e51602f
title: Función DownlevelGetLocaleScripts (Idndl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetLocaleScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: f636ab426cd4d50878df93e3e30d69de54d60ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278612"
---
# <a name="downlevelgetlocalescripts-function"></a>DownlevelGetLocaleScripts función)

Proporciona una lista de scripts para la configuración regional especificada.

> [!Note]  
> Esta función solo la usan las aplicaciones que se ejecutan en sistemas operativos anteriores a Windows Vista. Su uso requiere el paquete de descarga. Las aplicaciones que solo se ejecutan en Windows Vista y versiones posteriores deben llamar a [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) con *LCType* establecido en [ \_ SSCRIPTS de configuración regional](locale-sscripts.md).

 

## <a name="syntax"></a>Sintaxis


```C++
int DownlevelGetLocaleScripts(
  _In_  LPCWSTR lpLocaleName,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpLocaleName* \[ de\]
</dt> <dd>

Puntero a un [nombre de configuración regional](locale-names.md)terminada en NULL.

</dd> <dt>

*lpScripts* \[ enuncia\]
</dt> <dd>

Puntero a un búfer en el que esta función recupera una cadena terminada en null que representa una lista de scripts, utilizando la notación de 4 caracteres utilizada en [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html). Cada nombre de script consta de cuatro caracteres latinos y los nombres se recuperan en orden alfabético. Cada una de ellas, incluida la última, va seguida de un punto y coma.

Como alternativa, este parámetro puede contener un **valor null** si *cchScripts* está establecido en 0. En este caso, la función devuelve el tamaño necesario para el búfer de script.

</dd> <dt>

*cchScripts* \[ de\]
</dt> <dd>

Tamaño, en caracteres, para el búfer de script indicado por *lpScripts*.

Como alternativa, la aplicación puede establecer este parámetro en 0. En este caso, la función recupera **null** en *lpScripts* y devuelve el tamaño requerido para el búfer de script.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de caracteres recuperados en el búfer de script, incluido el carácter nulo de terminación. Si la función se ejecuta correctamente y el valor de *cchScripts* es 0, el valor devuelto es el tamaño necesario, en caracteres que incluye un carácter nulo de terminación, para el búfer de script.

Esta función devuelve 0 si no se realiza correctamente. Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:

-   ERROR \_ BADDB. La función no pudo obtener acceso a los datos. Esta situación no debería producirse normalmente y normalmente indica una instalación incorrecta, un problema de disco o un tipo similar.
-   ERROR \_ de \_ búfer insuficiente. Un tamaño de búfer proporcionado no era lo suficientemente grande o se estableció incorrectamente en **null**.
-   ERROR \_ de \_ parámetro no válido. Cualquiera de los valores de parámetro no era válido.

## <a name="remarks"></a>Observaciones

Esta función es útil como parte de una estrategia para mitigar los problemas de seguridad relacionados con [los nombres de dominio internacionalizados (IDN)](handling-internationalized-domain-names--idns.md).

Estos son algunos ejemplos de entradas y salidas para esta función, suponiendo un tamaño de búfer suficiente:



| Configuración regional                  | *lpLocaleName* | *lpScripts*     |
|-------------------------|----------------|-----------------|
| Spanish (Traditional Sort) - Spain | es-ES          | LATN           |
| Hindi (India)           | hi-IN          | Deva           |
| Japonés (Japón)        | ja-JP          | Hani; Hira; Kana |



 

La lista no contiene el script Latino a menos que sea una parte esencial del sistema de escritura usado para una configuración regional. Sin embargo, los caracteres latinos se suelen usar en el contexto de configuraciones regionales para las que no son nativos, como en el caso de un nombre empresarial extranjero. En el ejemplo anterior de Hindi en India, el único script recuperado es "Deva" (para devanagari), aunque los caracteres latinos también pueden aparecer en texto Hindi. La función [**DownlevelVerifyScripts**](downlevelverifyscripts.md) tiene una marca especial para abordar ese caso.

El archivo de encabezado y DLL necesarios forman parte de la descarga ["API de mitigación de nombres de dominio internacionalizados (IDN) de Microsoft"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) , disponible en el [centro de descarga de MSDN](https://www.microsoft.com/?ref=go).

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

[**DownlevelGetStringScripts**](downlevelgetstringscripts.md)
</dt> <dt>

[**DownlevelVerifyScripts**](downlevelverifyscripts.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 

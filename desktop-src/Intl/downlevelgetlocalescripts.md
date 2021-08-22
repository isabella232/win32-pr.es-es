---
description: Proporciona una lista de scripts para la configuración regional especificada.
ms.assetid: 0cedcf6c-bab4-4e0f-ab8f-04aa8e51602f
title: Función DownlevelGetLocaleScripts (Idndl.h)
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
ms.openlocfilehash: 02631a605f67f3c27dfcc29c1e660ca24e56b6072d4490ba8ba090ebdd8b9019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068255"
---
# <a name="downlevelgetlocalescripts-function"></a>Función DownlevelGetLocaleScripts

Proporciona una lista de scripts para la configuración regional especificada.

> [!Note]  
> Esta función solo la usan las aplicaciones que se ejecutan en sistemas operativos Windows Vista. Su uso requiere el paquete de descarga. Las aplicaciones que solo se ejecutan Windows Vista y versiones posteriores deben llamar a [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) con *LCType* establecido en [LOCALE \_ SSCRIPTS](locale-sscripts.md).

 

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

*lpLocaleName* \[ En\]
</dt> <dd>

Puntero a un nombre de [configuración regional terminada en NULL.](locale-names.md)

</dd> <dt>

*lpScripts* \[ out\]
</dt> <dd>

Puntero a un búfer en el que esta función recupera una cadena terminada en NULL que representa una lista de scripts, utilizando la notación de 4 caracteres usada en [ISO 15924.](https://www.unicode.org/iso15924/iso15924-codes.html) Cada nombre de script consta de cuatro caracteres latinos y los nombres se recuperan en orden alfabético. Cada uno de ellos, incluido el último, va seguido de un punto y coma.

Como alternativa, este parámetro puede contener **NULL si** *cchScripts* está establecido en 0. En este caso, la función devuelve el tamaño necesario para el búfer de script.

</dd> <dt>

*cchScripts* \[ En\]
</dt> <dd>

Tamaño, en caracteres, para el búfer de script indicado por *lpScripts*.

Como alternativa, la aplicación puede establecer este parámetro en 0. En este caso, la función recupera **NULL en** *lpScripts* y devuelve el tamaño necesario para el búfer de script.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de caracteres recuperados en el búfer de script, incluido el carácter nulo final. Si la función se ejecuta correctamente y el valor de *cchScripts* es 0, el valor devuelto es el tamaño necesario, en caracteres incluido un carácter nulo de terminación, para el búfer de script.

Esta función devuelve 0 si no se realiza correctamente. Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:

-   ERROR \_ BADDB. La función no pudo acceder a los datos. Esta situación no debería producirse normalmente y normalmente indica una instalación no correcta, un problema de disco o similar.
-   ERROR \_ BÚFER \_ INSUFICIENTE. Un tamaño de búfer proporcionado no era lo suficientemente grande o se estableció incorrectamente en **NULL.**
-   ERROR \_ PARÁMETRO \_ NO VÁLIDO. Cualquiera de los valores de parámetro no era válido.

## <a name="remarks"></a>Comentarios

Esta función es útil como parte de una estrategia para mitigar los problemas de seguridad relacionados con los nombres de [dominio internacionalizados (IDN).](handling-internationalized-domain-names--idns.md)

Estos son algunos ejemplos de entradas y salidas para esta función, suponiendo un tamaño de búfer suficiente:



| Configuración regional                  | *lpLocaleName* | *lpScripts*     |
|-------------------------|----------------|-----------------|
| Spanish (Traditional Sort) - Spain | es-ES          | Latn;           |
| Hindi (India)           | hi-IN          | Deva;           |
| Japonés (Japón)        | ja-JP          | Hani; Hira; Kana; |



 

La lista no contiene el script latino a menos que sea una parte esencial del sistema de escritura utilizado para una configuración regional. Sin embargo, los caracteres latinos se usan a menudo en el contexto de configuraciones regionales para las que no son nativos, como para un nombre empresarial externo. En el ejemplo anterior de Hindi en la India, el único script recuperado es "Deva" (para Devadín), aunque los caracteres latinos también pueden aparecer en el texto de Hindi. La [**función DownlevelVerifyScripts**](downlevelverifyscripts.md) tiene una marca especial para abordar ese caso.

El archivo de encabezado y el archivo DLL necesarios forman parte de la descarga ["Microsoft Internationalized Domain Name (IDN) Mitigation API" (API](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) de mitigación de nombres de dominio internacionalizados de Microsoft), disponible en el Centro [de descarga de MSDN.](https://www.microsoft.com/?ref=go)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                                                                                 |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                                                                        |
| Redistribuible<br/>          | API de mitigación de nombres de dominio internacionalizados (IDN) de Microsoft en Windows XP (SP2 o posterior), Windows Server 2003 (SP1 o posterior) o Windows Vista<br/> |
| Header<br/>                   | <dl> <dt>Idndl.h</dt> </dl>                                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Idndl.dll</dt> </dl>                                                                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con idiomas nacionales](national-language-support.md)
</dt> <dt>

[Funciones de compatibilidad con idiomas nacionales](national-language-support-functions.md)
</dt> <dt>

[Control de nombres de dominio internacionalizados (IDN)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[**DownlevelGetStringScripts**](downlevelgetstringscripts.md)
</dt> <dt>

[**DownlevelVerifyScripts**](downlevelverifyscripts.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 

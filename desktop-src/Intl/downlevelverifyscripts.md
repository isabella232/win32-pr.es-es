---
description: Compara dos listas de scripts enumeradas.
ms.assetid: 3500ce36-75e4-4d61-8449-a65c99532326
title: Función DownlevelVerifyScripts (Idndl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelVerifyScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: 62e029576d53109e3c57faf4ec913472f8aea65e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668413"
---
# <a name="downlevelverifyscripts-function"></a>DownlevelVerifyScripts función)

Compara dos listas de scripts enumeradas.

> [!Note]  
> Esta función solo la usan las aplicaciones que se ejecutan en sistemas operativos anteriores a Windows Vista. Su uso requiere el paquete de descarga. Las aplicaciones que solo se ejecutan en Windows Vista y versiones posteriores deben llamar a [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).

 

## <a name="syntax"></a>Sintaxis


```C++
BOOL DownlevelVerifyScripts(
  _In_ DWORD   dwFlags,
  _In_ LPCWSTR lpLocaleScripts,
  _In_ int     cchLocaleScripts,
  _In_ LPCWSTR lpTestScripts,
  _In_ int     cchTestScripts
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Marcas que especifican las opciones de comprobación de script.



| Value                                                                                                                                                             | Significado                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="VS_ALLOW_LATIN"></span><span id="vs_allow_latin"></span><dl> <dt>**VS \_ permitir \_ latín**</dt> </dl> | Permitir "latn" (alfabeto latino) en la lista de pruebas, aunque no esté en la lista de configuraciones regionales.<br/> |



 

</dd> <dt>

*lpLocaleScripts* \[ de\]
</dt> <dd>

Puntero a la lista de configuraciones regionales, la lista enumerada de scripts para una configuración regional determinada. Esta lista se rellena normalmente mediante una llamada a [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md).

</dd> <dt>

*cchLocaleScripts* \[ de\]
</dt> <dd>

Tamaño, en caracteres, de la cadena indicada por *lpLocaleScripts*. La aplicación establece este parámetro en-1 si la cadena termina en NULL. Si este parámetro se establece en 0, se produce un error en la función.

</dd> <dt>

*lpTestScripts* \[ de\]
</dt> <dd>

Puntero a la lista de pruebas, una segunda lista enumerada de scripts. Esta lista se rellena normalmente mediante una llamada a [**DownlevelGetStringScripts**](downlevelgetstringscripts.md).

</dd> <dt>

*cchTestScripts* \[ de\]
</dt> <dd>

Tamaño, en caracteres, de la cadena indicada por *lpTestScripts*. La aplicación establece este parámetro en-1 si la cadena termina en NULL. Si este parámetro se establece en 0, se produce un error en la función.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si la lista de pruebas no está vacía y todos los elementos de la lista también se incluyen en la lista de configuraciones regionales. De lo contrario, la función devuelve **false**.

Un valor devuelto de **false** puede indicar que la lista de pruebas contiene un elemento que no está en la lista de configuraciones regionales o puede indicar un error. Para distinguir entre estos dos casos, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). Si **DownlevelVerifyScripts** ha determinado correctamente que hay un elemento en la lista de pruebas que no está en la lista de configuraciones regionales, **GETLASTERROR** devuelve el error \_ Success. De lo contrario, **GetLastError** puede devolver uno de los siguientes códigos de error:

-   ERROR en \_ marcas no válidas \_ . Los valores proporcionados para marcas no eran válidos.
-   ERROR \_ de \_ parámetro no válido. Cualquiera de los valores de parámetro no era válido.

## <a name="remarks"></a>Observaciones

Esta función compara cadenas, como "LATN; Cyrl; ", que consta de una serie de nombres de script de 4 caracteres, con cada nombre de script seguido de un punto y coma. También tiene un caso especial en el que se debe tener en cuenta el hecho de que el script Latino se usa a menudo en idiomas y configuraciones regionales para los que no es nativo.

Esta función es útil como parte de una estrategia para mitigar los problemas de seguridad relacionados con [los nombres de dominio internacionalizados (IDN)](handling-internationalized-domain-names--idns.md).

A continuación se muestran ejemplos de la devolución de esta función y una llamada subsiguiente a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) en varios escenarios. Los dos últimos ejemplos ilustran, respectivamente, un caso en el que la lista de pruebas carece de un punto y coma de terminación (cadena incorrecta) y un caso en el que la lista de pruebas está vacía.



| Cadena "locale" | Cadena "Test" | *dwFlags*        | Valor devuelto | Devolución de GetLastError       |
|-----------------|---------------|------------------|--------------|---------------------------|
| Hani; Hira; Kana | Hani;         | N/D              | **TRUE**     | N/D                       |
| Hani; Hira; Kana | Hani; LATN    | 0                | **FALSE**    | ERROR \_ correcto            |
| Hani; Hira; Kana | Hani; LATN    | VS \_ permitir \_ latín | **TRUE**     | N/D                       |
| Hani; Hira; Kana | Cyrl         | N/D              | **FALSE**    | ERROR \_ correcto            |
| Hani; Hira; Kana | Cyrl         | N/D              | **FALSE**    | ERROR \_ de \_ parámetro no válido |
| Hani; Hira; Kana |               | N/D              | **FALSE**    | ERROR \_ correcto            |



 

El archivo de encabezado y DLL necesarios forman parte de la descarga ["API de mitigación de nombres de dominio internacionalizados (IDN) de Microsoft"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) , disponible en el [centro de descarga de MSDN](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                                                                  |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                                                         |
| Redistribuible<br/>          | API de mitigación de nombres de dominio internacionalizados (IDN) de Microsoft Windows XP con SP2, Windows Server 2003 con SP1, orWindows vista<br/> |
| Encabezado<br/>                   | <dl> <dt>Idndl. h</dt> </dl>                                                           |
| Archivo DLL<br/>                      | <dl> <dt>Idndl.dll</dt> </dl>                                                         |



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

[**DownlevelGetStringScripts**](downlevelgetstringscripts.md)
</dt> <dt>

[**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)
</dt> </dl>

 

 

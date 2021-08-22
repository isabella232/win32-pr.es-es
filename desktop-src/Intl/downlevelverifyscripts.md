---
description: Compara dos listas enumeradas de scripts.
ms.assetid: 3500ce36-75e4-4d61-8449-a65c99532326
title: Función DownlevelVerifyScripts (Idndl.h)
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
ms.openlocfilehash: df0bdb1e8968d6bb044a3f270eb9200adf1ecaa54137fe3cface0e0898a9b5be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068245"
---
# <a name="downlevelverifyscripts-function"></a>Función DownlevelVerifyScripts

Compara dos listas enumeradas de scripts.

> [!Note]  
> Esta función solo la usan las aplicaciones que se ejecutan en sistemas operativos Windows Vista. Su uso requiere el paquete de descarga. Las aplicaciones que solo se ejecutan Windows Vista y versiones posteriores deben llamar [**a VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).

 

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

*dwFlags* \[ En\]
</dt> <dd>

Marcas que especifican las opciones de comprobación del script.



| Value                                                                                                                                                             | Significado                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="VS_ALLOW_LATIN"></span><span id="vs_allow_latin"></span><dl> <dt>**VS \_ ALLOW \_ LATIN**</dt> </dl> | Permita "Latn" (script latino) en la lista de pruebas, aunque no esté en la lista de configuración regional.<br/> |



 

</dd> <dt>

*lpLocaleScripts* \[ En\]
</dt> <dd>

Puntero a la lista de configuración regional, la lista enumerada de scripts para una configuración regional determinada. Normalmente, esta lista se rellena mediante una llamada a [**DownlevelGetLocaleScripts.**](downlevelgetlocalescripts.md)

</dd> <dt>

*cchLocaleScripts* \[ En\]
</dt> <dd>

Tamaño, en caracteres, de la cadena indicada por *lpLocaleScripts*. La aplicación establece este parámetro en -1 si la cadena termina en NULL. Si este parámetro se establece en 0, se produce un error en la función.

</dd> <dt>

*lpTestScripts* \[ En\]
</dt> <dd>

Puntero a la lista de pruebas, una segunda lista enumerada de scripts. Normalmente, esta lista se rellena mediante una llamada a [**DownlevelGetStringScripts.**](downlevelgetstringscripts.md)

</dd> <dt>

*cchTestScripts* \[ En\]
</dt> <dd>

Tamaño, en caracteres, de la cadena indicada por *lpTestScripts*. La aplicación establece este parámetro en -1 si la cadena termina en NULL. Si este parámetro se establece en 0, se produce un error en la función.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si la lista de pruebas no está vacía y todos los elementos de la lista también se incluyen en la lista de configuración regional. De lo contrario, la función **devuelve FALSE.**

Un valor devuelto de **FALSE** puede indicar que la lista de pruebas contiene un elemento que no está en la lista de configuración regional o puede indicar un error. Para distinguir entre estos dos casos, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). Si **DownlevelVerifyScripts** ha determinado correctamente que hay un elemento en la lista de pruebas que no está en la lista de configuración regional, **GetLastError** devuelve ERROR \_ SUCCESS. De lo contrario, **GetLastError** puede devolver uno de los siguientes códigos de error:

-   ERROR \_ MARCAS NO \_ VÁLIDAS. Los valores proporcionados para las marcas no eran válidos.
-   ERROR \_ PARÁMETRO \_ NO VÁLIDO. Cualquiera de los valores de parámetro no era válido.

## <a name="remarks"></a>Comentarios

Esta función compara cadenas, como "Latn; Cyrl;", que consta de una serie de nombres de script de 4 caracteres, con cada nombre de script seguido de un punto y coma. También tiene un caso especial para tener en cuenta el hecho de que el script latino se usa a menudo en idiomas y configuraciones regionales para los que no es nativo.

Esta función es útil como parte de una estrategia para mitigar los problemas de seguridad relacionados con los nombres de [dominio internacionalizados (IDN).](handling-internationalized-domain-names--idns.md)

A continuación se muestran ejemplos de la devolución de esta función y una llamada posterior a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) en varios escenarios. Los dos últimos ejemplos muestran, respectivamente, un caso en el que la lista de pruebas no tiene un punto y coma final (cadena con formato anterior) y un caso en el que la lista de pruebas está vacía.



| Cadena "Locale" | Cadena "Test" | *dwFlags*        | Valor devuelto | GetLastError return       |
|-----------------|---------------|------------------|--------------|---------------------------|
| Hani; Hira; Kana; | Hani;         | N/D              | **TRUE**     | N/D                       |
| Hani; Hira; Kana; | Hani; Latn;    | 0                | **FALSE**    | ERROR \_ CORRECTO            |
| Hani; Hira; Kana; | Hani; Latn;    | VS \_ ALLOW \_ LATIN | **TRUE**     | N/D                       |
| Hani; Hira; Kana; | Cyrl;         | N/D              | **FALSE**    | ERROR \_ CORRECTO            |
| Hani; Hira; Kana; | Cyrl;         | N/D              | **FALSE**    | ERROR \_ PARÁMETRO NO \_ VÁLIDO |
| Hani; Hira; Kana; |               | N/D              | **FALSE**    | ERROR \_ CORRECTO            |



 

El archivo de encabezado y el archivo DLL necesarios forman parte de la descarga ["Microsoft Internationalized Domain Name (IDN) Mitigation API" (API](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) de mitigación de nombres de dominio internacionalizados de Microsoft), disponible en el Centro [de descarga de MSDN.](https://www.microsoft.com/?ref=go)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                                                                  |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                                                         |
| Redistribuible<br/>          | API de mitigación de nombres de dominio internacionalizados (IDN) de Microsoft enWindows XP con SP2, Windows Server 2003 con SP1 oWindows Vista<br/> |
| Header<br/>                   | <dl> <dt>Idndl.h</dt> </dl>                                                           |
| Archivo DLL<br/>                      | <dl> <dt>Idndl.dll</dt> </dl>                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con idiomas nacionales](national-language-support.md)
</dt> <dt>

[Funciones de compatibilidad con idiomas nacionales](national-language-support-functions.md)
</dt> <dt>

[Control de nombres de dominio internacionalizados (IDN)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md)
</dt> <dt>

[**DownlevelGetStringScripts**](downlevelgetstringscripts.md)
</dt> <dt>

[**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)
</dt> </dl>

 

 

---
description: Recupera el nombre de la configuración regional del elemento primario de la configuración regional proporcionada.
ms.assetid: a8db8107-822c-4bbc-acb8-40b25d2b41c4
title: Función DownlevelGetParentLocaleName (Nlsdl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: af7580188c7ded31c80476509aef8a10ee83b1cb1f9767ca5819eed053f1ce87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898746"
---
# <a name="downlevelgetparentlocalename-function"></a>Función DownlevelGetParentLocaleName

Recupera el nombre [de la configuración regional](locale-names.md) del elemento primario de la configuración regional proporcionada.

> [!Note]  
> Esta función solo la usan las aplicaciones que se ejecutan en sistemas operativos Windows Vista. Su uso requiere el paquete de descarga. Las aplicaciones que solo se ejecutan Windows Vista y versiones posteriores deben llamar a [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) con *LCType* establecido en [LOCALE \_ SPARENT](locale-sparent.md).

 

## <a name="syntax"></a>Sintaxis


```C++
int DownlevelGetParentLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Configuración regional* \[ En\]
</dt> <dd>

[Identificador de configuración regional](locale-identifiers.md) de la configuración regional. Puede usar la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) para crear un identificador de configuración regional o usar uno de los siguientes valores predefinidos.

-   [LOCALE \_ INVARIANT](locale-invariant.md)
-   [CONFIGURACIÓN REGIONAL \_ PREDETERMINADA DEL \_ SISTEMA](locale-system-default.md)
-   [CONFIGURACIÓN REGIONAL \_ PREDETERMINADA DEL \_ USUARIO](locale-user-default.md)

**Windows Vista y versiones posteriores:** También se admiten los siguientes identificadores de configuración regional personalizados.

-   [CONFIGURACIÓN REGIONAL \_ PREDETERMINADA \_ PERSONALIZADA](locale-custom-constants.md)
-   [CONFIGURACIÓN REGIONAL PREDETERMINADA \_ DE LA INTERFAZ DE USUARIO \_ \_ PERSONALIZADA](locale-custom-constants.md)
-   [CONFIGURACIÓN REGIONAL \_ PERSONALIZADA \_ SIN ESPECIFICAR](locale-custom-constants.md)

</dd> <dt>

*lpName* \[ out\]
</dt> <dd>

Puntero a un búfer en el que la función recupera el nombre de la configuración regional primaria o uno de los siguientes valores predefinidos. Este parámetro se establece en **NULL si** *cchName* está establecido en 0.

-   [NOMBRE DE \_ CONFIGURACIÓN REGIONAL \_ INVARIABLE](locale-name-constants.md)
-   [CONFIGURACIÓN REGIONAL NOMBRE \_ PREDETERMINADO \_ DEL \_ SISTEMA](locale-name-constants.md)
-   [CONFIGURACIÓN REGIONAL NOMBRE \_ DE \_ USUARIO \_ PREDETERMINADO](locale-name-constants.md)

</dd> <dt>

*cchName* \[ En\]
</dt> <dd>

Tamaño del búfer indicado por *lpName*, en puntos de código UTF-16. Un valor de 0 para este parámetro hace que la función ignore el búfer *lpName* y devuelva el tamaño del búfer, en caracteres (caracteres null incluidos), necesario para contener el nombre de la configuración regional primaria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el recuento de puntos de código UTF-16 en el nombre de la configuración regional, incluido el carácter nulo de terminación, si se realiza correctamente.

Esta función devuelve 0 si no se realiza correctamente. Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:

-   ERROR \_ BÚFER \_ INSUFICIENTE. Un tamaño de búfer proporcionado no era lo suficientemente grande o se estableció incorrectamente en **NULL.**
-   ERROR \_ PARÁMETRO \_ NO VÁLIDO. Cualquiera de los valores de parámetro no era válido.

## <a name="remarks"></a>Comentarios

El archivo de encabezado y el archivo DLL necesarios forman parte de la descarga "API de asignación de datos de nivel inferior de Microsoft NLS", disponible en el Centro [de descarga de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | API de asignación de datos de nivel inferior de Microsoft NLS enWindows XP con SP2 y versiones posteriores<br/>  |
| Header<br/>                   | <dl> <dt>Nlsdl.h</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con idiomas nacionales](national-language-support.md)
</dt> <dt>

[Funciones de compatibilidad con idiomas nacionales](national-language-support-functions.md)
</dt> <dt>

[Asignación de datos de configuración regional](mapping-locale-data.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 

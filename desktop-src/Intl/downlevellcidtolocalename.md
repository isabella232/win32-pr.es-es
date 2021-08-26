---
description: Convierte un identificador de configuración regional en un nombre de configuración regional.
ms.assetid: 8e40d097-08a2-43e8-88e8-a4ecaddf449a
title: Función DownlevelLCIDToLocaleName (Nlsdl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLCIDToLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: b96d0c983c46c5d16007aae3a59659099a48855048194153d0c8102d26dc5bd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898725"
---
# <a name="downlevellcidtolocalename-function"></a>Función DownlevelLCIDToLocaleName

Convierte un identificador [de configuración regional](locale-identifiers.md) en un nombre de configuración [regional.](locale-names.md)

> [!Note]  
> Esta función solo la usan las aplicaciones que se ejecutan en sistemas operativos Windows vista previos. Su uso requiere un paquete de descarga. Las aplicaciones que solo se ejecutan Windows Vista y versiones posteriores deben llamar a [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) para recuperar un nombre de configuración regional.

 

## <a name="syntax"></a>Sintaxis


```C++
int DownlevelLCIDToLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName,
  _In_  DWORD  dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Configuración regional* \[ En\]
</dt> <dd>

Identificador de configuración regional que se traducirá. Puede usar la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) para crear un identificador de configuración regional. Esta función no admite configuraciones regionales neutras ni los siguientes valores de identificador de configuración regional específicos.

-   [CONFIGURACIÓN REGIONAL \_ PREDETERMINADA DEL \_ SISTEMA](locale-system-default.md)
-   [CONFIGURACIÓN REGIONAL \_ PREDETERMINADA DEL \_ USUARIO](locale-user-default.md)
-   [CONFIGURACIÓN REGIONAL \_ PREDETERMINADA \_ PERSONALIZADA](locale-custom-constants.md)
-   [CONFIGURACIÓN REGIONAL \_ PREDETERMINADA DE LA INTERFAZ DE USUARIO \_ \_ PERSONALIZADA](locale-custom-constants.md)
-   [CONFIGURACIÓN REGIONAL \_ PERSONALIZADA \_ SIN ESPECIFICAR](locale-custom-constants.md)

</dd> <dt>

*lpName* \[ out\]
</dt> <dd>

Puntero a un búfer en el que esta función recupera el nombre de la configuración regional. La función recupera **NULL si** *cchName* está establecido en 0.

</dd> <dt>

*cchName* \[ En\]
</dt> <dd>

Tamaño, en puntos de código UTF-16, del búfer de nombre de configuración regional. La aplicación establece este parámetro en 0 para devolver el tamaño necesario del búfer de nombre de configuración regional.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Marcas que especifican el tipo de nombre que se recuperará. El valor predeterminado es DOWNLEVEL \_ LOCALE \_ NAME.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el recuento de puntos de código UTF-16 en el nombre de la configuración regional, incluido el carácter nulo de terminación, si se realiza correctamente. Si la función se realiza correctamente y el valor de *cchName* es 0, el valor devuelto es el tamaño necesario, en caracteres (incluidos los caracteres null), para el búfer de nombre de configuración regional.

La función devuelve 0 si no se realiza correctamente. Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:

-   ERROR \_ BÚFER \_ INSUFICIENTE. Un tamaño de búfer proporcionado no era lo suficientemente grande o se estableció incorrectamente en **NULL.**
-   ERROR \_ MARCAS NO \_ VÁLIDAS. El valor de *dwFlags* no es válido.
-   ERROR \_ PARÁMETRO NO \_ VÁLIDO. Cualquiera de los valores de parámetro no era válido.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Esta función no admite [configuraciones regionales personalizadas.](custom-locales.md)

 

El archivo de encabezado y el archivo DLL necesarios forman parte de la descarga "Api de asignación de datos de nivel inferior de Microsoft NLS", disponible en el [Centro de descarga de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                |
| Redistribuible<br/>          | API de asignación de datos de nivel inferior de Microsoft NLS enWindows XP con SP2 y laterorWindows Vista<br/> |
| Header<br/>                   | <dl> <dt>Nlsdl.h</dt> </dl>                  |
| Archivo DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con idiomas nacionales](national-language-support.md)
</dt> <dt>

[Funciones de compatibilidad con idiomas nacionales](national-language-support-functions.md)
</dt> <dt>

[Asignación de datos de configuración regional](mapping-locale-data.md)
</dt> <dt>

[**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename)
</dt> </dl>

 

 

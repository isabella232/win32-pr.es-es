---
description: Convierte un identificador de configuración regional en un nombre de configuración regional.
ms.assetid: 8e40d097-08a2-43e8-88e8-a4ecaddf449a
title: Función DownlevelLCIDToLocaleName (nlsdl. h)
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
ms.openlocfilehash: 2f8e4ce9763348cf765522ebbd624a6e82f1071a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668414"
---
# <a name="downlevellcidtolocalename-function"></a>DownlevelLCIDToLocaleName función)

Convierte un [identificador de configuración](locale-identifiers.md) regional en un [nombre de configuración regional](locale-names.md).

> [!Note]  
> Esta función solo la usan las aplicaciones que se ejecutan en sistemas operativos anteriores a Windows Vista. Su uso requiere un paquete de descarga. Las aplicaciones que solo se ejecutan en Windows Vista y versiones posteriores deben llamar a [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) para recuperar un nombre de configuración regional.

 

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

*Configuración regional* \[ de\]
</dt> <dd>

Identificador de configuración regional que se va a traducir. Puede usar la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) para crear un identificador de configuración regional. Esta función no admite configuraciones regionales neutras ni los siguientes valores de identificador de configuración regional específicos.

-   [configuración \_ predeterminada del sistema local \_](locale-system-default.md)
-   [\_valor predeterminado del usuario de configuración regional \_](locale-user-default.md)
-   [CONFIGURACIÓN \_ predeterminada personalizada \_](locale-custom-constants.md)
-   [CONFIGURACIÓN predeterminada de la \_ \_ interfaz de usuario personalizada \_](locale-custom-constants.md)
-   [configuración regional \_ personalizada no \_ especificada](locale-custom-constants.md)

</dd> <dt>

*lpName* \[ enuncia\]
</dt> <dd>

Puntero a un búfer en el que esta función recupera el nombre de la configuración regional. La función recupera **null** si *cchName* está establecido en 0.

</dd> <dt>

*cchName* \[ de\]
</dt> <dd>

Tamaño, en puntos de código UTF-16, del búfer de nombres de configuración regional. La aplicación establece este parámetro en 0 para devolver el tamaño necesario del búfer del nombre de la configuración regional.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Marcas que especifican el tipo de nombre que se va a recuperar. El valor predeterminado es el nombre de la configuración regional de nivel inferior \_ \_ .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el recuento de puntos de código UTF-16 en el nombre de la configuración regional, incluido el carácter nulo de terminación, si es correcto. Si la función se ejecuta correctamente y el valor de *cchName* es 0, el valor devuelto es el tamaño necesario, en caracteres (incluidos los caracteres null), para el búfer de nombre de la configuración regional.

La función devuelve 0 si no se realiza correctamente. Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:

-   ERROR \_ de \_ búfer insuficiente. Un tamaño de búfer proporcionado no era lo suficientemente grande o se estableció incorrectamente en **null**.
-   ERROR en \_ marcas no válidas \_ . El valor de *dwFlags* no es válido.
-   ERROR \_ de \_ parámetro no válido. Cualquiera de los valores de parámetro no era válido.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Esta función no admite [configuraciones regionales personalizadas](custom-locales.md).

 

El archivo de encabezado y DLL necesarios forman parte de la descarga de la "API de asignación de datos de Microsoft NLS Downlevel", disponible en el [centro de descarga de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                |
| Redistribuible<br/>          | API de asignación de datos de Microsoft NLS Downlevel Windows XP con SP2 y laterorWindows vista<br/> |
| Encabezado<br/>                   | <dl> <dt>Nlsdl. h</dt> </dl>                  |
| Archivo DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con National Language](national-language-support.md)
</dt> <dt>

[Funciones de soporte de National Language](national-language-support-functions.md)
</dt> <dt>

[Asignar datos de configuración regional](mapping-locale-data.md)
</dt> <dt>

[**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename)
</dt> </dl>

 

 

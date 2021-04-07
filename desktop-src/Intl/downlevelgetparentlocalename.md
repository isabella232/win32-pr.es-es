---
description: Recupera el nombre de configuración regional para el elemento primario de la configuración regional proporcionada.
ms.assetid: a8db8107-822c-4bbc-acb8-40b25d2b41c4
title: Función DownlevelGetParentLocaleName (nlsdl. h)
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
ms.openlocfilehash: d3a556d68c33249d2e6b49c48035cc58d8bac8e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002782"
---
# <a name="downlevelgetparentlocalename-function"></a>DownlevelGetParentLocaleName función)

Recupera el [nombre de configuración regional](locale-names.md) para el elemento primario de la configuración regional proporcionada.

> [!Note]  
> Esta función solo la usan las aplicaciones que se ejecutan en sistemas operativos anteriores a Windows Vista. Su uso requiere el paquete de descarga. Las aplicaciones que solo se ejecutan en Windows Vista y versiones posteriores deben llamar a [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) con *LCType* establecido en [ \_ SPARENT de configuración regional](locale-sparent.md).

 

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

*Configuración regional* \[ de\]
</dt> <dd>

[Identificador de configuración regional](locale-identifiers.md) de la configuración regional. Puede usar la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) para crear un identificador de configuración regional o usar uno de los siguientes valores predefinidos.

-   [configuración regional \_ INvariable](locale-invariant.md)
-   [configuración \_ predeterminada del sistema local \_](locale-system-default.md)
-   [\_valor predeterminado del usuario de configuración regional \_](locale-user-default.md)

**Windows Vista y versiones posteriores:** También se admiten los siguientes identificadores de configuración regional personalizados.

-   [CONFIGURACIÓN \_ predeterminada personalizada \_](locale-custom-constants.md)
-   [CONFIGURACIÓN predeterminada de la \_ \_ interfaz de usuario personalizada \_](locale-custom-constants.md)
-   [configuración regional \_ personalizada no \_ especificada](locale-custom-constants.md)

</dd> <dt>

*lpName* \[ enuncia\]
</dt> <dd>

Puntero a un búfer en el que la función recupera el nombre de la configuración regional primaria, o uno de los siguientes valores predefinidos. Este parámetro se establece en **null** si *cchName* está establecido en 0.

-   [nombre de configuración regional \_ \_ invariable](locale-name-constants.md)
-   [nombre de configuración regional \_ \_ predeterminado del sistema \_](locale-name-constants.md)
-   [nombre de configuración regional \_ \_ predeterminado del usuario \_](locale-name-constants.md)

</dd> <dt>

*cchName* \[ de\]
</dt> <dd>

Tamaño del búfer indicado por *lpName*, en puntos de código UTF-16. Un valor de 0 para este parámetro hace que la función omita el búfer *lpName* y devuelva el tamaño del búfer, en caracteres (caracteres null incluidos), necesario para contener el nombre de la configuración regional primaria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el recuento de puntos de código UTF-16 en el nombre de la configuración regional, incluido el carácter nulo de terminación, si es correcto.

Esta función devuelve 0 si no se realiza correctamente. Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:

-   ERROR \_ de \_ búfer insuficiente. Un tamaño de búfer proporcionado no era lo suficientemente grande o se estableció incorrectamente en **null**.
-   ERROR \_ de \_ parámetro no válido. Cualquiera de los valores de parámetro no era válido.

## <a name="remarks"></a>Observaciones

El archivo de encabezado y DLL necesarios forman parte de la descarga de la "API de asignación de datos de Microsoft NLS Downlevel", disponible en el [centro de descarga de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | API de asignación de datos de Microsoft NLS Downlevel Windows XP con SP2 y versiones posteriores<br/>  |
| Encabezado<br/>                   | <dl> <dt>Nlsdl. h</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con National Language](national-language-support.md)
</dt> <dt>

[Funciones de soporte de National Language](national-language-support-functions.md)
</dt> <dt>

[Asignar datos de configuración regional](mapping-locale-data.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 

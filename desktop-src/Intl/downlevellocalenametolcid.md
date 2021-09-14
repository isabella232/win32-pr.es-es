---
description: Convierte un nombre de configuración regional en un identificador de configuración regional que se puede usar para obtener información del sistema operativo.
ms.assetid: dc776c41-0376-4222-bebf-86be7e4be122
title: Función DownlevelLocaleNameToLCID (Nlsdl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLocaleNameToLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: c41b82c59b63a5b324e15f89c1f77118d454e428
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274687"
---
# <a name="downlevellocalenametolcid-function"></a>Función DownlevelLocaleNameToLCID

Convierte un nombre [de configuración regional](locale-names.md) en un identificador de [configuración](locale-identifiers.md) regional que se puede usar para obtener información del sistema operativo.

> [!Note]  
> Esta función solo la usan las aplicaciones que se ejecutan en sistemas operativos Windows vista previos. Su uso requiere un paquete de descarga. Las aplicaciones que solo se ejecutan Windows Vista y versiones posteriores deben llamar a [**LocaleNameToLCID para**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) recuperar un identificador de configuración regional.

 

## <a name="syntax"></a>Sintaxis


```C++
LCID DownlevelLocaleNameToLCID(
  _In_ LPWSTR lpName,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que representa un [nombre de configuración regional](locale-names.md).

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Marcas que especifican el tipo de nombre. El valor predeterminado es DOWNLEVEL \_ LOCALE \_ NAME.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de configuración regional que corresponde al nombre de la configuración regional si se realiza correctamente.

La función devuelve 0 si no se realiza correctamente. Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:

-   ERROR \_ MARCAS NO \_ VÁLIDAS. Los valores proporcionados para las marcas no eran válidos.
-   ERROR \_ PARÁMETRO NO \_ VÁLIDO. Cualquiera de los valores de parámetro no era válido.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Esta función no admite configuraciones regionales neutras. La función [**LocaleNameToLCID equivalente**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) admite configuraciones [regionales](custom-locales.md)personalizadas, pero solo para Windows Vista y versiones posteriores.

 

El archivo de encabezado y el archivo DLL necesarios forman parte de la descarga "Api de asignación de datos de nivel inferior de Microsoft NLS", disponible en el [Centro de descarga de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                |
| Redistribuible<br/>          | API de asignación de datos de nivel inferior de Microsoft NLS enWindows XP con SP2 y laterorWindows Vista<br/> |
| Encabezado<br/>                   | <dl> <dt>Nlsdl.h</dt> </dl>                  |
| Archivo DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl>               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Compatibilidad con idiomas nacionales](national-language-support.md)
</dt> <dt>

[Funciones de compatibilidad con idiomas nacionales](national-language-support-functions.md)
</dt> <dt>

[Asignación de datos de configuración regional](mapping-locale-data.md)
</dt> <dt>

[**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
</dt> </dl>

 

 

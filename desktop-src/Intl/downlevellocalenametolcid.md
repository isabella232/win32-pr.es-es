---
description: Convierte un nombre de configuración regional en un identificador de configuración regional que se puede utilizar para obtener información del sistema operativo.
ms.assetid: dc776c41-0376-4222-bebf-86be7e4be122
title: Función DownlevelLocaleNameToLCID (nlsdl. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653005"
---
# <a name="downlevellocalenametolcid-function"></a>DownlevelLocaleNameToLCID función)

Convierte un [nombre de configuración regional](locale-names.md) en un [identificador de configuración regional](locale-identifiers.md) que se puede utilizar para obtener información del sistema operativo.

> [!Note]  
> Esta función solo la usan las aplicaciones que se ejecutan en sistemas operativos anteriores a Windows Vista. Su uso requiere un paquete de descarga. Las aplicaciones que solo se ejecutan en Windows Vista y versiones posteriores deben llamar a [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) para recuperar un identificador de configuración regional.

 

## <a name="syntax"></a>Sintaxis


```C++
LCID DownlevelLocaleNameToLCID(
  _In_ LPWSTR lpName,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que representa un [nombre de configuración regional](locale-names.md).

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Marcas que especifican el tipo de nombre. El valor predeterminado es el nombre de la configuración regional de nivel inferior \_ \_ .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de configuración regional que corresponde al nombre de la configuración regional si se realiza correctamente.

La función devuelve 0 si no se realiza correctamente. Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:

-   ERROR en \_ marcas no válidas \_ . Los valores proporcionados para marcas no eran válidos.
-   ERROR \_ de \_ parámetro no válido. Cualquiera de los valores de parámetro no era válido.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Esta función no admite configuraciones regionales neutras. La función [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) equivalente admite [configuraciones regionales personalizadas](custom-locales.md), pero solo para Windows Vista y versiones posteriores.

 

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

[**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
</dt> </dl>

 

 

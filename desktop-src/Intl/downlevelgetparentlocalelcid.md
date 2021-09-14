---
description: Recupera el identificador de configuración regional para el elemento primario de la configuración regional proporcionada.
ms.assetid: 4cfa1787-6b9e-4dd4-8466-7b737e00a4b1
title: Función DownlevelGetParentLocaleLCID (Nlsdl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: b34f30425147057efe8039cc36514d699199c9a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274703"
---
# <a name="downlevelgetparentlocalelcid-function"></a>Función DownlevelGetParentLocaleLCID

Recupera el identificador [de configuración regional](locale-identifiers.md) para el elemento primario de la configuración regional proporcionada.

> [!Note]  
> Esta función solo la usan las aplicaciones que se ejecutan en sistemas operativos Windows Vista. Su uso requiere el paquete de descarga. Las aplicaciones que solo se ejecutan Windows Vista y versiones posteriores deben llamar a [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) con *LCType* establecido en [LOCALE \_ SPARENT](locale-sparent.md).

 

## <a name="syntax"></a>Sintaxis


```C++
LCID DownlevelGetParentLocaleLCID(
  _In_ LCID Locale
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Configuración regional* \[ En\]
</dt> <dd>

Identificador de configuración regional de la configuración regional para la que se va a recuperar el identificador de configuración regional primaria. Puede usar la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) para crear un identificador de configuración regional o usar uno de los siguientes valores predefinidos.

-   [LOCALE \_ INVARIANT](locale-invariant.md)
-   [CONFIGURACIÓN REGIONAL \_ PREDETERMINADA DEL \_ SISTEMA](locale-system-default.md)
-   [CONFIGURACIÓN REGIONAL \_ PREDETERMINADA DEL \_ USUARIO](locale-user-default.md)

**Windows Vista y versiones posteriores:** También se admiten los siguientes identificadores de configuración regional personalizados.

-   [CONFIGURACIÓN REGIONAL \_ PREDETERMINADA \_ PERSONALIZADA](locale-custom-constants.md)
-   [CONFIGURACIÓN REGIONAL PREDETERMINADA \_ DE LA INTERFAZ DE USUARIO \_ \_ PERSONALIZADA](locale-custom-constants.md)
-   [CONFIGURACIÓN REGIONAL \_ PERSONALIZADA \_ SIN ESPECIFICAR](locale-custom-constants.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de configuración regional primario si se realiza correctamente o 0 en caso contrario. Para obtener información de error extendida, la aplicación puede llamar a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que puede devolver uno de los siguientes códigos de error:

-   ERROR \_ PARÁMETRO \_ NO VÁLIDO. Cualquiera de los valores de parámetro no era válido.

## <a name="remarks"></a>Observaciones

El archivo de encabezado y el archivo DLL necesarios forman parte de la descarga "API de asignación de datos de nivel inferior de Microsoft NLS", disponible en el Centro [de descarga de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | API de asignación de datos de nivel inferior de Microsoft NLS enWindows XPor Windows Vista<br/>     |
| Encabezado<br/>                   | <dl> <dt>Nlsdl.h</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Compatibilidad con idiomas nacionales](national-language-support.md)
</dt> <dt>

[Funciones de compatibilidad con idiomas nacionales](national-language-support-functions.md)
</dt> <dt>

[Asignación de datos de configuración regional](mapping-locale-data.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 

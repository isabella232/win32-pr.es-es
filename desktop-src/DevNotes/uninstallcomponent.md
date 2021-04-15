---
description: Quita un paquete de excepciones.
ms.assetid: d590d0f8-c9b2-4973-999b-99bbf94d4928
title: UninstallComponent función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UninstallComponent
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: a541f51b030c9be7a26d573794e4df3a7cfc6f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649500"
---
# <a name="uninstallcomponent-function"></a>UninstallComponent función)

Quita un paquete de excepciones.

## <a name="syntax"></a>Sintaxis


```C++
void UninstallComponent(
  _In_opt_ const GUID  *CompGuid,
  _In_           DWORD Flags,
  _In_opt_       INT   VerMajor,
  _In_opt_       INT   VerMinor,
  _In_opt_       INT   VerBuild,
  _In_opt_       INT   VerQFE
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CompGuid* \[ en, opcional\]
</dt> <dd>

GUID del componente de excepción que se va a desinstalar.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Marcas usadas para controlar los comportamientos de instalación. Este parámetro puede ser una combinación de los valores siguientes.



| Value                                                                                                                                                                                                         | Significado                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <dt>**marcas de COMP \_ \_ NOUI**</dt> </dl>                                          | Suprime toda la interfaz de usuario.<br/>                                                                |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <dt>**marcas de COMP \_ \_ actualizar \_ DLLCACHE**</dt> </dl>        | Fuerza la actualización del directorio DLLCACHE cuando se actualiza un archivo del sistema.<br/>        |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <dt>**marcas de COMP \_ \_ usar \_ \_ caché SVCPACK**</dt> </dl> | Usa los archivos almacenados en memoria caché por una instalación de Windows Service Pack para sustituir los archivos de los que se ha realizado una copia de seguridad.<br/> |



 

</dd> <dt>

*VerMajor* \[ en, opcional\]
</dt> <dd>

Versión principal del componente de excepción que se va a desinstalar.

</dd> <dt>

*Parásitos* \[ en, opcional\]
</dt> <dd>

Versión secundaria del componente de excepción que se va a desinstalar.

</dd> <dt>

*VerBuild* \[ en, opcional\]
</dt> <dd>

Versión de compilación del componente de excepción que se va a desinstalar.

</dd> <dt>

*VerQFE* \[ en, opcional\]
</dt> <dd>

Revisión de la revisión del componente de excepción que se va a desinstalar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Los paquetes de excepción son archivos del sistema de Windows que se publican fuera de una versión completa de Windows y que actualizan los archivos del sistema operativo. Los paquetes de excepción solo los pueden crear equipos del sistema operativo a los que se les ha concedido autorización para actualizar archivos del sistema de Windows.

Para instalar y desinstalar archivos que no están protegidos por protección de archivos de Windows, use las funciones documentadas en [funciones generales de instalación](https://msdn.microsoft.com/library/ms794585.aspx). Para instalar controladores de dispositivos, los expendedores deben usar funciones documentadas en funciones de [instalación de dispositivos](https://msdn.microsoft.com/library/ms792954.aspx) y [funciones de Configuration Manager PNP](https://msdn.microsoft.com/library/ms790838.aspx).

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msoobci.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>


</dt> <dt>

[**InstallComponentW**](installcomponentw.md)
</dt> </dl>

 

 

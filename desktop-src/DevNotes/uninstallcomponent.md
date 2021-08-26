---
description: Quita un paquete de excepciones.
ms.assetid: d590d0f8-c9b2-4973-999b-99bbf94d4928
title: Función UninstallComponent
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
ms.openlocfilehash: d6b4ce8e447bc884d1b3ee64505d230b2e069ce6cda1630b027b8a48da68beda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001115"
---
# <a name="uninstallcomponent-function"></a>Función UninstallComponent

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

*CompGuid* \[ in, opcional\]
</dt> <dd>

GUID del componente de excepción que se va a desinstalar.

</dd> <dt>

*Marcas* \[ En\]
</dt> <dd>

Marcas usadas para controlar los comportamientos de instalación. Este parámetro puede ser una combinación de los valores siguientes.



| Value                                                                                                                                                                                                         | Significado                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <dt>**COMP \_ FLAGS \_ NOUI**</dt> </dl>                                          | Suprime toda la interfaz de usuario.<br/>                                                                |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <dt>**DLLCACHE \_ DE ACTUALIZACIÓN DE MARCAS DE \_ \_ COMP**</dt> </dl>        | Fuerza la actualización del directorio DLLCACHE cuando se actualiza un archivo del sistema.<br/>        |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <dt>**LAS \_ MARCAS DE COMP USAN \_ \_ SVCPACK \_ CACHE**</dt> </dl> | Usa los archivos almacenados en caché Windows service pack para reemplazar los archivos de los que se ha creado una copia de seguridad.<br/> |



 

</dd> <dt>

*VerMajor* \[ in, opcional\]
</dt> <dd>

Versión principal del componente de excepción que se va a desinstalar.

</dd> <dt>

*VerMinor* \[ in, opcional\]
</dt> <dd>

Versión secundaria del componente de excepción que se va a desinstalar.

</dd> <dt>

*VerBuild* \[ in, opcional\]
</dt> <dd>

Versión de compilación del componente de excepción que se va a desinstalar.

</dd> <dt>

*VerQFE* \[ in, opcional\]
</dt> <dd>

Revisión del componente de excepción que se va a desinstalar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Los paquetes de excepción Windows archivos del sistema que se liberan fuera de un paquete completo Windows versión y que actualizan los archivos del sistema operativo. Los paquetes de excepciones solo son creados por equipos de sistema operativo a los que se les ha concedido autorización para actualizar Windows archivos del sistema.

Para instalar y desinstalar archivos que no están protegidos por Windows File Protection, use las funciones documentadas en [Funciones de instalación generales](https://msdn.microsoft.com/library/ms794585.aspx). Para instalar controladores de dispositivos, los vendedores deben usar funciones documentadas en [Funciones de](https://msdn.microsoft.com/library/ms792954.aspx) instalación de dispositivos [y PnP Administrador de configuración Functions](https://msdn.microsoft.com/library/ms790838.aspx).

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msoobci.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>


</dt> <dt>

[**InstallComponentW**](installcomponentw.md)
</dt> </dl>

 

 

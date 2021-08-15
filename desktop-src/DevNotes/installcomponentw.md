---
description: Instala un paquete de excepción.
ms.assetid: c4c3c01c-9aaf-42cd-a690-13e2113b15b3
title: Función InstallComponentW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallComponentW
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: 9deaa460ec58ad0aa07af38aa03f53971068b4a6a1d43131e5473a7e4def908c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955924"
---
# <a name="installcomponentw-function"></a>Función InstallComponentW

Instala un paquete de excepción.

## <a name="syntax"></a>Sintaxis


```C++
void InstallComponentW(
  _In_           LPCWSTR InfPath,
  _In_opt_ const GUID    *CompGuid,
  _In_           DWORD   Flags,
  _In_opt_       INT     VerMajor,
  _In_opt_       INT     VerMinor,
  _In_opt_       INT     VerBuild,
  _In_opt_       INT     VerQFE,
  _In_opt_       LPCWSTR Name
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*InfPath* \[ En\]
</dt> <dd>

Ruta de acceso a la excepción INF que se debe procesar.

</dd> <dt>

*CompGuid* \[ in, opcional\]
</dt> <dd>

GUID del componente de excepción que se está instalando.

</dd> <dt>

*Marcas* \[ En\]
</dt> <dd>

Marcas usadas para controlar los comportamientos de instalación. Este parámetro puede ser una combinación de los valores siguientes.



| Valor                                                                                                                                                                                                                                                               | Significado                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_FORCE"></span><span id="comp_flags_force"></span><dl> <dt>**COMP \_ FLAGS \_ FORCE**</dt> <dt>0x00000020</dt> </dl>                             | Omite la comprobación de versión en los reemplazos de archivos.<br/>                                                                                                    |
| <span id="COMP_FLAGS_NEEDS_UNINSTALL"></span><span id="comp_flags_needs_uninstall"></span><dl> <dt>**COMP \_ FLAGS \_ NEEDS \_ UNINSTALL**</dt><dt></dt> </dl>        | Haga una copia de seguridad de los archivos que se actualizan para que los utilice una desinstalación del componente.<br/>                                                                      |
| <span id="COMP_FLAGS_NO_OVERWRITE"></span><span id="comp_flags_no_overwrite"></span><dl> <dt>**COMP \_ MARCAS \_ SIN \_ SOBRESCRITURA**</dt><dt></dt> </dl>                 | Omite la copia de seguridad de archivos si la versión del componente de excepción es la misma que la de un componente instalado. Esta marca se usa en un escenario de reinstalación.<br/> |
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <dt>**COMP \_ Marcas \_ noui**</dt> <dt>0x00000002</dt> </dl>                                | Suprime toda la interfaz de usuario.<br/>                                                                                                                               |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <dt>**COMP \_ FLAGS \_ UPDATE \_ DLLCACHE**</dt><dt></dt> </dl>        | Fuerza la actualización del directorio DLLCACHE cuando se actualiza un archivo del sistema.<br/>                                                                       |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <dt>**COMP \_ LAS MARCAS \_ USAN \_ SVCPACK \_ CACHE**</dt><dt></dt> </dl> | Usa los archivos almacenados en caché Windows instalación de Service Pack para reemplazar los archivos de los que se ha creado una copia de seguridad.<br/>                                                                |



 

</dd> <dt>

*VerMajor* \[ in, opcional\]
</dt> <dd>

Versión principal del componente Exception.

</dd> <dt>

*VerMinor* \[ in, opcional\]
</dt> <dd>

Versión secundaria del componente Exception.

</dd> <dt>

*VerBuild* \[ in, opcional\]
</dt> <dd>

Versión de compilación del componente Exception.

</dd> <dt>

*VerQFE* \[ in, opcional\]
</dt> <dd>

Revisión de revisión del componente Exception.

</dd> <dt>

*Nombre* \[ in, opcional\]
</dt> <dd>

Cadena descriptiva del componente que muestra el cuadro de diálogo protección de archivos de Windows si el sistema operativo detecta que un archivo de protección de Windows File Protection está dañado, alterado o dañado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve un **valor HRESULT** (S \_ OK o un código de error). Se puede comprobar un código de error con un valor de 0x20000100 para determinar si el error se debe a que se requiere un reinicio.

## <a name="remarks"></a>Comentarios

Los paquetes de excepción Windows archivos del sistema que se liberan fuera de un paquete completo Windows versión y que actualizan los archivos del sistema operativo. Los paquetes de excepciones solo son creados por equipos de sistema operativo a los que se les ha concedido autorización para actualizar Windows archivos del sistema.

Para instalar y desinstalar archivos que no están protegidos por Windows File Protection, use las funciones documentadas en [Funciones de instalación general](https://msdn.microsoft.com/library/ms794585.aspx). Para instalar controladores de dispositivo, los vendedores deben usar funciones documentadas en [Funciones](https://msdn.microsoft.com/library/ms792954.aspx) de instalación de dispositivos [y PnP Administrador de configuración Functions](https://msdn.microsoft.com/library/ms790838.aspx).

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msoobci.dll</dt> </dl> |



 

 

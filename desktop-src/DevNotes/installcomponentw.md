---
description: Instala un paquete de excepciones.
ms.assetid: c4c3c01c-9aaf-42cd-a690-13e2113b15b3
title: InstallComponentW función)
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
ms.openlocfilehash: 4d262322be6084429f03d5725f61c0e0f7140871
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660987"
---
# <a name="installcomponentw-function"></a>InstallComponentW función)

Instala un paquete de excepciones.

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

*InfPath* \[ de\]
</dt> <dd>

Ruta de acceso al INF de excepción que se va a procesar.

</dd> <dt>

*CompGuid* \[ en, opcional\]
</dt> <dd>

GUID del componente de excepción que se va a instalar.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Marcas usadas para controlar los comportamientos de instalación. Este parámetro puede ser una combinación de los valores siguientes.



| Value                                                                                                                                                                                                                                                               | Significado                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_FORCE"></span><span id="comp_flags_force"></span><dl> <dt>**COMP \_ . MARCAS \_ fuerzan**</dt> <dt>0x00000020</dt> </dl>                             | Omite la comprobación de versión en los reemplazos de archivos.<br/>                                                                                                    |
| <span id="COMP_FLAGS_NEEDS_UNINSTALL"></span><span id="comp_flags_needs_uninstall"></span><dl> <dt>**COMP \_ . las marcas \_ requieren \_ desinstalación**</dt><dt></dt> </dl>        | Realice una copia de seguridad de los archivos que se han actualizado para que los utilice una desinstalación del componente.<br/>                                                                      |
| <span id="COMP_FLAGS_NO_OVERWRITE"></span><span id="comp_flags_no_overwrite"></span><dl> <dt>**COMP \_ . MARCAS \_ sin \_ sobrescritura**</dt><dt></dt> </dl>                 | Omite la copia de seguridad de archivos si la versión del componente de excepción es igual que un componente instalado. Esta marca se usa en un escenario de reinstalación.<br/> |
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <dt>**COMP \_ . FLAGs \_ NOUI**</dt> <dt>0x00000002</dt> </dl>                                | Suprime toda la interfaz de usuario.<br/>                                                                                                                               |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <dt>**COMP \_ . MARCAS de \_ actualización de \_ DLLCACHE**</dt><dt></dt> </dl>        | Fuerza la actualización del directorio DLLCACHE cuando se actualiza un archivo del sistema.<br/>                                                                       |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <dt>**COMP \_ . MARCAS \_ usar \_ \_ caché SVCPACK**</dt><dt></dt> </dl> | Usa los archivos almacenados en memoria caché por una instalación de Windows Service Pack para sustituir los archivos de los que se ha realizado una copia de seguridad.<br/>                                                                |



 

</dd> <dt>

*VerMajor* \[ en, opcional\]
</dt> <dd>

Versión principal del componente de excepción.

</dd> <dt>

*Parásitos* \[ en, opcional\]
</dt> <dd>

Versión secundaria del componente de excepción.

</dd> <dt>

*VerBuild* \[ en, opcional\]
</dt> <dd>

Versión de compilación del componente de excepción.

</dd> <dt>

*VerQFE* \[ en, opcional\]
</dt> <dd>

Revisión de la revisión del componente de excepción.

</dd> <dt>

*Nombre* \[ de en, opcional\]
</dt> <dd>

Cadena descriptiva del componente que muestra el cuadro de diálogo protección de archivos de Windows si el sistema operativo detecta que un archivo de protección contra archivos de Windows está dañado, alterado o dañado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve un valor **HRESULT** (es \_ correcto o un código de error). Un código de error se puede comprobar con un valor de 0x20000100 para determinar si el error se debe a que se requiere un reinicio.

## <a name="remarks"></a>Observaciones

Los paquetes de excepción son archivos del sistema de Windows que se publican fuera de una versión completa de Windows y que actualizan los archivos del sistema operativo. Los paquetes de excepción solo los pueden crear equipos del sistema operativo a los que se les ha concedido autorización para actualizar archivos del sistema de Windows.

Para instalar y desinstalar archivos que no están protegidos por protección de archivos de Windows, use las funciones documentadas en [funciones generales de instalación](https://msdn.microsoft.com/library/ms794585.aspx). Para instalar controladores de dispositivos, los expendedores deben usar funciones documentadas en funciones de [instalación de dispositivos](https://msdn.microsoft.com/library/ms792954.aspx) y [funciones de Configuration Manager PNP](https://msdn.microsoft.com/library/ms790838.aspx).

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msoobci.dll</dt> </dl> |



 

 

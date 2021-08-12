---
description: Abre la base de datos shim.
ms.assetid: ece1bd39-20a1-42e6-8e2b-1d38f7223d42
title: Función SdbInitDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbInitDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0504b12254658250820cb3ecac3e9e47ee2a6ca242b15600fa69241b597bb0dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666386"
---
# <a name="sdbinitdatabase-function"></a>Función SdbInitDatabase

Abre la base de datos shim.

## <a name="syntax"></a>Sintaxis


```C++
HSDB WINAPI SdbInitDatabase(
  _In_ DWORD   dwFlags,
  _In_ LPCTSTR pszDatabasePath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Este parámetro especifica el formato de la ruta de acceso en el *parámetro pszDatabasePath.* Puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                                                                                      | Significado                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="HID_DOS_PATHS"></span><span id="hid_dos_paths"></span><dl> <dt>**HID \_ Rutas \_ de acceso dos**</dt> <dt>0x00000001</dt> </dl>                             | Ruta de acceso de estilo MS-DOS.<br/>                                                                       |
| <span id="HID_DATABASE_FULLPATH"></span><span id="hid_database_fullpath"></span><dl> <dt>**HID \_ Database \_ FULLPATH**</dt> <dt>0x00000002</dt> </dl>     | Ruta de acceso completa.<br/>                                                                                |
| <span id="HID_NO_DATABASE"></span><span id="hid_no_database"></span><dl> <dt>**HID \_ NO \_ SE HA**</dt> <dt>0X00000004</dt> </dl>                       | El *parámetro pszDatabasePath* se omite y no se abre ninguna base de datos.<br/>                       |
| <span id="HID_DATABASE_TYPE_MASK"></span><span id="hid_database_type_mask"></span><dl> <dt>**HID \_ DATABASE \_ TYPE \_ MASK**</dt> <dt>0xF00F0000</dt> </dl> | Este parámetro especifica una base de datos predefinida. Se *omite el parámetro pszDatabasePath.*<br/> |



 

Si *dwFlags contiene* **HID DATA TYPE \_ \_ \_ MASK,** este parámetro también puede incluir uno de los siguientes valores.



| Value                                                                                                                                                                                                                                                               | Significado                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <dt>**SDB \_ COMPATIBILIDAD \_ PRINCIPAL DE BASE DE \_**</dt> <dt>DATOS 0X80030000</dt> </dl>          | Base de datos de correcciones de compatibilidad (shim) de aplicación.<br/>         |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <dt>**SDB \_ BASE \_ DE DATOS PRINCIPAL \_ MSI**</dt> <dt>0x80020000</dt> </dl>             | Base de datos MSI.<br/>                      |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <dt>**SDB \_ CONTROLADORES \_ PRINCIPALES DE BASE \_ DE**</dt> <dt>DATOS 0x80040000</dt> </dl> | Base de datos de controladores que se va a bloquear.<br/> |



 

</dd> <dt>

*pszDatabasePath* \[ En\]
</dt> <dd>

Ruta de acceso a la base de datos. Este parámetro puede ser **NULL** si el *parámetro dwFlags* especifica una base de datos predefinida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve un identificador a la base de datos abierta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbGetAppPatchDir**](sdbgetapppatchdir.md)
</dt> <dt>

[**SdbGetMatchingExe**](sdbgetmatchingexe.md)
</dt> <dt>

[**SdbReleaseMatchingExe**](sdbreleasematchingexe.md)
</dt> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> </dl>

 

 





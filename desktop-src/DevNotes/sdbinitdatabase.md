---
description: Abre la base de datos de correcciones de compatibilidad.
ms.assetid: ece1bd39-20a1-42e6-8e2b-1d38f7223d42
title: SdbInitDatabase función)
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
ms.openlocfilehash: 7a3c63fa712aec988dbf13c4fb7f9fddbf159fdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495923"
---
# <a name="sdbinitdatabase-function"></a>SdbInitDatabase función)

Abre la base de datos de correcciones de compatibilidad.

## <a name="syntax"></a>Sintaxis


```C++
HSDB WINAPI SdbInitDatabase(
  _In_ DWORD   dwFlags,
  _In_ LPCTSTR pszDatabasePath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Este parámetro especifica el formato de la ruta de acceso en el parámetro *pszDatabasePath* . Puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                                                                                      | Significado                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="HID_DOS_PATHS"></span><span id="hid_dos_paths"></span><dl> <dt>**HID \_ \_Rutas**</dt> de acceso de dos <dt>0x00000001</dt> </dl>                             | Una ruta de acceso de estilo MS-DOS.<br/>                                                                       |
| <span id="HID_DATABASE_FULLPATH"></span><span id="hid_database_fullpath"></span><dl> <dt>**HID \_ BASE de datos \_ FULLPATH**</dt> <dt>0x00000002</dt> </dl>     | Ruta de acceso completa.<br/>                                                                                |
| <span id="HID_NO_DATABASE"></span><span id="hid_no_database"></span><dl> <dt>**HID \_ NO \_ Database**</dt> <dt>0x00000004</dt> </dl>                       | Se omite el parámetro *pszDatabasePath* y no se abre ninguna base de datos.<br/>                       |
| <span id="HID_DATABASE_TYPE_MASK"></span><span id="hid_database_type_mask"></span><dl> <dt>**HID \_ \_ \_ Máscara de tipo de base de datos**</dt> <dt>0xF00F0000</dt> </dl> | Este parámetro especifica una base de datos predefinida. Se omite el parámetro *pszDatabasePath* .<br/> |



 

Si *dwFlags* contiene **la \_ \_ \_ máscara de tipo de datos HID**, este parámetro también puede incluir uno de los valores siguientes.



| Value                                                                                                                                                                                                                                                               | Significado                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <dt>**SDB \_ \_Corrección de \_ compatibilidad principal de base de datos**</dt> <dt>0x80030000</dt> </dl>          | Base de datos de corrección de compatibilidad de aplicaciones.<br/>         |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <dt>**SDB \_ \_ \_ MSI principal**</dt> de la base de datos <dt>0x80020000</dt> </dl>             | Base de datos MSI.<br/>                      |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <dt>**SDB \_ \_ \_ Controladores principales de base de datos**</dt> <dt>0x80040000</dt> </dl> | Base de datos de controladores que se van a bloquear.<br/> |



 

</dd> <dt>

*pszDatabasePath* \[ de\]
</dt> <dd>

Ruta de acceso a la base de datos. Este parámetro puede ser **null** si el parámetro *dwFlags* especifica una base de datos predefinida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve un identificador a la base de datos abierta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                   |
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

 

 





---
description: Recupera el estado de la memoria caché de Archivos sin conexión.
ms.assetid: a8cc0dbb-0005-4e74-892e-898e2ebe0465
title: CSCQueryDatabaseStatus función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCQueryDatabaseStatus
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: badd869306290609ccadeba80e6ea67ca3479be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650064"
---
# <a name="cscquerydatabasestatus-function"></a>CSCQueryDatabaseStatus función)

\[Esta función no se admite y no debe usarse.\]

Recupera el estado de la memoria caché de Archivos sin conexión.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CSCQueryDatabaseStatus(
   ULONG *pulStatus,
   ULONG *pulErrors
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pulStatus* 
</dt> <dd>

Estado. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                                                                                               | Significado                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="FLAG_DATABASESTATUS_ENCRYPTED"></span><span id="flag_databasestatus_encrypted"></span><dl> <dt>**Marca \_ de DATABASESTATUS \_ cifrado**</dt> <dt>0x00000002</dt> </dl>                                      | La memoria caché está marcada para el cifrado y se cifran todos los archivos de la memoria caché.<br/>                |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_ENCRYPTED"></span><span id="flag_databasestatus_partially_encrypted"></span><dl> <dt>**Marca \_ de DATABASESTATUS el 0x00000004 \_ parcialmente \_ cifrado**</dt> <dt></dt> </dl>       | La memoria caché está marcada para el cifrado, pero algunos archivos de la memoria caché no están cifrados.<br/>          |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_UNENCRYPTED"></span><span id="flag_databasestatus_partially_unencrypted"></span><dl> <dt>**Marca \_ de DATABASESTATUS \_ parcialmente \_ descifrado**</dt> <dt>0x00000004</dt> </dl> | La memoria caché no está marcada para el cifrado, pero no se han descifrado todos los archivos de la memoria caché.<br/> |
| <span id="FLAG_DATABASESTATUS_UNENCRYPTED"></span><span id="flag_databasestatus_unencrypted"></span><dl> <dt>**Marca \_ de DATABASESTATUS \_ sin cifrar**</dt> <dt>0x00000000</dt> </dl>                                | La memoria caché no está marcada para el cifrado y se han descifrado todos los archivos de la memoria caché.<br/>      |



 

</dd> <dt>

*pulErrors* 
</dt> <dd>

Este parámetro es un valor distinto de cero si hay un error interno de la base de datos o 0 en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **true** si se realiza correctamente; de lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|---------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSCIsCSCEnabled**](csciscscenabled.md)
</dt> </dl>

 

 

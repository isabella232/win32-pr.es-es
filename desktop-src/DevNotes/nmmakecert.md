---
description: Crea un certificado de usuario para su uso con conferencias de NetMeeting.
ms.assetid: 22acdcbe-c9c9-4f1b-a62d-44a35e101eec
title: NmMakeCert función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NmMakeCert
api_type:
- DllExport
api_location:
- Nmmkcert.dll
ms.openlocfilehash: f90af11ada2bca330bbabeb83f4a8aa94e611630
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649933"
---
# <a name="nmmakecert-function"></a>NmMakeCert función)

Crea un certificado de usuario para su uso con conferencias de NetMeeting.

## <a name="syntax"></a>Sintaxis


```C++
void NmMakeCert(
   LPCSTR szFirstName,
   LPCSTR szLastName,
   LPCSTR szEmailName,
   LPCSTR szCity,
   LPCSTR szCountry,
   DWORD  dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*szFirstName* 
</dt> <dd>

Nombre del usuario.

</dd> <dt>

*szLastName* 
</dt> <dd>

Apellidos del usuario.

</dd> <dt>

*szEmailName* 
</dt> <dd>

El nombre de correo electrónico del usuario.

</dd> <dt>

*szCity* 
</dt> <dd>

La ciudad del usuario.

</dd> <dt>

*szCountry* 
</dt> <dd>

País o región del usuario.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Valor que indica cómo se debe crear el certificado. Los valores pueden ser cualquiera de los siguientes.



| Value                                                                                                                                                                                                                                                            | Significado                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="NMMKCERT_F_CLEANUP_ONLY"></span><span id="nmmkcert_f_cleanup_only"></span><dl> <dt>**NMMKCERT \_ \_ \_ Solo limpieza de F**</dt> <dt></dt> </dl>    | Elimine el certificado antiguo sin crear uno nuevo. <br/>            |
| <span id="NMMKCERT_F_DELETEOLDCERT"></span><span id="nmmkcert_f_deleteoldcert"></span><dl> <dt>**NMMKCERT \_ F \_ DELETEOLDCERT**</dt> <dt>0x00000001</dt> </dl>  | Elimine el certificado antiguo creado anteriormente con esta función. <br/> |
| <span id="NMMKCERT_F_LOCAL_MACHINE"></span><span id="nmmkcert_f_local_machine"></span><dl> <dt>**NMMKCERT \_ \_ \_ Máquina local de F**</dt> <dt>0x00000002</dt> </dl> | Cree el certificado en el almacén de certificados de la máquina local. <br/>    |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 1 si la función se ejecuta correctamente y – 1 si se produce un error en la función.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Nmmkcert.dll</dt> </dl> |



 

 

---
description: Agrega una cadena y datos adicionales a una tabla.
ms.assetid: e6f29cb0-4468-435d-9ae3-217d4f69e87e
title: pSetupStringTableAddStringEx función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableAddStringEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 22de3bcc2ad21b82e1fd8306a0c668f83c723b9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670672"
---
# <a name="psetupstringtableaddstringex-function"></a>pSetupStringTableAddStringEx función)

\[Esta función no está disponible en Windows Vista ni Windows Server 2008.\]

Agrega una cadena y datos adicionales a una tabla.

## <a name="syntax"></a>Sintaxis


```C++
LONG pSetupStringTableAddStringEx(
  _In_     PVOID StringTable,
  _In_     PTSTR String,
  _In_     DWORD Flags,
  _In_opt_ PVOID ExtraData,
  _In_opt_ UINT  ExtraDataSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StringTable* \[ de\]
</dt> <dd>

Puntero a la tabla de cadenas.

</dd> <dt>

*Cadena* \[ de\]
</dt> <dd>

Puntero a la cadena que se va a agregar a la tabla.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

El valor de este parámetro puede ser `STRTAB_CASE_SENSITIVE | STRTAB_NEW_EXTRADATA` .



| Value                                                                                                                                                                                                                                             | Significado                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="STRTAB_CASE_SENSITIVE"></span><span id="strtab_case_sensitive"></span><dl> <dt>**STRTAB \_ 0x001 que \_ distingue mayúsculas de minúsculas**</dt> <dt></dt> </dl> | String distingue mayúsculas de minúsculas.<br/> |
| <span id="STRTAB_NEW_EXTRADATA"></span><span id="strtab_new_extradata"></span><dl> <dt>**STRTAB \_ NEW \_ ExtraData**</dt> <dt>0x004</dt> </dl>    | Hay datos adicionales.<br/>      |



 

</dd> <dt>

*ExtraData* \[ en, opcional\]
</dt> <dd>

Un puntero opcional a un objeto de datos adicional.

</dd> <dt>

*ExtraDataSize* \[ en, opcional\]
</dt> <dd>

Tamaño de los datos adicionales.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 

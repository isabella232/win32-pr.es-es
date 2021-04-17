---
description: Elimina una tabla de cadenas.
ms.assetid: a3ac1672-f898-44a0-bb7b-64ac24bdb9bf
title: pSetupStringTableDestroy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableDestroy
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 472ee152d98c064edb8bac5d4de849b505b634da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670517"
---
# <a name="psetupstringtabledestroy-function"></a>pSetupStringTableDestroy función)

\[Esta función no está disponible en Windows Vista ni Windows Server 2008.\]

Elimina una tabla de cadenas.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI pSetupStringTableDestroy(
  _In_ PVOID StringTable
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StringTable* \[ de\]
</dt> <dd>

Puntero a la tabla de cadenas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 

---
description: Recupera una cadena de mensaje sin formato cuando se proporciona un identificador de código de error (IDA).
ms.assetid: 3869e0c0-b3ec-4409-b071-04fd793ebf93
title: JetErrIDARawMessage función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrIDARawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 8a904a99577a6fa0fd6955f4c78906b470ea96b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671544"
---
# <a name="jeterridarawmessage-function"></a>JetErrIDARawMessage función)

Recupera una cadena de mensaje sin formato cuando se proporciona un identificador de código de error (IDA).

## <a name="syntax"></a>Sintaxis


```C++
JET_ERR JetErrIDARawMessage(
   JETERR_IDA           Ida,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ida* 
</dt> <dd>

Número que se asigna a un código de error específico y se muestra al usuario.

</dd> <dt>

*pMessage* 
</dt> <dd>

Puntero al mensaje de error.

</dd> <dt>

*cbMessage* 
</dt> <dd>

Recuento del número de bytes del mensaje de error.

</dd> <dt>

*pcbActual* 
</dt> <dd>

Puntero al número real de bytes leídos.

</dd> <dt>

*pContextId* 
</dt> <dd>

Puntero al identificador de contexto que está asociado con el archivo de ayuda.

</dd> <dt>

*pwszHelp/archivo* 
</dt> <dd>

Un puntero a un puntero al archivo que explica el error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve **jet \_ errSuccess**; de lo contrario, devuelve un mensaje sin formato que indica el motivo específico del error.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 

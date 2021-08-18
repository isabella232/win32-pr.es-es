---
description: Recupera un identificador de código de error (IDA) y una cadena de mensaje sin formato cuando se proporciona un error jet.
ms.assetid: f90b6986-a8d5-430e-94b3-176012c7e282
title: Función JetErrRawMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrRawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: efc7332530b5b03b0c9150adb8b0e105d0e5d17eeae9bbc485fb073391de2cad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749686"
---
# <a name="jeterrrawmessage-function"></a>Función JetErrRawMessage

Recupera un identificador de código de error (IDA) y una cadena de mensaje sin formato cuando se proporciona un error jet.

## <a name="syntax"></a>Sintaxis


```C++
JET_ERR JetErrRawMessage(
   JET_ERR              err,
   JETERR_IDA           *pIda,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Err* 
</dt> <dd>

Error de Jet que corresponde a la información que se obtiene.

</dd> <dt>

*pIda* 
</dt> <dd>

Puntero a la IDA.

</dd> <dt>

*pMessage* 
</dt> <dd>

Puntero al mensaje de error.

</dd> <dt>

*cbMessage* 
</dt> <dd>

Recuento del número de bytes del mensaje de error.

</dd> <dt>

*actual* 
</dt> <dd>

Puntero al número real de bytes leídos.

</dd> <dt>

*pContextId* 
</dt> <dd>

Puntero al identificador de contexto asociado al archivo de ayuda.

</dd> <dt>

*pwszHelp/file* 
</dt> <dd>

Apunta a un puntero al archivo que explica el error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve **jet \_ errSuccess;** de lo contrario, devuelve un mensaje de error sin formato que indica el motivo específico del error.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 

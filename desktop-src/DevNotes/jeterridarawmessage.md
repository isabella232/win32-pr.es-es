---
description: Recupera una cadena de mensaje sin formato cuando se proporciona un identificador de código de error (IDA).
ms.assetid: 3869e0c0-b3ec-4409-b071-04fd793ebf93
title: Función JetErrIDARawMessage
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
ms.openlocfilehash: 39bd07b3ac75bed85ff26dd7f014420ebaca8be16d6f0195d40e9161c0905496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955764"
---
# <a name="jeterridarawmessage-function"></a>Función JetErrIDARawMessage

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

Puntero a un puntero al archivo que explica el error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve **jet \_ errSuccess;** de lo contrario, devuelve un mensaje sin formato que indica el motivo específico del error.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 

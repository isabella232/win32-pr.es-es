---
description: Recupera un identificador de código de error (IDA) y una cadena de mensaje sin formato cuando se proporciona un error de jet.
ms.assetid: f90b6986-a8d5-430e-94b3-176012c7e282
title: JetErrRawMessage función)
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
ms.openlocfilehash: 1b52fa519bee3abacd0cd9bd7e8eaaa0676d007c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649519"
---
# <a name="jeterrrawmessage-function"></a>JetErrRawMessage función)

Recupera un identificador de código de error (IDA) y una cadena de mensaje sin formato cuando se proporciona un error de jet.

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

*ERR* 
</dt> <dd>

Error de jet que corresponde a la información que se obtiene.

</dd> <dt>

*pIda* 
</dt> <dd>

Puntero a IDA.

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

Apunta a un puntero al archivo que explica el error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve **jet \_ errSuccess**; de lo contrario, devuelve un mensaje de error sin formato que indica el motivo específico del error.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 

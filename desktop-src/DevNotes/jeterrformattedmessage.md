---
description: Recupera un identificador de código de error (IDA) y crea la cadena de presentación final cuando se proporciona un error jet y la información de error extendida.
ms.assetid: 961da4fb-cb70-4f3d-a4a4-1774be7a05f4
title: Función JetErrFormattedMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrFormattedMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 8b0fa6eb0ac4bc29e5657d3e58d9be1c27188a0faf7c7d68281ceca239dea8e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955784"
---
# <a name="jeterrformattedmessage-function"></a>Función JetErrFormattedMessage

Recupera un identificador de código de error (IDA) y crea la cadena de presentación final cuando se proporciona un error jet y la información de error extendida.

## <a name="syntax"></a>Sintaxis


```C++
JET_ERR JetErrFormattedMessage(
   JET_ERR              err,
   JETERR_EXTERR        *pExtendedErrorInfo,
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

Número de error de Jet que se usa para buscar y dar formato al mensaje de error que se puede mostrar.

</dd> <dt>

*pExtendedErrorInfo* 
</dt> <dd>

Toda la información de error de Jet, incluido el nombre de la base de datos, el nombre de la tabla y cualquier información de error secundaria.

</dd> <dt>

*pIda* 
</dt> <dd>

Puntero al IDA asociado al código de error específico.

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

Si la función se realiza correctamente, devuelve **jet \_ errSuccess;** de lo contrario, devuelve un mensaje de error con formato que indica el motivo específico del error.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 

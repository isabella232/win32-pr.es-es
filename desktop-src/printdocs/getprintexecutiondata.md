---
description: GetPrintExecutionData recupera el contexto de impresión actual.
ms.assetid: bb9506aa-a0da-46bc-a86a-84a79587cd50
title: Función GetPrintExecutionData (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintExecutionData
api_type:
- DllExport
api_location:
- winspool.drv
ms.openlocfilehash: 0bbe08e82fb8f753d6e4fd23776618cb5f555b390434fdd0feddd231aaebc635
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971354"
---
# <a name="getprintexecutiondata-function"></a>Función GetPrintExecutionData

**GetPrintExecutionData recupera** el contexto de impresión actual.

> [!Note]  
> Esta función está pensada para su uso por los controladores de impresora que se ejecutan en el contexto del colador de impresión.

 

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI GetPrintExecutionData(
  _Out_ PRINT_EXECUTION_DATA *pData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pData* \[ out\]
</dt> <dd>

Puntero a una variable que recibe la dirección de la [**estructura PRINT \_ EXECUTION \_ DATA.**](print-execution-data.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si la función se realiza correctamente; en caso **contrario, FALSE**. Si el valor devuelto es **FALSE,** llame [**a GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener el estado del error.

## <a name="remarks"></a>Comentarios

Los controladores de impresora deben llamar a [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) en el módulo winspool.drv para obtener la dirección de la función **GetPrintExecutionData** porque **GetPrintExecutionData** no se admite en Windows Vista ni en versiones anteriores de Windows.

**GetPrintExecutionData** solo produce un error si el valor de *pData* es **NULL.**

El valor del miembro **clientAppPID** de [**PRINT EXECUTION \_ \_ DATA**](print-execution-data.md) solo es significativo si el valor de **context** es PRINT EXECUTION **CONTEXT \_ \_ \_ WOW64**. Si el valor de **context no** es PRINT EXECUTION **CONTEXT \_ \_ \_ WOW64**, el valor de **clientAppPID** es 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**CONTEXTO DE \_ EJECUCIÓN DE \_ IMPRESIÓN**](print-execution-context.md)
</dt> <dt>

[**IMPRIMIR \_ DATOS DE \_ EJECUCIÓN**](print-execution-data.md)
</dt> </dl>

 


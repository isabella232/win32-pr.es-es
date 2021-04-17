---
description: GetPrintExecutionData recupera el contexto de impresión actual.
ms.assetid: bb9506aa-a0da-46bc-a86a-84a79587cd50
title: Función GetPrintExecutionData (winspool. h)
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
ms.openlocfilehash: a1b2f2674c9ef186338c91ed2e4500d8408964d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697695"
---
# <a name="getprintexecutiondata-function"></a>GetPrintExecutionData función)

**GetPrintExecutionData** recupera el contexto de impresión actual.

> [!Note]  
> Esta función está pensada para que la usen los controladores de impresora que se ejecutan en el contexto del administrador de trabajos de impresión.

 

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI GetPrintExecutionData(
  _Out_ PRINT_EXECUTION_DATA *pData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdata* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe la dirección de la estructura [**de \_ \_ datos**](print-execution-data.md) de la ejecución de impresión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si la función se ejecuta correctamente; en caso contrario, **false**. Si el valor devuelto es **false**, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener el estado de error.

## <a name="remarks"></a>Observaciones

Los controladores de impresora deben llamar a [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) en el módulo winspool. drv para obtener la dirección de la función **GetPrintExecutionData** porque **GetPrintExecutionData** no se admite en Windows Vista o en versiones anteriores de Windows.

**GetPrintExecutionData** solo produce un error si el valor de *pdata* es **null**.

El valor del miembro **clientAppPID** de los [**\_ \_ datos de ejecución de impresión**](print-execution-data.md) solo es significativo si el valor de **Context** es el **contexto de ejecución de impresión \_ \_ \_ WOW64**. Si el valor de **Context** no es el **contexto de ejecución de impresión \_ \_ \_ WOW64**, el valor de **clientAppPID** es 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**\_contexto de ejecución de impresión \_**](print-execution-context.md)
</dt> <dt>

[**IMPRIMIR \_ datos de ejecución \_**](print-execution-data.md)
</dt> </dl>

 


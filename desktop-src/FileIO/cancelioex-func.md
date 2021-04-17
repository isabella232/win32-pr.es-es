---
description: Marca las operaciones de e/s pendientes para el identificador de archivo especificado. La función solo cancela las operaciones de e/s en el proceso actual, independientemente del subproceso que haya creado la operación de e/s.
ms.assetid: a2ce13b8-7da6-4848-848d-901d9667c2e3
title: Función CancelIoEx (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIoEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 3de44762ad9a230a9d8cc410c4ba3ae7c2d9964e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687405"
---
# <a name="cancelioex-function"></a>CancelIoEx función)

Marca las operaciones de e/s pendientes para el identificador de archivo especificado. La función solo cancela las operaciones de e/s en el proceso actual, independientemente del subproceso que haya creado la operación de e/s.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CancelIoEx(
  _In_     HANDLE       hFile,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFile* \[ de\]
</dt> <dd>

Identificador del archivo.

</dd> <dt>

*lpOverlapped* \[ en, opcional\]
</dt> <dd>

Puntero a una estructura de datos [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) que contiene los datos usados para la e/s asincrónica.

Si este parámetro es **null**, se cancelan todas las solicitudes de e/s para el parámetro *hFile* .

Si este parámetro no es **null**, solo las solicitudes de e/s específicas emitidas para el archivo con la estructura superpuesta *lpOverlapped* especificada se marcan como canceladas, lo que significa que puede cancelar una o más solicitudes, mientras que la función [**CancelIo**](cancelio.md) cancela todas las solicitudes pendientes en un identificador de archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es distinto de cero. La operación de cancelación para todas las operaciones de e/s pendientes emitidas por el proceso de llamada para el identificador de archivo especificado se solicitó correctamente. La aplicación no debe liberar o reutilizar la estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) asociada a las operaciones de e/s canceladas hasta que se hayan completado. El subproceso puede usar la función [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) para determinar cuándo se han completado las operaciones de e/s.

Si se produce un error en la función, el valor devuelto es 0 (cero). Para obtener información de error extendida, llame a la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

Si esta función no encuentra una solicitud para cancelar, el valor devuelto es 0 (cero) y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve **error \_ no \_ encontrado**.

## <a name="remarks"></a>Observaciones

La función **CancelIoEx** permite cancelar solicitudes en subprocesos distintos del subproceso que realiza la llamada. La función [**CancelIo**](cancelio.md) solo cancela las solicitudes en el mismo subproceso que llamó a la función **CancelIo** . **CancelIoEx** cancela solo e/s pendientes en el identificador, no cambia el estado del identificador. Esto significa que no se puede confiar en el estado del identificador porque no se puede saber si la operación se completó correctamente o se canceló.

Si hay alguna operación de e/s pendiente en curso para el identificador de archivo especificado, la función **CancelIoEx** las marca para su cancelación. La mayoría de los tipos de operaciones se pueden cancelar inmediatamente; otras operaciones pueden continuar hasta su finalización antes de que se cancelen realmente y se notifique al llamador. La función **CancelIoEx** no espera a que se completen todas las operaciones canceladas.

Si el identificador de archivo está asociado a un puerto de finalización, un paquete de finalización de e/s no se pone en cola en el puerto si se cancela correctamente una operación sincrónica. En el caso de las operaciones asincrónicas aún pendientes, la operación de cancelación pondrá en cola un paquete de finalización de e/s.

La operación que se está cancelando se completa con uno de los tres Estados siguientes: debe comprobar el estado de finalización para determinar el estado de finalización. Los tres Estados son:

-   La operación se completó con normalidad. Esto puede ocurrir incluso si se canceló la operación, porque es posible que no se haya enviado la solicitud de cancelación en el tiempo para cancelar la operación.
-   Operación cancelada. La función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve la **operación de error \_ \_ anulada**.
-   No se pudo realizar la operación debido a otro error. La función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el código de error pertinente.

En Windows 8 y Windows Server 2012, esta función es compatible con las siguientes tecnologías.



| Technology                                           | Compatible      |
|------------------------------------------------------|----------------|
| Protocolo bloque de mensajes del servidor (SMB) 3,0<br/>   | Sí<br/> |
| Conmutación por error transparente SMB 3,0 (TFO)<br/>        | Sí<br/> |
| SMB 3,0 con recursos compartidos de archivos de escalabilidad horizontal (por lo tanto)<br/>   | Sí<br/> |
| Sistema de archivos Volumen compartido de clúster (CsvFS)<br/> | Sí<br/> |
| Sistema de archivos resistente a errores (ReFS)<br/>              | Sí<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                                                                                                                                                                                                                   |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                                                                                                                                                                                                             |
| Encabezado<br/>                   | <dl> <dt>IoAPI. h (incluye Windows. h); </dt> <dt>Winbase. h en Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista (incluido Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                 |
| Archivo DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CancelIo**](cancelio.md)
</dt> <dt>

[**CancelSynchronousIo**](cancelsynchronousio-func.md)
</dt> <dt>

[Cancelar operaciones de e/s pendientes](canceling-pending-i-o-operations.md)
</dt> <dt>

[Funciones de administración de archivos](file-management-functions.md)
</dt> <dt>

[E/s sincrónica y asincrónica](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 


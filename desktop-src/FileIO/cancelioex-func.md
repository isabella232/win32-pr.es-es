---
description: Marca las operaciones de E/S pendientes para el identificador de archivo especificado. La función solo cancela las operaciones de E/S en el proceso actual, independientemente del subproceso que haya creado la operación de E/S.
ms.assetid: a2ce13b8-7da6-4848-848d-901d9667c2e3
title: Función CancelIoEx (IoAPI.h)
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
ms.openlocfilehash: 3726bf221073f33d87481d7a6bb6f2f4fd459812616975fba38d9a9a8f0334ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582615"
---
# <a name="cancelioex-function"></a>Función CancelIoEx

Marca las operaciones de E/S pendientes para el identificador de archivo especificado. La función solo cancela las operaciones de E/S en el proceso actual, independientemente del subproceso que haya creado la operación de E/S.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CancelIoEx(
  _In_     HANDLE       hFile,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFile* \[ En\]
</dt> <dd>

Identificador del archivo.

</dd> <dt>

*lpOverlapped* \[ in, opcional\]
</dt> <dd>

Puntero a una estructura [**de datos OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) que contiene los datos usados para la E/S asincrónica.

Si este parámetro es **NULL,** se cancelan todas las solicitudes de E/S para el parámetro *hFile.*

Si este parámetro no es **NULL,** solo las solicitudes de E/S específicas que se emitieron para el archivo con la estructura superpuesta *lpOverlapped* especificada se marcan como canceladas, lo que significa que puede cancelar una o varias solicitudes, mientras que la función [**CancelIo**](cancelio.md) cancela todas las solicitudes pendientes en un identificador de archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es distinto de cero. Se solicitó correctamente la operación de cancelación para todas las operaciones de E/S pendientes emitidas por el proceso de llamada para el identificador de archivo especificado. La aplicación no debe liberar ni reutilizar la estructura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) asociada a las operaciones de E/S canceladas hasta que se hayan completado. El subproceso puede usar la [**función GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) para determinar cuándo se han completado las propias operaciones de E/S.

Si se produce un error en la función, el valor devuelto es 0 (cero). Para obtener información de error extendida, llame a [**la función GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

Si esta función no encuentra una solicitud para cancelar, el valor devuelto es 0 (cero) y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve **ERROR NOT \_ \_ FOUND**.

## <a name="remarks"></a>Comentarios

La **función CancelIoEx** permite cancelar solicitudes en subprocesos distintos del subproceso que realiza la llamada. La [**función CancelIo**](cancelio.md) solo cancela solicitudes en el mismo subproceso que llamó a la **función CancelIo.** **CancelIoEx** solo cancela E/S pendientes en el identificador, no cambia el estado del identificador; Esto significa que no puede confiar en el estado del identificador porque no puede saber si la operación se completó correctamente o se canceló.

Si hay alguna operación de E/S pendiente en curso para el identificador de archivo especificado, la **función CancelIoEx** las marca como cancelación. La mayoría de los tipos de operaciones se pueden cancelar inmediatamente; Otras operaciones pueden continuar hasta su finalización antes de que se cancelen realmente y se notifique al autor de la llamada. La **función CancelIoEx** no espera a que se completen todas las operaciones canceladas.

Si el identificador de archivo está asociado a un puerto de finalización, un paquete de finalización de E/S no se pone en cola en el puerto si se cancela correctamente una operación sincrónica. Para las operaciones asincrónicas aún pendientes, la operación de cancelación pondrá en cola un paquete de finalización de E/S.

La operación que se cancela se completa con uno de los tres estados; debe comprobar el estado de finalización para determinar el estado de finalización. Los tres estados son:

-   La operación se completó con normalidad. Esto puede ocurrir incluso si la operación se canceló, ya que es posible que la solicitud de cancelación no se haya enviado a tiempo para cancelar la operación.
-   Operación cancelada. La [**función GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve **ERROR OPERATION \_ \_ ABORTED.**
-   Error en la operación con otro error. La [**función GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el código de error pertinente.

En Windows 8 y Windows Server 2012, esta función es compatible con las siguientes tecnologías.



| Tecnología                                           | Compatible      |
|------------------------------------------------------|----------------|
| Protocolo bloque de mensajes de servidor (SMB) 3.0<br/>   | Sí<br/> |
| Conmutación por error transparente (TFO) de SMB 3.0<br/>        | Sí<br/> |
| SMB 3.0 con recursos compartidos de archivos de escalabilidad horizontal (SO)<br/>   | Sí<br/> |
| Volumen compartido de clúster de archivos (CsvFS)<br/> | Sí<br/> |
| Sistema de archivos resistente a errores (ReFS)<br/>              | Sí<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                                                                                                                                                                                                                   |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                                                                                                                                                                                                             |
| Header<br/>                   | <dl> <dt>IoAPI.h (incluir Windows.h);</dt> <dt>WinBase.h en Windows Server 2008 R2, Windows 7, Windows Server 2008 y Windows Vista (incluido Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                 |
| Archivo DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CancelIo**](cancelio.md)
</dt> <dt>

[**CancelSynchronousIo**](cancelsynchronousio-func.md)
</dt> <dt>

[Cancelación de operaciones de E/S pendientes](canceling-pending-i-o-operations.md)
</dt> <dt>

[Funciones de administración de archivos](file-management-functions.md)
</dt> <dt>

[E/S sincrónica y asincrónica](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 


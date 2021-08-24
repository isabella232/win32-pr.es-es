---
description: Recupera varias entradas de puerto de finalización simultáneamente.
ms.assetid: 3996c02c-562c-4697-a091-e241ad54b239
title: Función GetQueuedCompletionStatusEx (IoAPI.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetQueuedCompletionStatusEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: f81bc0c997e3637fa941cb5a23f6394ba1f585566c8d633cadb00c9fd75ac805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696125"
---
# <a name="getqueuedcompletionstatusex-function"></a>Función GetQueuedCompletionStatusEx

Recupera varias entradas de puerto de finalización simultáneamente. Espera a que se completen las operaciones de E/S pendientes asociadas al puerto de finalización especificado.

Para quitar de la cola los paquetes de finalización de E/S de uno en uno, use la [**función GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI GetQueuedCompletionStatusEx(
  _In_  HANDLE             CompletionPort,
  _Out_ LPOVERLAPPED_ENTRY lpCompletionPortEntries,
  _In_  ULONG              ulCount,
  _Out_ PULONG             ulNumEntriesRemoved,
  _In_  DWORD              dwMilliseconds,
  _In_  BOOL               fAlertable
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CompletionPort* \[ En\]
</dt> <dd>

Identificador del puerto de finalización. Para crear un puerto de finalización, use [**la función CreateIoCompletionPort.**](createiocompletionport.md)

</dd> <dt>

*lpCompletionPortEntries* \[ out\]
</dt> <dd>

En la entrada, apunta a una matriz preasignada de [**estructuras OVERLAPPED \_ ENTRY.**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry)

En la salida, recibe una matriz de [**estructuras OVERLAPPED \_ ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) que contiene las entradas. *UlNumEntriesRemoved* proporciona el número de elementos de matriz.

El número de bytes transferidos durante cada E/S, la clave de finalización que indica en qué archivo se produjo cada E/S y la dirección de estructura superpuesta usada en cada E/S original se devuelven en la matriz *lpCompletionPortEntries.*

</dd> <dt>

*ulCount* \[ En\]
</dt> <dd>

Número máximo de entradas que se quitarán.

</dd> <dt>

*ulNumEntriesRemoved* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número de entradas quitadas realmente.

</dd> <dt>

*dwMilliseconds* \[ En\]
</dt> <dd>

Número de milisegundos que el autor de la llamada está dispuesto a esperar a que aparezca un paquete de finalización en el puerto de finalización. Si un paquete de finalización no aparece dentro del tiempo especificado, la función se completa con el tiempo de espera y devuelve **FALSE.**

Si *dwMilliseconds* es **INFINITE** (0xFFFFFFFF), la función nunca pasará el tiempo de espera. Si *dwMilliseconds* es cero y no hay ninguna operación de E/S para quitar de la cola, la función se tiempo de espera inmediatamente.

</dd> <dt>

*fAlertable* \[ En\]
</dt> <dd>

Si este parámetro es **FALSE**, la función no se devuelve hasta que haya transcurrido el período de tiempo de espera o se recupere una entrada.

Si el parámetro es **TRUE** y no hay ninguna entrada disponible, la función realiza una espera que se puede alertar. El subproceso devuelve cuando el sistema pone en cola una rutina de finalización de E/S o APC en el subproceso y el subproceso ejecuta la función .

Una rutina de finalización se pone en cola cuando se ha completado la función [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) o [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) en la que se especificó y el subproceso que realiza la llamada es el subproceso que inició la operación. Un APC se pone en cola cuando se llama a [**QueueUserAPC.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero (**TRUE**) si es correcto o cero (**FALSE**) de lo contrario.

Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

Esta función asocia un subproceso al puerto de finalización especificado. Un subproceso se puede asociar a un puerto de finalización como máximo.

Esta función devuelve **TRUE cuando** se completa al menos una E/S pendiente, pero es posible que se haya realizado un error en una o varias operaciones de E/S. Tenga en cuenta que es el usuario de esta función quien debe comprobar la lista de entradas devueltas en el parámetro *lpCompletionPortEntries* para determinar cuál de ellas corresponde a las posibles operaciones de E/S con error al consultar el estado contenido en el miembro **lpOverlapped** en cada [**OVERLAPPED \_ ENTRY.**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry)

Esta función devuelve **FALSE cuando** no se ha descolado ninguna operación de E/S. Esto suele significar que se produjo un error al procesar los parámetros para esta llamada, o que el identificador *CompletionPort* se cerró o no es válido de otro modo. La [**función GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) proporciona información de error extendida.

Si se produce un error en una llamada a [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) porque el identificador asociado a él está cerrado, la función devuelve **FALSE** y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devolverá **ERROR \_ ABANDONED \_ WAIT \_ 0.**

Las aplicaciones de servidor pueden tener varios subprocesos que llaman a la función **GetQueuedCompletionStatusEx** para el mismo puerto de finalización. A medida que se completan las operaciones de E/S, se ponen en cola en este puerto en orden primero en salir. Si un subproceso está esperando activamente esta llamada, una o varias solicitudes en cola completan la llamada solo para ese subproceso.

Para obtener más información sobre la teoría del puerto de finalización de E/S, el uso y las funciones asociadas, vea [Puertos de finalización de E/S.](i-o-completion-ports.md)

En Windows 8 y Windows Server 2012, esta función es compatible con las siguientes tecnologías.



| Tecnología                                           | Compatible      |
|------------------------------------------------------|----------------|
| Protocolo bloque de mensajes de servidor (SMB) 3.0<br/>   | Sí<br/> |
| Conmutación por error transparente (TFO) de SMB 3.0<br/>        | Sí<br/> |
| SMB 3.0 con recursos compartidos de archivos de escalabilidad horizontal (SO)<br/>   | Sí<br/> |
| Volumen compartido de clúster file system (CsvFS)<br/> | Sí<br/> |
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

**Temas de información general**
</dt> <dt>

[Funciones de administración de archivos](file-management-functions.md)
</dt> <dt>

[Puertos de finalización de E/S](i-o-completion-ports.md)
</dt> <dt>

[Uso de los Windows encabezados](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

**Funciones**
</dt> <dt>

[**ConnectNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
</dt> <dt>

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md)
</dt> <dt>

[**TransactNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
</dt> <dt>

[**WaitCommEvent**](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> </dl>

 


---
description: Recupera simultáneamente varias entradas del puerto de finalización.
ms.assetid: 3996c02c-562c-4697-a091-e241ad54b239
title: Función GetQueuedCompletionStatusEx (IoAPI. h)
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
ms.openlocfilehash: d45471cc066e6de7cb388036e06e727fe828a532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669693"
---
# <a name="getqueuedcompletionstatusex-function"></a>GetQueuedCompletionStatusEx función)

Recupera simultáneamente varias entradas del puerto de finalización. Espera a que se completen las operaciones de e/s pendientes asociadas al puerto de finalización especificado.

Para quitar de la cola los paquetes de finalización de e/s de uno en uno, use la función [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

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

*CompletionPort* \[ de\]
</dt> <dd>

Identificador del puerto de finalización. Para crear un puerto de finalización, utilice la función [**CreateIoCompletionPort**](createiocompletionport.md) .

</dd> <dt>

*lpCompletionPortEntries* \[ enuncia\]
</dt> <dd>

En la entrada, apunta a una matriz preasignada de estructuras de [**\_ entrada superpuestas**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) .

En la salida, recibe una matriz de estructuras de [**\_ entrada superpuestas**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) que contienen las entradas. El número de elementos de matriz lo proporciona *ulNumEntriesRemoved*.

Número de bytes transferidos durante cada operación de e/s, la clave de finalización que indica en qué archivo se produjo cada e/s y la dirección de la estructura superpuesta utilizada en cada e/s original se devuelve en la matriz *lpCompletionPortEntries* .

</dd> <dt>

*ulCount* \[ de\]
</dt> <dd>

Número máximo de entradas que se van a quitar.

</dd> <dt>

*ulNumEntriesRemoved* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el número de entradas realmente quitadas.

</dd> <dt>

*dwMilliseconds* \[ de\]
</dt> <dd>

Número de milisegundos que el llamador está dispuesto a esperar a que aparezca un paquete de finalización en el puerto de finalización. Si un paquete de finalización no aparece en el tiempo especificado, la función agota el tiempo de espera y devuelve **false**.

Si *dwMilliseconds* es **infinito** (0xFFFFFFFF), la función nunca agotará el tiempo de espera. Si *dwMilliseconds* es cero y no hay ninguna operación de e/s para quitar de la cola, se agotará el tiempo de espera de la función de inmediato.

</dd> <dt>

*fAlertable* \[ de\]
</dt> <dd>

Si este parámetro es **false**, la función no devuelve ningún resultado hasta que haya transcurrido el período de tiempo de espera o se haya recuperado una entrada.

Si el parámetro es **true** y no hay ninguna entrada disponible, la función realiza una espera de alerta. El subproceso devuelve cuando el sistema pone en cola una rutina de finalización de e/s o APC en el subproceso y el subproceso ejecuta la función.

Una rutina de finalización se pone en cola cuando se ha completado la función [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) o [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) en la que se especificó, y el subproceso que realiza la llamada es el subproceso que inició la operación. Un APC se pone en cola cuando se llama a [**QueueUserAPC**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero (**true**) si es correcto o cero (**false**) en caso contrario.

Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

Esta función asocia un subproceso al puerto de finalización especificado. Un subproceso se puede asociar a un puerto de finalización como máximo.

Esta función devuelve **true** cuando se ha completado al menos una e/s pendiente, pero es posible que se haya producido un error en una o varias operaciones de e/s. Tenga en cuenta que el usuario de esta función puede comprobar la lista de entradas devueltas en el parámetro *lpCompletionPortEntries* para determinar cuáles se corresponden con las posibles operaciones de e/s con errores examinando el estado contenido en el miembro **lpOverlapped** de cada [**\_ entrada superpuesta**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry).

Esta función devuelve **false** cuando no se quitó la cola de ninguna operación de e/s. Esto suele significar que se ha producido un error al procesar los parámetros de esta llamada o que el identificador *CompletionPort* se cerró o no es válido. La función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) proporciona información de error extendida.

Si se produce un error en una llamada a [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) porque el identificador asociado a él está cerrado, la función devuelve **false** y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devolverá el error que se ha **\_ abandonado \_ Wait \_ 0**.

Las aplicaciones de servidor pueden tener varios subprocesos que llaman a la función **GetQueuedCompletionStatusEx** para el mismo puerto de finalización. A medida que se completan las operaciones de e/s, se ponen en cola en este puerto en el orden de los primeros en salir. Si un subproceso está esperando activamente en esta llamada, una o varias solicitudes en cola completan la llamada solo para ese subproceso.

Para obtener más información sobre la teoría del puerto de finalización de e/s, el uso y las funciones asociadas, consulte [puertos de finalización de e/s](i-o-completion-ports.md).

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

**Temas de información general**
</dt> <dt>

[Funciones de administración de archivos](file-management-functions.md)
</dt> <dt>

[Puertos de finalización de e/s](i-o-completion-ports.md)
</dt> <dt>

[Usar los encabezados de Windows](/windows/desktop/WinProg/using-the-windows-headers)
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

 


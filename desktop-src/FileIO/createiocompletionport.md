---
description: Crea un puerto de finalización de entrada/salida (E/S) y lo asocia a un identificador de archivo especificado, o crea un puerto de finalización de E/S que aún no está asociado a un identificador de archivo, lo que permite la asociación en un momento posterior.
ms.assetid: 40cb47fc-7b15-47f6-bee2-2611d4686053
title: Función CreateIoCompletionPort (IoAPI.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateIoCompletionPort
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 6612c3087841aa0c13f131581f8a05c29403e4fccf81bd6f0dc338b1dd9e42a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083165"
---
# <a name="createiocompletionport-function"></a>Función CreateIoCompletionPort

Crea un puerto de finalización de entrada/salida (E/S) y lo asocia a un identificador de archivo especificado, o crea un puerto de finalización de E/S que aún no está asociado a un identificador de archivo, lo que permite la asociación en un momento posterior.

La asociación de una instancia de un identificador de archivo abierto con un puerto de finalización de E/S permite a un proceso recibir una notificación de la finalización de operaciones asincrónicas de E/S que implican ese identificador de archivo.

> [!Note]
>
> El término *identificador de archivo* tal como se usa aquí hace referencia a una abstracción del sistema que representa un punto de conexión de E/S superpuesto, no solo un archivo en disco. Los objetos del sistema que admiten E/S superpuestas, como puntos de conexión de red, sockets TCP, canalizaciones con nombre y ranuras de correo, se pueden usar como identificadores de archivo. Para más información, consulte la sección Comentarios.

 

## <a name="syntax"></a>Sintaxis


```C++
HANDLE WINAPI CreateIoCompletionPort(
  _In_     HANDLE    FileHandle,
  _In_opt_ HANDLE    ExistingCompletionPort,
  _In_     ULONG_PTR CompletionKey,
  _In_     DWORD     NumberOfConcurrentThreads
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FileHandle* \[ En\]
</dt> <dd>

Identificador de archivo abierto o **VALOR DE IDENTIFICADOR NO \_ \_ VÁLIDO.**

El identificador debe ser para un objeto que admita E/S superpuesta.

Si se proporciona un identificador, debe haber abierto para la finalización de E/S superpuesta. Por ejemplo, debe especificar la marca **FILE \_ FLAG \_ OVERLAPPED** al usar la [**función CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para obtener el identificador.

Si **se especifica INVALID HANDLE \_ \_ VALUE,** la función crea un puerto de finalización de E/S sin asociarlo a un identificador de archivo. En este caso, el *parámetro ExistingCompletionPort* debe ser **NULL** y se omite el parámetro *CompletionKey.*

</dd> <dt>

*ExistingCompletionPort* \[ in, opcional\]
</dt> <dd>

Identificador de un puerto de finalización de E/S existente o **NULL.**

Si este parámetro especifica un puerto de finalización de E/S existente, la función lo asocia al identificador especificado por el *parámetro FileHandle.* La función devuelve el identificador del puerto de finalización de E/S existente si se realiza correctamente; no crea un nuevo puerto de finalización de E/S.

Si este parámetro es **NULL,** la función crea un nuevo puerto de finalización de E/S y, si el parámetro *FileHandle* es válido, lo asocia al nuevo puerto de finalización de E/S. De lo contrario, no se produce ninguna asociación de identificador de archivo. La función devuelve el identificador al nuevo puerto de finalización de E/S si se realiza correctamente.

</dd> <dt>

*CompletionKey* \[ En\]
</dt> <dd>

Clave de finalización definida por el usuario por identificador que se incluye en cada paquete de finalización de E/S para el identificador de archivo especificado. Para obtener más información, vea la sección Comentarios.

</dd> <dt>

*NumberOfConcurrentThreads* \[ En\]
</dt> <dd>

Número máximo de subprocesos que el sistema operativo puede permitir para procesar simultáneamente paquetes de finalización de E/S para el puerto de finalización de E/S. Este parámetro se omite si el *parámetro ExistingCompletionPort* no es **NULL.**

Si este parámetro es cero, el sistema permite tantos subprocesos en ejecución simultáneamente como procesadores en el sistema.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es el identificador de un puerto de finalización de E/S:

-   Si el *parámetro ExistingCompletionPort* era **NULL,** el valor devuelto es un nuevo identificador.

-   Si el *parámetro ExistingCompletionPort* era un identificador de puerto de finalización de E/S válido, el valor devuelto es ese mismo identificador.

-   Si el *parámetro FileHandle* era un identificador válido, ese identificador de archivo ahora está asociado al puerto de finalización de E/S devuelto.

Si se produce un error en la función, el valor devuelto es **NULL.** Para obtener información de error extendida, llame a [**la función GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Comentarios

Se puede indicar al sistema de E/S que envíe paquetes de notificación de finalización de E/S a los puertos de finalización de E/S, donde se ponen en cola. La **función CreateIoCompletionPort** proporciona esta funcionalidad.

Un puerto de finalización de E/S y su identificador están asociados al proceso que lo creó y no se pueden compartir entre procesos. Sin embargo, un único identificador se puede compartir entre subprocesos en el mismo proceso.

**CreateIoCompletionPort** se puede usar en tres modos distintos:

-   Cree solo un puerto de finalización de E/S sin asociarlo a un identificador de archivo.
-   Asocie un puerto de finalización de E/S existente a un identificador de archivo.
-   Realice la creación y la asociación en una sola llamada.

Para crear un puerto de finalización de E/S sin asociarlo, establezca el parámetro *FileHandle* en **INVALID HANDLE \_ \_ VALUE**, el parámetro *ExistingCompletionPort* en **NULL** y el parámetro *CompletionKey* en cero (que se omite en este caso). Establezca el *parámetro NumberOfConcurrentThreads* en el valor de simultaneidad deseado para el nuevo puerto de finalización de E/S, o cero para el valor predeterminado (el número de procesadores del sistema).

El identificador pasado en el *parámetro FileHandle* puede ser cualquier identificador que admita E/S superpuesta. Normalmente, se trata de un identificador abierto por la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) mediante la marca **FILE FLAG \_ \_ OVERLAPPED** (por ejemplo, archivos, ranuras de correo y canalizaciones). Los objetos creados por otras funciones, como [**socket,**](/windows/desktop/api/winsock2/nf-winsock2-socket) también se pueden asociar a un puerto de finalización de E/S. Para obtener un ejemplo de uso de sockets, [**vea AcceptEx**](/windows/desktop/api/mswsock/nf-mswsock-acceptex). Un identificador solo se puede asociar a un puerto de finalización de E/S y, una vez realizada la asociación, el identificador permanece asociado a ese puerto de finalización de E/S hasta que se cierra.

Para obtener más información sobre la teoría del puerto de finalización de E/S, el uso y las funciones asociadas, vea [Puertos de finalización de E/S.](i-o-completion-ports.md)

Se pueden asociar varios identificadores de archivo a un único puerto de finalización de E/S llamando a **CreateIoCompletionPort** varias veces con el mismo identificador de puerto de finalización de E/S en el parámetro *ExistingCompletionPort* y un identificador de archivo diferente en el *parámetro FileHandle* cada vez.

Use el *parámetro CompletionKey* para ayudar a la aplicación a realizar el seguimiento de las operaciones de E/S que se han completado. **CreateIoCompletionPort** no usa este valor para el control funcional; en su lugar, se adjunta al identificador de archivo especificado en el *parámetro FileHandle* en el momento de la asociación con un puerto de finalización de E/S. Esta clave de finalización debe ser única para cada identificador de archivo y acompaña al identificador de archivo a lo largo del proceso interno de la cola de finalización. Se devuelve en la llamada de [**función GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) cuando llega un paquete de finalización. La función [**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) también usa el parámetro *CompletionKey* para poner en cola sus propios paquetes de finalización de propósito especial.

Después de asociar una instancia de un identificador abierto a un puerto de finalización de E/S, no se puede usar en las funciones [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) o [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) porque estas funciones tienen sus propios mecanismos asincrónicos de E/S.

Es mejor no compartir un identificador de archivo asociado a un puerto de finalización de E/S mediante la herencia de identificadores o una llamada a la [**función DuplicateHandle.**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) Las operaciones realizadas con estos identificadores duplicados generan notificaciones de finalización. Se recomienda tener en cuenta detenidamente.

El identificador de puerto de finalización de E/S y cada identificador de archivo asociado a ese puerto de finalización de E/S determinado se conocen como referencias al puerto de finalización *de E/S*. El puerto de finalización de E/S se libera cuando no hay más referencias a él. Por lo tanto, todos estos identificadores deben cerrarse correctamente para liberar el puerto de finalización de E/S y sus recursos del sistema asociados. Una vez que se cumplen estas condiciones, cierre el identificador del puerto de finalización de E/S llamando a la [**función CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)

En Windows 8 y Windows Server 2012, esta función es compatible con las siguientes tecnologías.



| Tecnología                                           | Compatible      |
|------------------------------------------------------|----------------|
| Protocolo bloque de mensajes de servidor (SMB) 3.0<br/>   | Sí<br/> |
| Conmutación por error transparente (TFO) de SMB 3.0<br/>        | Sí<br/> |
| SMB 3.0 con recursos compartidos de archivos de escalabilidad horizontal (SO)<br/>   | Sí<br/> |
| Volumen compartido de clúster de archivos (CsvFS)<br/> | Sí<br/> |
| Sistema de archivos resistente a errores (ReFS)<br/>              | Sí<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones \[ de escritorio XP para aplicaciones para \| UWP\]<br/>                                                                                                                                                                                                                                                       |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2003 \[ \| aplicaciones para UWP\]<br/>                                                                                                                                                                                                                                              |
| Header<br/>                   | <dl> <dt>IoAPI.h (incluir Windows.h);</dt> <dt>WinBase.h en Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP (Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                  |
| Archivo DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                  |



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

[Windows Sockets 2](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

**Funciones**
</dt> <dt>

[**AcceptEx**](/windows/desktop/api/mswsock/nf-mswsock-acceptex)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md)
</dt> <dt>

[**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 


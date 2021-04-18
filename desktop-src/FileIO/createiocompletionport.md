---
description: Crea un puerto de finalización de entrada/salida (e/s) y lo asocia a un identificador de archivo especificado, o crea un puerto de finalización de e/s que todavía no está asociado a un identificador de archivo, lo que permite la asociación en otro momento.
ms.assetid: 40cb47fc-7b15-47f6-bee2-2611d4686053
title: CreateIoCompletionPort (función) (IoAPI. h)
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
ms.openlocfilehash: b85ec931e740de192655ada091a990cd97180b6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687655"
---
# <a name="createiocompletionport-function"></a>CreateIoCompletionPort (función)

Crea un puerto de finalización de entrada/salida (e/s) y lo asocia a un identificador de archivo especificado, o crea un puerto de finalización de e/s que todavía no está asociado a un identificador de archivo, lo que permite la asociación en otro momento.

La Asociación de una instancia de un identificador de archivo abierto con un puerto de finalización de e/s permite que un proceso reciba una notificación de la realización de operaciones de e/s asincrónicas que impliquen ese identificador de archivo.

> [!Note]
>
> El término *identificador de archivo* tal como se usa aquí hace referencia a una abstracción del sistema que representa un punto de conexión de e/s superpuesto, no solo un archivo en disco. Los objetos del sistema que admiten e/s superpuestas como puntos de conexión de red, Sockets TCP, canalizaciones con nombre y ranuras de correo se pueden usar como identificadores de archivo. Para obtener más información, vea la sección Comentarios.

 

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

*FileHandle* \[ de\]
</dt> <dd>

Identificador de archivo abierto o **\_ \_ valor de identificador no válido**.

El identificador debe ser un objeto que admita e/s superpuesta.

Si se proporciona un identificador, debe haberse abierto para la finalización de e/s superpuesta. Por ejemplo, debe especificar la marca de superposición de **\_ marcador \_ de archivo** al utilizar la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para obtener el identificador.

Si se especifica un **\_ \_ valor de identificador no válido** , la función crea un puerto de finalización de e/s sin asociarlo a un identificador de archivo. En este caso, el parámetro *ExistingCompletionPort* debe ser **null** y se omitirá el parámetro *CompletionKey* .

</dd> <dt>

*ExistingCompletionPort* \[ en, opcional\]
</dt> <dd>

Identificador de un puerto de finalización de e/s existente o **null**.

Si este parámetro especifica un puerto de finalización de e/s existente, la función lo asocia con el identificador especificado por el parámetro *FileHandle* . La función devuelve el identificador del puerto de finalización de e/s existente si se realiza correctamente; no crea un nuevo puerto de finalización de e/s.

Si este parámetro es **null**, la función crea un nuevo puerto de finalización de e/s y, si el parámetro *FileHandle* es válido, lo asocia al nuevo puerto de finalización de e/s. En caso contrario, no se produce ninguna asociación de identificador de archivo. Si se realiza correctamente, la función devuelve el identificador al nuevo puerto de finalización de e/s.

</dd> <dt>

*CompletionKey* \[ de\]
</dt> <dd>

La clave de finalización definida por el usuario por controlador que se incluye en cada paquete de finalización de e/s para el identificador de archivo especificado. Para obtener más información, vea la sección Comentarios.

</dd> <dt>

*NumberOfConcurrentThreads* \[ de\]
</dt> <dd>

Número máximo de subprocesos que el sistema operativo puede permitir para procesar simultáneamente los paquetes de finalización de e/s para el puerto de finalización de e/s. Se omite este parámetro si el parámetro *ExistingCompletionPort* no es **null**.

Si este parámetro es cero, el sistema permite tantos subprocesos que se ejecutan simultáneamente como procesadores en el sistema.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es el identificador de un puerto de finalización de e/s:

-   Si el parámetro *ExistingCompletionPort* era **null**, el valor devuelto es un nuevo identificador.

-   Si el parámetro *ExistingCompletionPort* era un identificador de puerto de finalización de e/s válido, el valor devuelto es el mismo identificador.

-   Si el parámetro *FileHandle* era un identificador válido, ese identificador de archivo se asocia ahora con el puerto de finalización de e/s devuelto.

Si se produce un error en la función, el valor devuelto es **null**. Para obtener información de error extendida, llame a la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Observaciones

Se puede indicar al sistema de e/s que envíe paquetes de notificación de finalización de e/s a los puertos de finalización de e/s, donde se ponen en cola. La función **CreateIoCompletionPort** proporciona esta funcionalidad.

Un puerto de finalización de e/s y su identificador se asocian con el proceso que lo creó y no se pueden compartir entre los procesos. Sin embargo, un único identificador se compartirá entre los subprocesos del mismo proceso.

**CreateIoCompletionPort** se puede usar en tres modos distintos:

-   Cree solo un puerto de finalización de e/s sin asociarlo a un identificador de archivo.
-   Asociar un puerto de finalización de e/s existente con un identificador de archivo.
-   Realice la creación y la asociación en una sola llamada.

Para crear un puerto de finalización de e/s sin asociarlo, establezca el parámetro *FileHandle* en el **valor de \_ identificador \_ no válido**, el parámetro *ExistingCompletionPort* en **null** y el parámetro *CompletionKey* en cero (que se omite en este caso). Establezca el parámetro *NumberOfConcurrentThreads* en el valor de simultaneidad deseado para el nuevo puerto de finalización de e/s, o bien, cero para el valor predeterminado (el número de procesadores del sistema).

El identificador pasado en el parámetro *FileHandle* puede ser cualquier controlador que admita e/s superpuesta. Normalmente, se trata de un identificador abierto por la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) mediante el uso de la marca de **\_ indicador \_ superpuesto de archivo** (por ejemplo, archivos, ranuras de correo y canalizaciones). Los objetos creados por otras funciones como [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) también se pueden asociar a un puerto de finalización de e/s. Para obtener un ejemplo de uso de sockets, consulte [**AcceptEx**](/windows/desktop/api/mswsock/nf-mswsock-acceptex). Un identificador solo se puede asociar a un puerto de finalización de e/s y, una vez realizada la asociación, el identificador permanece asociado a ese puerto de finalización de e/s hasta que se cierra.

Para obtener más información sobre la teoría del puerto de finalización de e/s, el uso y las funciones asociadas, consulte [puertos de finalización de e/s](i-o-completion-ports.md).

Se pueden asociar varios identificadores de archivo a un único puerto de finalización de e/s llamando a **CreateIoCompletionPort** varias veces con el mismo identificador de puerto de finalización de e/s en el parámetro *ExistingCompletionPort* y un identificador de archivo diferente en el parámetro *FileHandle* cada vez.

Use el parámetro *CompletionKey* para ayudar a la aplicación a realizar un seguimiento de las operaciones de e/s que se han completado. **CreateIoCompletionPort** no usa este valor para el control funcional. en su lugar, se adjunta al identificador de archivo especificado en el parámetro *FileHandle* en el momento de la asociación con un puerto de finalización de e/s. Esta clave de finalización debe ser única para cada identificador de archivo y acompañará al identificador de archivo a lo largo del proceso de cola de finalización interna. Se devuelve en la llamada a la función [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) cuando llega un paquete de finalización. La función [**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) también usa el parámetro *CompletionKey* para poner en cola sus propios paquetes de finalización especial.

Una vez que una instancia de un identificador abierto está asociada a un puerto de finalización de e/s, no se puede usar en la función [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) o [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) porque estas funciones tienen sus propios mecanismos de e/s asincrónicos.

Es mejor no compartir un identificador de archivo asociado a un puerto de finalización de e/s mediante el uso de la herencia de identificadores o una llamada a la función [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) . Las operaciones realizadas con estos identificadores duplicados generan notificaciones de finalización. Se recomienda tener cuidado.

El identificador de puerto de finalización de e/s y todos los identificadores de archivo asociados a ese puerto de terminación de e/s concreto se conocen como *referencias al puerto de terminación de e/s*. El puerto de finalización de e/s se libera cuando no hay más referencias a él. Por lo tanto, todos estos identificadores deben estar cerrados correctamente para liberar el puerto de finalización de e/s y sus recursos del sistema asociados. Una vez que se cumplen estas condiciones, cierre el identificador del puerto de finalización de e/s mediante una llamada a la función [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .

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
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows XP \|\]<br/>                                                                                                                                                                                                                                                       |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2003 \|\]<br/>                                                                                                                                                                                                                                              |
| Encabezado<br/>                   | <dl> <dt>IoAPI. h (incluye Windows. h); </dt> <dt>Winbase. h en Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP (incluido Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                  |
| Archivo DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                  |



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

 


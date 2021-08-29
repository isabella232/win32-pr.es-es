---
description: Lee datos de un archivo abierto.
ms.assetid: 7EA2FE38-20DA-43E1-A764-66A81725D1EA
title: Función NtReadFile (Wdm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtReadFile
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 57eacec05ec56fe3b174ee58569adca4c0f644e698aae3b603c7db5ab8f25f57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984175"
---
# <a name="ntreadfile-function"></a>Función NtReadFile

Lee datos de un archivo abierto.

Esta función es el modo de usuario equivalente a la [**función ZwReadFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntreadfile) documentada en Windows Driver Kit (WDK).

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS NtReadFile(
  _In_     HANDLE           FileHandle,
  _In_opt_ HANDLE           Event,
  _In_opt_ PIO_APC_ROUTINE  ApcRoutine,
  _In_opt_ PVOID            ApcContext,
  _Out_    PIO_STATUS_BLOCK IoStatusBlock,
  _Out_    PVOID            Buffer,
  _In_     ULONG            Length,
  _In_opt_ PLARGE_INTEGER   ByteOffset,
  _In_opt_ PULONG           Key
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FileHandle* \[ En\]
</dt> <dd>

Identificador del objeto de archivo. Este identificador se crea mediante una llamada correcta a [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) o [**NtOpenFile.**](/windows/desktop/api/Winternl/nf-winternl-ntopenfile)

</dd> <dt>

*Evento* \[ en, opcional\]
</dt> <dd>

Opcionalmente, un identificador de un objeto de evento para establecer en el estado señalado una vez completada la operación de lectura. Los controladores intermedios y de dispositivo deben establecer este parámetro en **NULL.**

</dd> <dt>

*ApcRoutine* \[ en, opcional\]
</dt> <dd>

Este parámetro está reservado. Los controladores intermedios y de dispositivo deben establecer este puntero en **NULL.**

</dd> <dt>

*ApcContext* \[ en, opcional\]
</dt> <dd>

Este parámetro está reservado. Los controladores intermedios y de dispositivo deben establecer este puntero en **NULL.**

</dd> <dt>

*IoStatusBlock* \[ out\]
</dt> <dd>

Puntero a una [**estructura IO \_ STATUS \_ BLOCK**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_io_status_block) que recibe el estado de finalización final e información sobre la operación de lectura solicitada. El **miembro Information** recibe el número de bytes leídos realmente del archivo.

</dd> <dt>

*Búfer* \[ out\]
</dt> <dd>

Puntero a un búfer asignado por el autor de la llamada que recibe los datos leídos del archivo.

</dd> <dt>

*Longitud* \[ En\]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *buffer*.

</dd> <dt>

*ByteOffset* \[ en, opcional\]
</dt> <dd>

Puntero a una variable que especifica el desplazamiento de bytes inicial en el archivo donde se iniciará la operación de lectura. Si se intenta leer más allá del final del archivo, **NtReadFile** devuelve un error.

Si la llamada a [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) establece cualquiera de las marcas *CreateOptions* FILE SYNCHRONOUS IO ALERT o \_ FILE SYNCHRONOUS IO \_ \_ \_ \_ NONALERT, el Administrador de \_ E/S mantiene la posición del archivo actual. Si es así, el autor de la llamada **de NtReadFile** puede especificar que se utilice el desplazamiento de posición del archivo actual en lugar de un *valor ByteOffset* explícito. Esta especificación se puede realizar mediante uno de los métodos siguientes:

-   Especifique un puntero a un valor **LARGE \_ INTEGER** con el miembro **HighPart** establecido en -1 y el **miembro LowPart** establecido en el valor definido por el sistema FILE \_ USE FILE POINTER \_ \_ \_ POSITION.

-   Pase un **puntero NULL** para *ByteOffset.*

**NtReadFile** actualiza la posición actual del archivo agregando el número de bytes leídos cuando completa la operación de lectura, si usa la posición de archivo actual mantenida por el Administrador de E/S.

Incluso cuando el Administrador de E/S mantiene la posición de archivo actual, el autor de la llamada puede restablecer esta posición pasando un *valor ByteOffset* explícito a **NtReadFile**. Al hacerlo, cambia automáticamente la posición actual del archivo a ese valor *ByteOffset,* realiza la operación de lectura y, a continuación, actualiza la posición según el número de bytes leídos realmente. Esta técnica proporciona al autor de la llamada el servicio de búsqueda y lectura atómico.

</dd> <dt>

*Clave* \[ en, opcional\]
</dt> <dd>

Los controladores intermedios y de dispositivo deben establecer este puntero en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtReadFile devuelve** STATUS \_ SUCCESS o el código de error NTSTATUS adecuado.

## <a name="remarks"></a>Comentarios

Los llamadores **de NtReadFile** ya deben haber llamado [**a NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) con el valor FILE READ DATA o \_ GENERIC READ establecido en el parámetro \_ \_ *DesiredAccess.*

Si la llamada anterior a [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) establece la marca FILE NO INTERMEDIATE BUFFERING del parámetro \_ \_ \_ *CreateOptions* en **NtCreateFile,**  los parámetros Length y *ByteOffset* en **NtReadFile** deben ser múltiplo del tamaño del sector. Para obtener más información, **vea NtCreateFile**.

**NtReadFile comienza** a leer desde el *byteOffset dado* o la posición del archivo actual en el búfer *dado.* Finaliza la operación de lectura en una de las siguientes condiciones:

-   El búfer está lleno porque se ha leído el número de bytes especificado por el parámetro *Length.* Por lo tanto, no se pueden colocar más datos en el búfer sin desbordamiento.

-   Se alcanza el final del archivo durante la operación de lectura, por lo que no hay más datos en el archivo que se transferirán al búfer.

Si el autor de la llamada abrió el archivo con la marca SYNCHRONIZE establecida en *DesiredAccess*, el subproceso de llamada puede sincronizarse con la finalización de la operación de lectura esperando en el identificador de archivo, *FileHandle*. El identificador se señala cada vez que se completa una operación de E/S que se emitió en el identificador. Sin embargo, el autor de la llamada no debe esperar en un identificador que se abrió para el acceso sincrónico a archivos (FILE \_ SYNCHRONOUS \_ IO NONALERT o FILE SYNCHRONOUS IO \_ \_ \_ \_ ALERT). En este caso, **NtReadFile** espera en nombre del autor de la llamada y no vuelve hasta que se completa la operación de lectura. El autor de la llamada puede esperar de forma segura en el identificador de archivo solo si se cumplen las tres condiciones siguientes:

-   El identificador se abrió para el acceso asincrónico (es decir, no se especificó ninguna marca FILE \_ SYNCHRONOUS \_ IO \_ *XXX).*

-   El identificador solo se usa para una operación de E/S a la vez.

-   **NtReadFile devolvió** STATUS \_ PENDING.

Un controlador debe llamar **a NtReadFile** en el contexto del proceso del sistema si existe alguna de las condiciones siguientes:

-   El controlador creó el identificador de archivo que pasa **a NtReadFile.**

-   **NtReadFile** notificará al controlador la finalización de E/S mediante un evento creado por el controlador.

-   **NtReadFile notificará** al controlador la finalización de E/S mediante una rutina de devolución de llamada de APC que el controlador pasa a **NtReadFile**.

Los identificadores de archivos y eventos solo son válidos en el contexto de proceso donde se crean los identificadores. Por lo tanto, para evitar problemas de seguridad, el controlador debe crear cualquier identificador de archivo o evento que pase a **NtReadFile** en el contexto del proceso del sistema en lugar del contexto del proceso en el que se encuentra el controlador.

Del mismo modo, se debe llamar a **NtReadFile** en el contexto del proceso del sistema si notifica al controlador la finalización de E/S mediante un APC, ya que las API siempre se desencadenan en el contexto del subproceso que emite la solicitud de E/S. Si el controlador llama a **NtReadFile** en el contexto de un proceso que no sea el del sistema, el APC podría retrasarse indefinidamente o podría no desenlazárselo en absoluto.

Para obtener más información sobre cómo trabajar con archivos, vea [Using Files in a Driver](/windows-hardware/drivers/kernel/using-files-in-a-driver).

Los llamadores **de NtReadFile** deben ejecutarse en IRQL = NIVEL PASIVO y con \_ las API de kernel especiales [habilitadas.](/windows-hardware/drivers/kernel/disabling-apcs)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                    |
| Plataforma de destino<br/>          | <dl> <dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Header<br/>                   | <dl> <dt>Wdm.h (incluya Wdm.h, Ntddk.h o Ntifs.h)</dt> </dl>                   |
| Biblioteca<br/>                  | <dl> <dt>Ntdll.lib</dt> </dl>                                                    |
| Archivo DLL<br/>                      | <dl> <dt>Ntdll.dll (modo de usuario)</dt> </dl>                                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**KeInitializeEvent**](/windows-hardware/drivers/ddi/wdm/nf-wdm-keinitializeevent)
</dt> <dt>

[**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile)
</dt> <dt>

[**NtQueryInformationFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntqueryinformationfile)
</dt> <dt>

[**NtSetInformationFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntsetinformationfile)
</dt> <dt>

[**NtWriteFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntwritefile)
</dt> </dl>

 

 

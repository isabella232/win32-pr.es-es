---
description: Lee datos de un archivo abierto.
ms.assetid: 7EA2FE38-20DA-43E1-A764-66A81725D1EA
title: Función NtReadFile (WDM. h)
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
ms.openlocfilehash: be1a73c6451012dfd97d7d4c55c23f0842cf1551
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538535"
---
# <a name="ntreadfile-function"></a>NtReadFile función)

Lee datos de un archivo abierto.

Esta función es el modo de usuario equivalente a la función [**ZwReadFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntreadfile) documentada en el kit de controladores de Windows (WDK).

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

*FileHandle* \[ de\]
</dt> <dd>

Identificador del objeto de archivo. Este identificador se crea mediante una llamada correcta a [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) o [**NtOpenFile**](/windows/desktop/api/Winternl/nf-winternl-ntopenfile).

</dd> <dt>

*Evento* \[ de en, opcional\]
</dt> <dd>

Opcionalmente, identificador de un objeto de evento que se va a establecer en el estado señalado una vez finalizada la operación de lectura. Los controladores intermedios y de dispositivo deben establecer este parámetro en **null**.

</dd> <dt>

*ApcRoutine* \[ en, opcional\]
</dt> <dd>

Este parámetro está reservado. Los controladores intermedios y de dispositivo deben establecer este puntero en **null**.

</dd> <dt>

*ApcContext* \[ en, opcional\]
</dt> <dd>

Este parámetro está reservado. Los controladores intermedios y de dispositivo deben establecer este puntero en **null**.

</dd> <dt>

*IoStatusBlock* \[ enuncia\]
</dt> <dd>

Puntero a una estructura de [**\_ \_ bloque de estado de e/s**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_io_status_block) que recibe el estado final de finalización e información sobre la operación de lectura solicitada. El miembro de **información** recibe el número de bytes realmente leídos del archivo.

</dd> <dt>

*Búfer* \[ de enuncia\]
</dt> <dd>

Puntero a un búfer asignado por el llamador que recibe los datos leídos del archivo.

</dd> <dt>

*Longitud* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta el *búfer*.

</dd> <dt>

*Byteoffset (* \[ en, opcional\]
</dt> <dd>

Puntero a una variable que especifica el desplazamiento de bytes de inicio en el archivo donde comenzará la operación de lectura. Si se intenta leer más allá del final del archivo, **NtReadFile** devuelve un error.

Si la llamada a [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) establece una de las alertas de e/s sincrónicas sincrónicas del archivo de marcas de *CreateOptions* o del archivo \_ \_ \_ \_ \_ \_ , el administrador de e/s mantiene la posición actual del archivo. Si es así, el llamador de **NtReadFile** puede especificar que se use el desplazamiento de la posición del archivo actual en lugar de un valor *byteoffset (* explícito. Esta especificación puede realizarse mediante uno de los métodos siguientes:

-   Especifique un puntero a un **valor \_ entero grande** con el miembro **HighPart** establecido en-1 y el miembro **LowPart** establecido en el archivo de valor definido por el sistema \_ use la posición del puntero de \_ archivo \_ \_ .

-   Pase un puntero **nulo** para *byteoffset (*.

**NtReadFile** actualiza la posición del archivo actual agregando el número de bytes leídos cuando finaliza la operación de lectura, si usa la posición de archivo actual que mantiene el administrador de e/s.

Incluso cuando el administrador de e/s mantiene la posición actual del archivo, el autor de la llamada puede restablecer esta posición pasando un valor de *byteoffset (* explícito a **NtReadFile**. Al hacerlo, se cambia automáticamente la posición del archivo actual a ese valor *byteoffset (* , se realiza la operación de lectura y, a continuación, se actualiza la posición según el número de bytes leídos realmente. Esta técnica proporciona el servicio de búsqueda y lectura atómica del llamador.

</dd> <dt>

*Clave* \[ de en, opcional\]
</dt> <dd>

Los controladores intermedios y de dispositivo deben establecer este puntero en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtReadFile** devuelve un estado \_ correcto o el código de error NTSTATUS adecuado.

## <a name="remarks"></a>Observaciones

Los autores de llamadas de **NtReadFile** deben haber llamado ya a [**NTCREATEFILE**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) con el archivo \_ Read \_ Data o Generic \_ Read Value establecido en el parámetro *DesiredAccess* .

Si la llamada anterior a [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) establece el \_ indicador archivo \_ sin \_ almacenamiento en búfer intermedio en el parámetro *CreateOptions* en **NtCreateFile**, los parámetros *length* y *byteoffset (* de **NtReadFile** deben ser múltiplos del tamaño del sector. Para obtener más información, vea **NtCreateFile**.

**NtReadFile** comienza a leer desde el *byteoffset (* determinado o la posición del archivo actual en el *búfer* especificado. Finaliza la operación de lectura en una de las siguientes condiciones:

-   El búfer está lleno porque se ha leído el número de bytes especificado por el parámetro de *longitud* . Por lo tanto, no se pueden colocar más datos en el búfer sin desbordamiento.

-   Se alcanza el final del archivo durante la operación de lectura, por lo que no hay más datos en el archivo que se van a transferir al búfer.

Si el autor de la llamada abrió el archivo con la marca SYNCHRONIZE establecida en *DesiredAccess*, el subproceso que realiza la llamada puede sincronizarse con la finalización de la operación de lectura esperando en el identificador de archivo, *FileHandle*. El identificador se señaliza cada vez que se completa una operación de e/s que se emitió en el identificador. Sin embargo, el autor de la llamada no debe esperar en un identificador que se abrió para el acceso a archivos sincrónicos (la alerta de e/s sincrónica de archivo y de e/s sincrónica de archivo \_ \_ \_ \_ \_ \_ ). En este caso, **NtReadFile** espera en nombre del autor de la llamada y no devuelve ningún resultado hasta que se completa la operación de lectura. El autor de la llamada puede esperar en el identificador de archivo sin ningún riesgo si se cumplen las tres condiciones siguientes:

-   El identificador se abrió para el acceso asincrónico (es decir, \_ \_ \_  no se especificó ninguna marca de e/s sincrónica de archivo).

-   El identificador se usa solo para una operación de e/s a la vez.

-   **NtReadFile** devolvió el estado \_ pendiente.

Un controlador debe llamar a **NtReadFile** en el contexto del proceso del sistema si se cumple alguna de las condiciones siguientes:

-   El controlador creó el identificador de archivo que pasa a **NtReadFile**.

-   **NtReadFile** notificará al controlador la finalización de e/s por medio de un evento creado por el controlador.

-   **NtReadFile** notificará al controlador de finalización de e/s por medio de una rutina de devolución de llamada APC que el controlador pasa a **NtReadFile**.

Los identificadores de archivo y de evento solo son válidos en el contexto del proceso en el que se crean los identificadores. Por lo tanto, para evitar brechas de seguridad, el controlador debe crear cualquier archivo o controlador de eventos que pase a **NtReadFile** en el contexto del proceso del sistema, en lugar del contexto del proceso en el que se encuentra el controlador.

Del mismo modo, se debe llamar a **NtReadFile** en el contexto del proceso del sistema si notifica al controlador de finalización de e/s por medio de una APC, ya que APC se activa siempre en el contexto del subproceso que emite la solicitud de e/s. Si el controlador llama a **NtReadFile** en el contexto de un proceso que no es el del sistema, el APC podría retrasarse indefinidamente, o podría no activarse en absoluto.

Para obtener más información sobre cómo trabajar con archivos, vea [usar archivos en un controlador](/windows-hardware/drivers/kernel/using-files-in-a-driver).

Los autores de llamadas de **NtReadFile** deben ejecutarse en IRQL = \_ nivel pasivo y con el [APC de kernel especial habilitado](/windows-hardware/drivers/kernel/disabling-apcs).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                    |
| Plataforma de destino<br/>          | <dl> <dt>[Mundo](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Encabezado<br/>                   | <dl> <dt>WDM. h (incluir WDM. h, Ntddk. h o Ntifs. h)</dt> </dl>                   |
| Biblioteca<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl>                                                    |
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

 

 

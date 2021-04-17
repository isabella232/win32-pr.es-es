---
description: Recupera los niveles actuales de luz de corte de CA y DC y el estado de energía actual.
ms.assetid: c7b7c302-6e92-46a7-b9a6-e3f2a3e44d1b
title: Código de control de IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS (Ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: 547501a28492aecfe06f63f95b0e007fc80d3d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677900"
---
# <a name="ioctl_video_query_display_brightness-control-code"></a>\_Consulta de vídeo ioctl \_ \_ Mostrar código de control de \_ brillo

\[Este código de control está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. La compatibilidad con este código de control se ha quitado en Windows Server 2008 y Windows Vista. En su lugar, use la clase [**WmiMonitorBrightness**](/windows/desktop/WmiCoreProv/wmimonitorbrightness) .\]

Recupera los niveles actuales de luz de corte de CA y DC y el estado de energía actual.

Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS,  // dwIoControlCode
  NULL,                            // lpInBuffer
  0,                               // nInBufferSize
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador de \\ \\ . \\ Dispositivo LCD. Para recuperar un identificador de dispositivo, llame a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Código de control de la operación. Este valor identifica la operación específica que se va a realizar y el tipo de dispositivo en el que se va a realizar. Use **ioctl \_ video \_ query \_ Display \_ Brightness** para esta operación.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

No se utiliza con esta operación; se establece en **null**.

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

No se utiliza con esta operación; se establece en cero.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Un puntero a un búfer que recibirá una estructura de [**\_ brillo**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) de la pantalla.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Tamaño del búfer de salida, en bytes.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Puntero a una variable que recibe el tamaño, en bytes, de los datos de salida devueltos.

Si el búfer de salida es demasiado pequeño para devolver datos, se produce un error en la llamada, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el error de código \_ insuficiente \_ búfer y el recuento de bytes devuelto es cero.

Si el búfer de salida es demasiado pequeño para contener todos los datos, pero puede contener algunas entradas, el sistema operativo devuelve tanto como cabe en la llamada, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el error del código de error \_ más \_ datos y *lpBytesReturned* indica la cantidad de datos devueltos. La aplicación debe volver a llamar a [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con la misma operación, especificando un nuevo punto de partida.

Si *lpOverlapped* es **null** (Nonoverlapped de e/s), *lpBytesReturned* no puede ser **null**.

Si *lpOverlapped* no es **null** (e/s superpuesta), *lpBytesReturned* puede ser **null**. Si se trata de una operación superpuesta, puede recuperar el número de bytes devueltos mediante una llamada a la función [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) . Si *hDevice* está asociado a un puerto de finalización de e/s, puede obtener el número de bytes devueltos mediante una llamada a la función [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Puntero a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

Si *hDevice* se abrió con la marca de indicador de archivo \_ \_ superpuesto, *lpOverlapped* debe apuntar a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida. En este caso, la operación se realiza como una operación superpuesta (asincrónica). Si el dispositivo se ha abierto con la \_ marca de indicador de archivo \_ superpuesto y *lpOverlapped* es **null**, la función genera un error de manera imprevisible.

Si se abrió *hDevice* sin especificar la marca de la marca de archivo \_ \_ superpuesta, se omite *lpOverlapped* y [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) no devuelve ningún resultado hasta que se haya completado la operación o hasta que se produzca un error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se completa correctamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.

Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

El archivo de encabezado utilizado para compilar aplicaciones que incluyen esta funcionalidad, Ntddvdeo. h, se incluye en el kit de desarrollo de controladores (DDK) de Microsoft Windows. Para obtener información sobre cómo obtener el DDK, vea [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .

Como alternativa, puede definir este código de control como se indica a continuación:

``` syntax
#define IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x126, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP1 \[\]<br/>                                  |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP2<br/>                                                        |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003 R2<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Ntddvdeo. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaz de control de retroiluminación](backlight-control-interface.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**brillo de la pantalla \_**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))
</dt> <dt>

[**brillo de la pantalla del conjunto de \_ vídeos de ioctl \_ \_ \_**](ioctl-video-set-display-brightness.md)
</dt> </dl>

 


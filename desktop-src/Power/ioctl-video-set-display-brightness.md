---
description: Establece los niveles de retroiluminación de AC y DC actuales.
ms.assetid: baa77811-046d-4a07-b3df-2a31fba2d9a7
title: Código de control de IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS (Ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: a0c679f352012eea66b80335bc3ad1547501dd92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001956"
---
# <a name="ioctl_video_set_display_brightness-control-code"></a>Juego de vídeo de IOCTL \_ \_ \_ Mostrar \_ código de control de brillo

Establece los niveles de retroiluminación de AC y DC actuales.

Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS, // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of the input buffer
  NULL,                        // lpOutBuffer
  0,                           // nOutBufferSize 
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
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

Código de control de la operación. Este valor identifica la operación específica que se va a realizar y el tipo de dispositivo en el que se va a realizar. Use el brillo de la pantalla del conjunto de vídeos de ioctl para esta operación. **\_ \_ \_ \_**

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Puntero a una estructura [**de \_ brillo**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) de la pantalla.

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Tamaño del búfer al que apunta *lpOutBuffer*, en bytes.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

No se utiliza con esta operación; se establece en **null**.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

No se utiliza con esta operación; se establece en cero.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Puntero a una variable que recibe el recuento real de bytes devueltos por la función en el búfer de salida.

Si *lpOverlapped* es **null** (Nonoverlapped de e/s), *lpBytesReturned* se usa internamente y no puede ser **null**.

Si *lpOverlapped* no es **null** (e/s superpuesta), *lpBytesReturned* puede ser **null**.

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

Los valores especificados en los miembros **ucACBrightness** y **ucDCBrightness** de la estructura de [**\_ brillo**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) de la pantalla deben haber sido devueltos previamente por el [**\_ \_ \_ \_ brillo compatible con la consulta de vídeo ioctl**](ioctl-video-query-supported-brightness.md). Por ejemplo, si los valores admitidos son 10, 20, 30, 40, 50, 60, 70, 80, 90 y 100, el uso de un valor de 33 sería un error.

El archivo de encabezado utilizado para compilar aplicaciones que incluyen esta funcionalidad, Ntddvdeo. h, se incluye en el kit de desarrollo de controladores (DDK) de Microsoft Windows. Para obtener información sobre cómo obtener el DDK, vea [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .

Como alternativa, puede definir este código de control como se indica a continuación:

``` syntax
#define IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x127, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP con SP1 \[ solo aplicaciones de escritorio\]<br/>                   |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Ntddvdeo. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaz de control de retroiluminación](backlight-control-interface.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**brillo de la pantalla \_**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))
</dt> <dt>

[**\_brillo de \_ visualización de consulta de vídeo ioctl \_ \_**](ioctl-video-query-display-brightness.md)
</dt> <dt>

[**\_ \_ \_ brillo compatible con consulta de vídeo ioctl \_**](ioctl-video-query-supported-brightness.md)
</dt> </dl>

 


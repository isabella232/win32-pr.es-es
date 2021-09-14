---
description: Establece los niveles actuales de retroiluminación de CA y controlador de dominio.
ms.assetid: baa77811-046d-4a07-b3df-2a31fba2d9a7
title: IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS código de control (Ntddvdeo.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062852"
---
# <a name="ioctl_video_set_display_brightness-control-code"></a>Código de control DISPLAY BRIGHTNESS del CONJUNTO DE \_ \_ VÍDEO \_ \_ DE IOCTL

Establece los niveles actuales de retroiluminación de CA y controlador de dominio.

Para realizar esta operación, llame a la [**función DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.


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

Identificador de \\ \\ . \\ Dispositivo USB. Para recuperar un identificador de dispositivo, llame a la [**función CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Código de control de la operación. Este valor identifica la operación específica que se va a realizar y el tipo de dispositivo en el que se va a realizar. Use **IOCTL \_ VIDEO SET DISPLAY BRIGHTNESS \_ \_ \_ para** esta operación.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Puntero a una [**estructura DISPLAY \_ BRIGHTNESS.**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Tamaño del búfer al que apunta *lpOutBuffer*, en bytes.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

No se usa con esta operación; se establece en **NULL.**

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

No se usa con esta operación; se establece en cero.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Puntero a una variable que recibe el recuento real de bytes devueltos por la función en el búfer de salida.

Si *lpOverlapped* es **NULL** (E/S nooverlapped), *lpBytesReturned* se usa internamente y no puede ser **NULL.**

Si *lpOverlapped no* es **NULL** (E/S superpuesta), *lpBytesReturned* puede ser **NULL.**

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Puntero a una [**estructura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

Si *hDevice se* abrió con la marca \_ FILE FLAG \_ OVERLAPPED, *lpOverlapped* debe apuntar a una estructura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida. En este caso, la operación se realiza como una operación superpuesta (asincrónica). Si el dispositivo se abrió con la marca FILE FLAG OVERLAPPED y lpOverlapped es NULL, la función produce un error \_ \_ de manera imprevisible.  

Si *hDevice* se abrió sin especificar la marca \_ FILE FLAG \_ OVERLAPPED, *lpOverlapped* se omite y [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) no vuelve hasta que se ha completado la operación o hasta que se produce un error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se completa correctamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.

Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

Los valores especificados en los miembros **ucACBrightness** y **ucDCBrightness** de la estructura [**DISPLAY \_ BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) deben haber sido devueltos previamente por [**IOCTL \_ VIDEO QUERY \_ \_ SUPPORTED \_ BRIGHTNESS**](ioctl-video-query-supported-brightness.md). Por ejemplo, si los valores admitidos son 10, 20, 30, 40, 50, 60, 70, 80, 90 y 100, el uso de un valor de 33 sería un error.

El archivo de encabezado que se usa para compilar aplicaciones que incluyen esta funcionalidad, Ntddvdeo.h, se incluye en microsoft Windows Driver Development Kit (DDK). Para obtener información sobre cómo obtener el DDK, consulte [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .

Como alternativa, puede definir este código de control de la siguiente manera:

``` syntax
#define IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x127, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio sp1 \[\]<br/>                   |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Ntddvdeo.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Interfaz de control de retroiluminación](backlight-control-interface.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**BRILLO DE \_ LA PANTALLA**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))
</dt> <dt>

[**BRILLO DE VISUALIZACIÓN \_ DE LA CONSULTA DE VÍDEO \_ \_ DE \_ IOCTL**](ioctl-video-query-display-brightness.md)
</dt> <dt>

[**BRILLO COMPATIBLE \_ CON LA CONSULTA DE VÍDEO \_ \_ DE \_ IOCTL**](ioctl-video-query-supported-brightness.md)
</dt> </dl>

 


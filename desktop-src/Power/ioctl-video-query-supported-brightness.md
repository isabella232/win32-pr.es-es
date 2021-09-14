---
description: Recupera los niveles de retroiluminación admitidos.
ms.assetid: b4c1ee3f-af75-477e-b7ed-53be905374d7
title: IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS código de control (Ntddvdeo.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: a5618ec29fd47ba690106b5f826e6fb145eac208
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062853"
---
# <a name="ioctl_video_query_supported_brightness-control-code"></a>Código de control DE BRILLO COMPATIBLE CON LA CONSULTA DE VÍDEO \_ \_ \_ \_ DE IOCTL

Recupera los niveles de retroiluminación admitidos.

Para realizar esta operación, llame a la [**función DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS,  // dwIoControlCode
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

Identificador de \\ \\ . \\ Dispositivo USB. Para recuperar un identificador de dispositivo, llame a la [**función CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Código de control de la operación. Este valor identifica la operación específica que se va a realizar y el tipo de dispositivo en el que se va a realizar. Use **EL BRILLO ADMITIDO DE LA CONSULTA DE VÍDEO \_ \_ \_ \_ DE IOCTL** para esta operación.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

No se usa con esta operación; se establece en **NULL.**

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

No se usa con esta operación; se establece en cero.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Puntero a un búfer que recibe una matriz de los niveles de energía disponibles. Este búfer debe tener una longitud de 256 bytes.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Tamaño del búfer de salida, en bytes.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Puntero a una variable que recibe el tamaño, en bytes, de los datos de salida devueltos.

Si el búfer de salida es demasiado pequeño para devolver datos, se produce un error en la llamada, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el código de error ERROR INSUFFICIENT BUFFER y el recuento de bytes devuelto \_ \_ es cero.

Si el búfer de salida es demasiado pequeño para contener todos los datos, pero puede contener algunas entradas, el sistema operativo devuelve lo que cabe, se produce un error en la llamada, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el código de error ERROR MORE DATA y \_ \_ *lpBytesReturned* indica la cantidad de datos devueltos. La aplicación debe llamar de nuevo a [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con la misma operación, especificando un nuevo punto de partida.

Si *lpOverlapped* es **NULL** (E/S nooverlapped), *lpBytesReturned* no puede ser **NULL.**

Si *lpOverlapped no* es **NULL** (E/S superpuesta), *lpBytesReturned* puede ser **NULL.** Si se trata de una operación superpuesta, puede recuperar el número de bytes devueltos llamando a la [**función GetOverlappedResult.**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) Si *hDevice* está asociado a un puerto de finalización de E/S, puede obtener el número de bytes devueltos llamando a la función [**GetQueuedCompletionStatus.**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

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

Cada elemento de la matriz *lpOutBuffer* tiene una longitud de un byte. Por lo tanto, al devolverse, el parámetro *lpBytesReturned* indica el número de niveles admitidos. Cada nivel es un valor de 0 a 100. Cuanto mayor sea el valor, más brillante será la luz de fondo. Se admiten todos los niveles, independientemente de si la fuente de alimentación es AC o DC.

El archivo de encabezado que se usa para compilar aplicaciones que incluyen esta funcionalidad, Ntddvdeo.h, se incluye en microsoft Windows Driver Development Kit (DDK). Para obtener información sobre cómo obtener el DDK, consulte [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .

Como alternativa, puede definir este código de control de la siguiente manera:

``` syntax
#define IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x125, METHOD_BUFFERED, FILE_ANY_ACCESS)
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
</dt> </dl>

 


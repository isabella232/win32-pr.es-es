---
title: Comando MCI_RESERVE (mmsystem. h)
description: El \_ comando reserva de MCI asigna espacio en disco contiguo para el área de trabajo de la instancia de controlador de dispositivo para su uso con grabaciones posteriores. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 01f0a377-0179-4b05-a642-af152a7a12ae
keywords:
- Comando de MCI_RESERVE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_RESERVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b89eb457b63012aa9ee5624efef95945258d42c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996858"
---
# <a name="mci_reserve-command"></a>\_Comando reserva de MCI

El \_ comando reserva de MCI asigna espacio en disco contiguo para el área de trabajo de la instancia de controlador de dispositivo para su uso con grabaciones posteriores. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESERVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESERVE_PARMS) lpReserve
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI. Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*lpReserve*
</dt> <dd>

Puntero a una estructura de [**parms de DGV de MCI \_ \_ reservada \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Si el área de trabajo contiene datos no guardados, estos datos se perderán. Si no se reserva espacio en disco antes de la grabación, el comando [MCI \_ Record](mci-record.md) realiza una reserva implícita con parámetros predeterminados específicos del dispositivo. En algunas implementaciones, no es necesario reservar y el controlador del dispositivo puede omitirla. El espacio de reserva explícita proporciona un mejor control sobre cuándo se produce el retraso de la asignación de disco, cuánto espacio se asigna y dónde se asigna el espacio en disco. La cantidad y la ubicación del espacio en disco que ya está reservada para esta instancia de dispositivo se pueden cambiar emitiendo la reserva de MCI de \_ nuevo. Cualquier espacio en disco asignado y todavía sin usar no se cancela hasta que se guardan los datos grabados o hasta que se cierra la instancia del controlador de dispositivo.

Si el vídeo está desactivado con la \_ marca MCI OFF del comando [MCI \_ SETVIDEO](mci-setvideo.md) , el espacio reservado no incluye ningún vídeo. Si el audio está desactivado con la \_ marca MCI OFF del comando [MCI \_ SETAUDIO](mci-setaudio.md) , el espacio reservado no incluye audio. Si el audio y el vídeo están desactivados o si el tamaño solicitado es cero, no se reserva ningún espacio y se cancela la asignación de cualquier espacio reservado existente.

Las siguientes marcas adicionales se aplican a los dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>\_ \_ reserva de MCI DGV \_ en
</dt> <dd>

El miembro **lpstrPath** de la estructura identificada por *lpReserve* contiene una dirección de un búfer que contiene la ubicación de un archivo temporal. El búfer contiene solo la unidad y la ruta de acceso al directorio del archivo utilizado para almacenar los datos registrados; el nombre de archivo lo especifica el controlador del dispositivo. Este archivo temporal se elimina cuando se cierra la instancia del dispositivo a menos que se guarde explícitamente. Si se omite esta marca, el controlador de dispositivo especifica dónde se asigna espacio en disco.

</dd> <dt>

<span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>tamaño de reserva de MCI \_ DGV \_ \_
</dt> <dd>

El miembro **dwSize** de la estructura identificada por *lpReserve* especifica la cantidad aproximada de espacio en disco que se va a reservar en el área de trabajo para la grabación. El valor se especifica en el formato de hora actual. La cantidad de espacio en disco se calcula a partir de la hora solicitada y desde la que el formato de archivo y el algoritmo de audio y vídeo y los valores de calidad están en vigor. Si se omite esta marca, el controlador de dispositivo podría usar un valor predeterminado que defina.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Comandos MCI](mci-commands.md)
</dt> </dl>

 


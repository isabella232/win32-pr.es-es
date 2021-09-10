---
title: MCI_RESERVE comando (Mmsystem.h)
description: El comando MCI RESERVE asigna espacio en disco contiguo para el área de trabajo de la instancia del controlador de dispositivo \_ para su uso con la grabación posterior. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 01f0a377-0179-4b05-a642-af152a7a12ae
keywords:
- MCI_RESERVE comando Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370057"
---
# <a name="mci_reserve-command"></a>Comando MCI \_ RESERVE

El comando MCI RESERVE asigna espacio en disco contiguo para el área de trabajo de la instancia del controlador de dispositivo \_ para su uso con la grabación posterior. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT o MCI \_ TEST. Para obtener información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*lpReserve*
</dt> <dd>

Puntero a una [**estructura \_ MCI DGV \_ RESERVE \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Si el área de trabajo contiene datos no guardados, estos datos se pierden. Si el espacio en disco no está reservado antes de la grabación, el comando RECORD de [MCI \_ ](mci-record.md) realiza una reserva implícita con parámetros predeterminados específicos del dispositivo. En algunas implementaciones, la reserva no es necesaria y el controlador del dispositivo podría omitirla. Reservar espacio explícitamente proporciona un mejor control sobre cuándo se produce el retraso para la asignación de disco, cuánto espacio se asigna y dónde se asigna el espacio en disco. La cantidad y la ubicación del espacio en disco ya reservado para esta instancia de dispositivo se pueden cambiar mediante la emisión de MCI \_ RESERVE de nuevo. Cualquier espacio en disco asignado y aún sin usar no se desasigna hasta que se guarden los datos registrados o hasta que se cierre la instancia del controlador de dispositivo.

Si el vídeo está desactivado con la marca MCI OFF del comando \_ [MCI \_ SETVIDEO,](mci-setvideo.md) el espacio reservado no incluye ningún vídeo. Si el audio está desactivado con la marca MCI OFF del comando \_ [ \_ SETAUDIO de MCI,](mci-setaudio.md) el espacio reservado no incluye ningún audio. Si el audio y el vídeo están desactivados o si el tamaño solicitado es cero, no se reserva ningún espacio y se desasigna cualquier espacio reservado existente.

Las siguientes marcas adicionales se aplican a los dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>RESERVA \_ DE MCI DGV \_ \_ EN
</dt> <dd>

El **miembro lpstrPath** de la estructura identificada por *lpReserve* contiene una dirección de un búfer que contiene la ubicación de un archivo temporal. El búfer contiene solo la ruta de acceso de la unidad y el directorio del archivo utilizado para contener los datos registrados; el controlador de dispositivo especifica el nombre de archivo. Este archivo temporal se elimina cuando se cierra la instancia del dispositivo a menos que se guarde explícitamente. Si se omite esta marca, el controlador de dispositivo especifica dónde se asigna espacio en disco.

</dd> <dt>

<span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>TAMAÑO DE RESERVA \_ DE MCI DGV \_ \_
</dt> <dd>

El **miembro dwSize** de la estructura identificada por *lpReserve* especifica la cantidad aproximada de espacio en disco que se reserva en el área de trabajo para la grabación. El valor se especifica en el formato de hora actual. La cantidad de espacio en disco se calcula a partir del tiempo solicitado y de qué formato de archivo y algoritmo de audio y vídeo y valores de calidad están en vigor. Si se omite esta marca, el controlador de dispositivo podría usar un valor predeterminado que defina.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Comandos de MCI](mci-commands.md)
</dt> </dl>

 


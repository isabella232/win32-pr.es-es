---
title: MCI_SAVE comando (Mmsystem.h)
description: El comando SAVE de MCI \_ guarda el archivo actual.
ms.assetid: 286e6f31-cb93-443b-8191-8c363b366eae
keywords:
- MCI_SAVE comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SAVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a241c0379731e870940cd676c33ae192efc5d297
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473879"
---
# <a name="mci_save-command"></a>Comando SAVE de MCI \_

El comando SAVE de MCI \_ guarda el archivo actual. Los dispositivos que modifican archivos no deben destruir la copia original hasta que reciban el mensaje de guardado. Los dispositivos de superposición de vídeo y audio de forma de onda reconocen este comando. Aunque los dispositivos de vídeo digital y los secuenciadores MIDI también reconocen este comando, los controladores MCIAVI y MCISEQ no lo implementan.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SAVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SAVE_PARMS ) lpSave
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

MCI \_ NOTIFY, MCI \_ WAIT o, para dispositivos de vídeo digital y VCR, MCI \_ TEST. Para obtener información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSave"></span><span id="lpsave"></span><span id="LPSAVE"></span>*lpSave*
</dt> <dd>

Puntero a una [**estructura \_ MCI SAVE \_ PARMS.**](mci-save-parms.md) (Los dispositivos con parámetros adicionales pueden reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Este comando es compatible con dispositivos que devuelven **TRUE** cuando se llama al comando [ \_ GETDEVCAPS](mci-getdevcaps.md) de MCI con la marca \_ GETDEVCAPS \_ CAN SAVE de MCI. \_

La siguiente marca adicional se aplica a todos los dispositivos que [admiten MCI \_ SAVE](/windows):

<dl> <dt>

<span id="MCI_SAVE_FILE"></span><span id="mci_save_file"></span>ARCHIVO GUARDADO DE MCI \_ \_
</dt> <dd>

El **miembro lpfilename** de la estructura identificada por *lpSave* contiene una dirección de un búfer que contiene el nombre de archivo de destino.

</dd> </dl>

Las siguientes marcas adicionales se usan con el **tipo de dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI \_ DGV \_ RECT
</dt> <dd>

El **miembro rc** de la estructura identificada por *lpSave* contiene un rectángulo válido. El rectángulo especifica una región del búfer de marco que se guardará en el archivo especificado. El primer par de coordenadas especifica la esquina superior izquierda del rectángulo; el segundo par especifica el ancho y el alto. Los dispositivos de vídeo digital deben usar el [comando MCI \_ CAPTURE](mci-capture.md) para capturar el contenido del búfer de fotogramas. (Los dispositivos de superposición de vídeo también deben usar MCI \_ CAPTURE). Esta marca es para la compatibilidad con el conjunto de comandos existente de superposición de vídeo de MCI.

</dd> <dt>

<span id="MCI_DGV_SAVE_ABORT"></span><span id="mci_dgv_save_abort"></span>MCI \_ DGV \_ SAVE \_ ABORT
</dt> <dd>

Detiene una operación de guardado en curso. Debe ser la única marca presente.

</dd> <dt>

<span id="MCI_DGV_SAVE_KEEPRESERVE"></span><span id="mci_dgv_save_keepreserve"></span>MCI \_ DGV \_ SAVE \_ KEEPRESERVE
</dt> <dd>

No se desasigna el espacio en disco sin usar que se deja desde el [comando original de MCI \_ RESERVE.](mci-reserve.md)

</dd> </dl>

En el caso de los dispositivos de vídeo digital, el *parámetro lpSave* apunta a una estructura [**MCI \_ DGV \_ SAVE \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa)

La siguiente marca adicional se usa con el tipo **de dispositivo de** superposición:

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ RECT
</dt> <dd>

El **miembro rc** de la estructura identificada por *lpSave* contiene un rectángulo de presentación válido que indica el área del búfer de vídeo que se guardará.

</dd> </dl>

En el caso de los dispositivos de superposición de vídeo, el parámetro *lpSave* apunta a una [**estructura MCI \_ OVLY \_ SAVE \_ PARMS.**](/previous-versions//dd743447(v=vs.85))

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

 


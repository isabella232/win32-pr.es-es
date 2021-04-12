---
title: Comando MCI_SAVE (mmsystem. h)
description: El \_ comando MCI Save guarda el archivo actual.
ms.assetid: 286e6f31-cb93-443b-8191-8c363b366eae
keywords:
- Comando de MCI_SAVE de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489586"
---
# <a name="mci_save-command"></a>Comando de guardado de MCI \_

El \_ comando MCI Save guarda el archivo actual. Los dispositivos que modifican archivos no deben destruir la copia original hasta que reciban el mensaje de guardado. Los dispositivos de audio y la superposición de vídeo y de onda reconocen este comando. Aunque los dispositivos de vídeo digital y los secuenciadores MIDI también reconocen este comando, los controladores MCIAVI y MCISEQ no lo implementan.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

MCI \_ Notify, espera de MCI \_ o, para dispositivos de vídeo digital y VCR, prueba de MCI \_ . Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSave"></span><span id="lpsave"></span><span id="LPSAVE"></span>*lpSave*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms de guardado de MCI**](mci-save-parms.md) . (Los dispositivos con parámetros adicionales podrían reemplazar esta estructura con una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Este comando es compatible con los dispositivos que devuelven **true** cuando se llama al comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) con el \_ marcador MCI GETDEVCAPS \_ Can \_ Save.

La marca adicional siguiente se aplica a todos los dispositivos que admiten el [ \_ guardado de MCI](/windows):

<dl> <dt>

<span id="MCI_SAVE_FILE"></span><span id="mci_save_file"></span>\_Guardar \_ archivo MCI
</dt> <dd>

El miembro **lpfilename** de la estructura identificada por *lpSave* contiene una dirección de un búfer que contiene el nombre de archivo de destino.

</dd> </dl>

Con el tipo de dispositivo **DigitalVideo** se usan las siguientes marcas adicionales:

<dl> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV \_ Rect
</dt> <dd>

El miembro **RC** de la estructura identificada por *lpSave* contiene un rectángulo válido. El rectángulo especifica una región del búfer de fotogramas que se guardará en el archivo especificado. El primer par de coordenadas especifica la esquina superior izquierda del rectángulo; el segundo par especifica el ancho y el alto. Los dispositivos de vídeo digital deben usar el comando [MCI \_ Capture](mci-capture.md) para capturar el contenido del búfer de fotogramas. (Los dispositivos de superposición de vídeo también deben usar MCI \_ ) CAPTURE). Esta marca es por compatibilidad con el conjunto de comandos de vídeo superposición de MCI existente.

</dd> <dt>

<span id="MCI_DGV_SAVE_ABORT"></span><span id="mci_dgv_save_abort"></span>\_DGV de \_ almacenamiento de MCI \_
</dt> <dd>

Detiene una operación de guardar en curso. Debe ser la única marca presente.

</dd> <dt>

<span id="MCI_DGV_SAVE_KEEPRESERVE"></span><span id="mci_dgv_save_keepreserve"></span>MCI \_ DGV \_ Save \_ KEEPRESERVE
</dt> <dd>

No se cancela la asignación del espacio en disco que queda sin usar desde el comando de [ \_ reserva de MCI](mci-reserve.md) original.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, el parámetro *lpSave* apunta a una estructura [**MCI \_ DGV \_ Save \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa) .

La siguiente marca adicional se usa con el tipo de dispositivo **superpuesto** :

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY \_ Rect
</dt> <dd>

El miembro **RC** de la estructura identificada por *lpSave* contiene un rectángulo de presentación válido que indica el área del búfer de vídeo que se va a guardar.

</dd> </dl>

En el caso de los dispositivos de superposición de vídeo, el parámetro *lpSave* apunta a una estructura [**MCI \_ OVLY \_ Save \_ parms**](/previous-versions//dd743447(v=vs.85)) .

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

 


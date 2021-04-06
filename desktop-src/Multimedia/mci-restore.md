---
title: Comando MCI_RESTORE (mmsystem. h)
description: El \_ comando MCI restore copia un mapa de bits de un archivo en el búfer de fotogramas. Los dispositivos de vídeo digital reconocen este comando. Este comando realiza la acción opuesta del comando MCI \_ Capture.
ms.assetid: ed309cc6-72a3-4abb-aef2-40a55381d8b6
keywords:
- Comando de MCI_RESTORE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_RESTORE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b0c82db597a0e347f382c7cda55ce507f4e6dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803259"
---
# <a name="mci_restore-command"></a>Comando de restauración de MCI \_

El \_ comando MCI restore copia un mapa de bits de un archivo en el búfer de fotogramas. Los dispositivos de vídeo digital reconocen este comando. Este comando realiza la acción opuesta del comando [MCI \_ Capture](mci-capture.md) .

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESTORE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESTORE_PARMS) lpRestore
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

<span id="lpRestore"></span><span id="lprestore"></span><span id="LPRESTORE"></span>*lpRestore*
</dt> <dd>

Puntero a una estructura [**MCI \_ DGV \_ restore \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

La implementación puede reconocer varios formatos de imagen, pero siempre se acepta un mapa de bits independiente del dispositivo (DIB) de Windows.

Las siguientes marcas adicionales se aplican a los dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_RESTORE_FROM"></span><span id="mci_dgv_restore_from"></span>\_ \_ restauración de DGV \_ de MCI desde
</dt> <dd>

El miembro **lpstrFileName** de la estructura identificada por *lpRestore* contiene una dirección de un búfer que contiene el nombre de archivo de origen. El nombre de archivo es obligatorio.

</dd> <dt>

<span id="MCI_DGV_RESTORE_AT"></span><span id="mci_dgv_restore_at"></span>\_ \_ restauración de MCI DGV \_ en
</dt> <dd>

El miembro **RC** de la estructura identificada por *lpRestore* contiene un rectángulo válido. El rectángulo especifica una región del búfer de fotogramas relativa a su origen. El primer par de coordenadas especifica la esquina superior izquierda del rectángulo; el segundo par especifica el ancho y el alto. Si no se especifica esta marca, la imagen se copia en la esquina superior izquierda del búfer de fotogramas.

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

 


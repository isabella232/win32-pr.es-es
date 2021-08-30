---
title: MCI_RESTORE comando (Mmsystem.h)
description: El comando RESTORE de MCI \_ copia un mapa de bits de un archivo en el búfer de fotogramas. Los dispositivos de vídeo digital reconocen este comando. Este comando realiza la acción opuesta del comando MCI \_ CAPTURE.
ms.assetid: ed309cc6-72a3-4abb-aef2-40a55381d8b6
keywords:
- MCI_RESTORE comando Windows Multimedia
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
ms.openlocfilehash: 4a51753dbb5ed265bc9d60d5aafed38a9618854cb63500c1bf58e4d20b87a1ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038895"
---
# <a name="mci_restore-command"></a>Comando RESTORE de MCI \_

El comando RESTORE de MCI \_ copia un mapa de bits de un archivo en el búfer de fotogramas. Los dispositivos de vídeo digital reconocen este comando. Este comando realiza la acción opuesta del [comando MCI \_ CAPTURE.](mci-capture.md)

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT o MCI \_ TEST. Para obtener información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpRestore"></span><span id="lprestore"></span><span id="LPRESTORE"></span>*lpRestore*
</dt> <dd>

Puntero a una [**estructura \_ MCI DGV \_ RESTORE \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Comentarios

La implementación puede reconocer diversos formatos de imagen, pero siempre Windows mapa de bits independiente del dispositivo (DIB).

Las siguientes marcas adicionales se aplican a los dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_RESTORE_FROM"></span><span id="mci_dgv_restore_from"></span>RESTAURACIÓN \_ DE MCI DGV \_ \_ DESDE
</dt> <dd>

El **miembro lpstrFileName** de la estructura identificada por *lpRestore* contiene una dirección de un búfer que contiene el nombre de archivo de origen. Se requiere el nombre de archivo.

</dd> <dt>

<span id="MCI_DGV_RESTORE_AT"></span><span id="mci_dgv_restore_at"></span>RESTAURACIÓN \_ DE MCI DGV \_ \_ EN
</dt> <dd>

El **miembro rc** de la estructura identificada por *lpRestore* contiene un rectángulo válido. El rectángulo especifica una región del búfer de marco con respecto a su origen. El primer par de coordenadas especifica la esquina superior izquierda del rectángulo; el segundo par especifica el ancho y el alto. Si no se especifica esta marca, la imagen se copia en la esquina superior izquierda del búfer de fotogramas.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Comandos de MCI](mci-commands.md)
</dt> </dl>

 


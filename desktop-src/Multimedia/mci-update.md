---
title: MCI_UPDATE comando (Mmsystem.h)
description: El comando UPDATE de MCI \_ actualiza el rectángulo de presentación. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 90a8c10f-61b9-49a1-bbcc-e0729aa8c454
keywords:
- MCI_UPDATE comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_UPDATE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 423186096c88a8f1ff74987ff57c6b49dc6c3131
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370189"
---
# <a name="mci_update-command"></a>Comando UPDATE de MCI \_

El comando UPDATE de MCI \_ actualiza el rectángulo de presentación. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UPDATE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
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

**MCI \_ NOTIFY,** **MCI \_ WAIT** o, para dispositivos de vídeo digital, **MCI \_ TEST**. Para obtener información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*
</dt> <dd>

Puntero a una [**estructura \_ MCI GENERIC \_ PARMS.**](mci-generic-parms.md) (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las siguientes marcas adicionales se usan con el tipo de dispositivo "digitalvideo":

<dl> <dt>

<span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>ACTUALIZACIÓN \_ DE MCI DGV \_ \_ HDC
</dt> <dd>

El **miembro hDC** de la estructura identificada por *lpDest* contiene una ventana válida del controlador de dominio que se debe pintar. Esta marca es obligatoria.

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI \_ DGV \_ RECT
</dt> <dd>

El **miembro rc** de la estructura identificada por *lpUnfreeze* contiene un rectángulo de presentación válido. El rectángulo especifica el rectángulo de recorte en relación con el rectángulo del cliente.

</dd> <dt>

<span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>MCI \_ DGV \_ UPDATE \_ PAINT
</dt> <dd>

Una aplicación usa esta marca cuando recibe un [**mensaje \_ WM PAINT**](/windows/desktop/gdi/wm-paint) destinado a un controlador de dominio para mostrar. Un dispositivo de búfer de fotogramas suele pintar el color de la clave. Si el dispositivo para mostrar no tiene un búfer de fotogramas, podría omitir el comando UPDATE de MCI cuando se usa la marca \_ **\_ MCI DGV \_ UPDATE \_ PAINT** porque la pantalla se volverá a dibujar durante la operación de reproducción.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, el parámetro *lpDest* apunta a una estructura [**\_ MCI DGV \_ UPDATE \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms)

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

 


---
title: MCI_WINDOW comando (Mmsystem.h)
description: El comando WINDOW de MCI \_ especifica la ventana y las características de la ventana para los dispositivos gráficos. Los dispositivos de superposición de vídeo y vídeo digital reconocen este comando.
ms.assetid: 8b6c4d9a-ee72-4c64-aebe-6c8153167496
keywords:
- MCI_WINDOW comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_WINDOW
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41b4d630dbc9dbc7403e93cd0bda3de2eef1e5cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245847"
---
# <a name="mci_window-command"></a>Comando VENTANA de MCI \_

El comando WINDOW de MCI \_ especifica la ventana y las características de la ventana para los dispositivos gráficos. Los dispositivos de superposición de vídeo y vídeo digital reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WINDOW, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpWindow
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

MCI \_ NOTIFY, MCI \_ WAIT o, para dispositivos de vídeo digital, MCI \_ TEST. Para obtener información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*lpWindow*
</dt> <dd>

Puntero a una [**estructura \_ MCI GENERIC \_ PARMS.**](mci-generic-parms.md) (Los dispositivos con conjuntos de comandos extendidos pueden reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Los dispositivos gráficos deben crear una ventana predeterminada cuando se abre un dispositivo, pero no deben mostrarla hasta que reciban el [comando MCI \_ PLAY.](mci-play.md) El comando WINDOW de MCI se usa para proporcionar una ventana creada por la aplicación al dispositivo y para cambiar las características de visualización de una ventana de presentación predeterminada o definida \_ por la aplicación. Si la aplicación proporciona la ventana de presentación, debe estar preparada para actualizar un rectángulo no válido en la ventana.

Las siguientes marcas adicionales se usan con el **tipo de dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>HWND \_ DE VENTANA DE MCI DGV \_ \_
</dt> <dd>

El identificador de la ventana necesaria para su uso como destino se incluye en el **miembro hWnd** de la estructura identificada *por lpWindow*.

</dd> <dt>

<span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>ESTADO DE VENTANA \_ DE MCI DGV \_ \_
</dt> <dd>

El **miembro nCmdShow** de la estructura identificada por *lpWindow* contiene parámetros para establecer el estado de la ventana.

</dd> <dt>

<span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>TEXTO DE VENTANA \_ DE MCI DGV \_ \_
</dt> <dd>

El **miembro lpstrText** de la estructura identificada por *lpWindow* contiene una dirección de un búfer que contiene el título usado en la barra de título de la ventana.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, el *parámetro lpWindow* apunta a una estructura [**\_ MCI DGV \_ WINDOW \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa)

Las siguientes marcas adicionales se usan con el tipo **de dispositivo de** superposición:

<dl> <dt>

<span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>VENTANA MCI \_ OVLY \_ DESHABILITAR \_ \_ STRETCH
</dt> <dd>

Deshabilita la extensión de la imagen.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>VENTANA MCI \_ OVLY \_ HABILITAR \_ \_ STRETCH
</dt> <dd>

Habilita el stretching de la imagen.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>HWND DE VENTANA DE MCI \_ OVLY \_ \_
</dt> <dd>

El identificador de la ventana utilizada para el destino se incluye en el **miembro hWnd** de la estructura identificada *por lpWindow*. Establezca esta marca en MCI \_ OVLY \_ WINDOW DEFAULT para volver a la ventana \_ predeterminada.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>ESTADO DE VENTANA DE MCI \_ \_ \_ OVLY
</dt> <dd>

El **miembro nCmdShow** de la estructura *lpWindow* contiene parámetros para establecer el estado de la ventana. Esta marca equivale a llamar a [ShowWindow con](/windows/win32/api/winuser/nf-winuser-showwindow) el *parámetro state.* Las constantes son las mismas que las definidas en WINDOWS. H (como SW \_ HIDE, SW \_ MINIMIZE o SW \_ SHOWNORMAL).

</dd> <dt>

<span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>TEXTO DE \_ LA VENTANA MCI OVLY \_ \_
</dt> <dd>

El **miembro lpstrText** de la estructura identificada por *lpWindow* contiene una dirección de un búfer que contiene el título usado para la ventana.

</dd> </dl>

En el caso de los dispositivos de superposición de vídeo, el parámetro *lpWindow* apunta a una estructura [**\_ MCI OVLY \_ WINDOW \_ PARMS.**](mci-ovly-window-parms.md)

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

 


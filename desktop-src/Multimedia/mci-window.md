---
title: Comando MCI_WINDOW (mmsystem. h)
description: El \_ comando MCI Window especifica la ventana y las características de la ventana para los dispositivos gráficos. Los dispositivos de vídeo digital y de superposición reconocen este comando.
ms.assetid: 8b6c4d9a-ee72-4c64-aebe-6c8153167496
keywords:
- Comando de MCI_WINDOW de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996538"
---
# <a name="mci_window-command"></a>\_Comando de ventana MCI

El \_ comando MCI Window especifica la ventana y las características de la ventana para los dispositivos gráficos. Los dispositivos de vídeo digital y de superposición reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_La notificación de MCI, la espera de MCI \_ o, para dispositivos de vídeo digital, la prueba de MCI \_ . Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*lpWindow*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) . (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Los dispositivos gráficos deben crear una ventana predeterminada cuando se abre un dispositivo, pero no se debe mostrar hasta que reciban el comando de [ \_ reproducción de MCI](mci-play.md) . El \_ comando MCI Window se usa para proporcionar una ventana creada por la aplicación al dispositivo y para cambiar las características de presentación de una ventana de visualización definida por la aplicación o predeterminada. Si la aplicación proporciona la ventana de presentación, debe estar preparada para actualizar un rectángulo no válido en la ventana.

Con el tipo de dispositivo **DigitalVideo** se usan las siguientes marcas adicionales:

<dl> <dt>

<span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>\_ventana DGV de MCI \_ \_
</dt> <dd>

El identificador de la ventana necesaria para su uso como destino se incluye en el miembro **hWnd** de la estructura identificada por *lpWindow*.

</dd> <dt>

<span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>Estado de la ventana de MCI \_ DGV \_ \_
</dt> <dd>

El miembro **nCmdShow** de la estructura identificada por *lpWindow* contiene parámetros para establecer el estado de la ventana.

</dd> <dt>

<span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>texto de la ventana de DGV de MCI \_ \_ \_
</dt> <dd>

El miembro **lpstrText** de la estructura identificada por *lpWindow* contiene una dirección de un búfer que contiene el título usado en la barra de título de la ventana.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, el parámetro *lpWindow* apunta a una estructura [**parms de DGV de \_ \_ ventana \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa) .

Se usan las siguientes marcas adicionales con el tipo de dispositivo **superpuesto** :

<dl> <dt>

<span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>ventana de OVLY de MCI \_ \_ \_ deshabilitar \_ Stretch
</dt> <dd>

Deshabilita la expansión de la imagen.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>ventana de OVLY de MCI \_ \_ \_ habilitar \_ Stretch
</dt> <dd>

Habilita la expansión de la imagen.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>\_ventana OVLY de MCI \_ \_
</dt> <dd>

El identificador de la ventana que se usa para el destino se incluye en el miembro **hWnd** de la estructura identificada por *lpWindow*. Establezca esta marca en \_ \_ \_ el valor predeterminado de la ventana MCI OVLY para volver a la ventana predeterminada.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>Estado de la ventana de MCI \_ OVLY \_ \_
</dt> <dd>

El miembro **nCmdShow** de la estructura *lpWindow* contiene parámetros para establecer el estado de la ventana. Esta marca es equivalente a llamar a [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow) con el parámetro *State* . Las constantes son las mismas que las definidas en WINDOWS. H (como SW \_ Hide, SW \_ minimizar o SW \_ SHOWNORMAL).

</dd> <dt>

<span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>texto de la ventana de OVLY de MCI \_ \_ \_
</dt> <dd>

El miembro **lpstrText** de la estructura identificada por *lpWindow* contiene una dirección de un búfer que contiene el título que se usa para la ventana.

</dd> </dl>

En el caso de los dispositivos de superposición de vídeo, el parámetro *lpWindow* apunta a una estructura [**parms de OVLY de \_ \_ ventana \_ MCI**](mci-ovly-window-parms.md) .

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

 


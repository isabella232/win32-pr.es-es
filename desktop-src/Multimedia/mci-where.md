---
title: MCI_WHERE comando (Mmsystem.h)
description: El comando MCI \_ WHERE obtiene el rectángulo de recorte para el dispositivo de vídeo.
ms.assetid: f64a7e49-4ee1-4836-ba9a-0bbdc47626b3
keywords:
- MCI_WHERE comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_WHERE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6619131319863d1159a3bdb8bb85d366243544a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245846"
---
# <a name="mci_where-command"></a>Comando WHERE de MCI \_

El comando MCI \_ WHERE obtiene el rectángulo de recorte para el dispositivo de vídeo. Los dispositivos de vídeo digital y de superposición de vídeo reconocen este comando. Los **miembros** superior **e izquierdo** del [RECT](/previous-versions//ms536136(v=vs.85)) devuelto contienen el  origen  del rectángulo de recorte, y los miembros derecho e inferior contienen el ancho y el alto del rectángulo de recorte. (Este no es el uso estándar de los **miembros derecho** **e** inferior).

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WHERE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpQuery
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

<span id="lpQuery"></span><span id="lpquery"></span><span id="LPQUERY"></span>*lpQuery*
</dt> <dd>

Puntero a una [**estructura \_ MCI GENERIC \_ PARMS.**](mci-generic-parms.md) (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las siguientes marcas adicionales se usan con el **tipo de dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_WHERE_DESTINATION"></span><span id="mci_dgv_where_destination"></span>MCI \_ DGV \_ WHERE \_ DESTINATION
</dt> <dd>

Obtiene una descripción de la región rectangular que se usa para mostrar vídeo e imágenes en el área cliente de la ventana actual.

</dd> <dt>

<span id="MCI_DGV_WHERE_FRAME"></span><span id="mci_dgv_where_frame"></span>MCI \_ DGV \_ WHERE \_ FRAME
</dt> <dd>

Obtiene una descripción de la región rectangular del búfer de marco en la que se escalan las imágenes del rectángulo de vídeo. Las coordenadas del rectángulo se colocan en el **miembro rc** de la estructura identificada por *lpQuery*.

</dd> <dt>

<span id="MCI_DGV_WHERE_MAX"></span><span id="mci_dgv_where_max"></span>MCI \_ DGV \_ WHERE \_ MAX
</dt> <dd>

Cuando se usa con MCI DGV WHERE DESTINATION o \_ \_ \_ MCI \_ DGV WHERE SOURCE, el rectángulo devuelto indica el ancho y alto máximos de \_ \_ la región especificada. Cuando se usa con MCI \_ DGV WHERE WINDOW, el rectángulo devuelto \_ indica el tamaño de toda la \_ pantalla.

</dd> <dt>

<span id="MCI_DGV_WHERE_SOURCE"></span><span id="mci_dgv_where_source"></span>MCI \_ DGV \_ WHERE \_ SOURCE
</dt> <dd>

Obtiene una descripción de la región rectangular (recortada del búfer de marco) que se ajusta para ajustarse al rectángulo de destino en la pantalla.

</dd> <dt>

<span id="MCI_DGV_WHERE_VIDEO"></span><span id="mci_dgv_where_video"></span>MCI \_ DGV \_ WHERE \_ VIDEO
</dt> <dd>

Obtiene una descripción de la región rectangular recortada del origen de la presentación para rellenar el rectángulo de marco en el búfer del marco. Las coordenadas del rectángulo se colocan en el **miembro rc** de la estructura identificada por *lpQuery*.

</dd> <dt>

<span id="MCI_DGV_WHERE_WINDOW"></span><span id="mci_dgv_where_window"></span>VENTANA WHERE DE MCI \_ DGV \_ \_
</dt> <dd>

Obtiene una descripción del marco de la ventana de presentación.

</dd> <dt>


</dt> <dd></dd> </dl>

En el caso de los dispositivos de vídeo digital, el parámetro *lpQuery* apunta a una estructura **de MCI \_ DGV \_ WHERE \_ PARMS.** La **estructura MCI \_ DGV WHERE \_ \_ PARMS** es idéntica a la estructura [**\_ MCI DGV \_ RECT \_ PARMS.**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms)

Las siguientes marcas adicionales se usan con el tipo **de dispositivo superpuesto:**

<dl> <dt>

<span id="MCI_OVLY_WHERE_DESTINATION"></span><span id="mci_ovly_where_destination"></span>MCI \_ OVLY \_ WHERE \_ DESTINATION
</dt> <dd>

Obtiene el rectángulo de presentación de destino. Las coordenadas del rectángulo se colocan en el **miembro rc** de la estructura identificada por *lpQuery*.

</dd> <dt>

<span id="MCI_OVLY_WHERE_FRAME"></span><span id="mci_ovly_where_frame"></span>MCI \_ OVLY \_ WHERE \_ FRAME
</dt> <dd>

Obtiene el rectángulo del marco superpuesto. Las coordenadas del rectángulo se colocan en el **miembro rc** de la estructura identificada por *lpQuery*.

</dd> <dt>

<span id="MCI_OVLY_WHERE_SOURCE"></span><span id="mci_ovly_where_source"></span>MCI \_ OVLY \_ WHERE \_ SOURCE
</dt> <dd>

Obtiene el rectángulo de origen. Las coordenadas del rectángulo se colocan en el **miembro rc** de la estructura identificada por *lpQuery*.

</dd> <dt>

<span id="MCI_OVLY_WHERE_VIDEO"></span><span id="mci_ovly_where_video"></span>MCI \_ OVLY \_ WHERE \_ VIDEO
</dt> <dd>

Obtiene el rectángulo de vídeo. Las coordenadas del rectángulo se colocan en el **miembro rc** de la estructura identificada por *lpQuery*.

</dd> </dl>

En el caso de los dispositivos de superposición de vídeo, el parámetro *lpQuery* apunta a una estructura [**\_ \_ MCI OVLY RECT \_ PARMS.**](mci-ovly-rect-parms.md)

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

 


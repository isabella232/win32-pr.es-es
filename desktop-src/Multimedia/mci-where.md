---
title: Comando MCI_WHERE (mmsystem. h)
description: El \_ comando MCI donde obtiene el rectángulo de recorte para el dispositivo de vídeo.
ms.assetid: f64a7e49-4ee1-4836-ba9a-0bbdc47626b3
keywords:
- Comando de MCI_WHERE de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996450"
---
# <a name="mci_where-command"></a>\_Comando MCI Where

El \_ comando MCI donde obtiene el rectángulo de recorte para el dispositivo de vídeo. Los dispositivos de vídeo digital y de superposición reconocen este comando. Los miembros **superior** e **izquierdo** del [Rect](/previous-versions//ms536136(v=vs.85)) devuelto contienen el origen del rectángulo de recorte y los miembros **derecho** e **inferior** contienen el ancho y el alto del rectángulo de recorte. (Este no es el uso estándar de los miembros **derecho** e **inferior** ).

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_La notificación de MCI, la espera de MCI \_ o, para dispositivos de vídeo digital, la prueba de MCI \_ . Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpQuery"></span><span id="lpquery"></span><span id="LPQUERY"></span>*lpQuery*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) . (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Con el tipo de dispositivo **DigitalVideo** se usan las siguientes marcas adicionales:

<dl> <dt>

<span id="MCI_DGV_WHERE_DESTINATION"></span><span id="mci_dgv_where_destination"></span>MCI \_ DGV \_ donde \_ destino
</dt> <dd>

Obtiene una descripción de la región rectangular utilizada para mostrar vídeo e imágenes en el área cliente de la ventana actual.

</dd> <dt>

<span id="MCI_DGV_WHERE_FRAME"></span><span id="mci_dgv_where_frame"></span>\_DGV MCI \_ donde \_ marco
</dt> <dd>

Obtiene una descripción de la región rectangular del búfer de fotogramas en el que se escalan las imágenes del rectángulo de vídeo. Las coordenadas del rectángulo se colocan en el miembro **RC** de la estructura identificada por *lpQuery*.

</dd> <dt>

<span id="MCI_DGV_WHERE_MAX"></span><span id="mci_dgv_where_max"></span>MCI \_ DGV \_ Where \_ Max
</dt> <dd>

Cuando se usa con MCI \_ DGV \_ donde \_ Destination o MCI \_ DGV \_ Where \_ source, el rectángulo devuelto indica el ancho y el alto máximos de la región especificada. Cuando se usa con la ventana de MCI \_ DGV \_ Where \_ , el rectángulo devuelto indica el tamaño de la pantalla completa.

</dd> <dt>

<span id="MCI_DGV_WHERE_SOURCE"></span><span id="mci_dgv_where_source"></span>MCI \_ DGV \_ Where \_ source
</dt> <dd>

Obtiene una descripción de la región rectangular (recortada a partir del búfer de fotogramas) que se ajusta para ajustarse al rectángulo de destino de la pantalla.

</dd> <dt>

<span id="MCI_DGV_WHERE_VIDEO"></span><span id="mci_dgv_where_video"></span>DGV de MCI \_ \_ donde \_ vídeo
</dt> <dd>

Obtiene una descripción de la región rectangular recortada del origen de presentación para rellenar el rectángulo del marco en el búfer de fotogramas. Las coordenadas del rectángulo se colocan en el miembro **RC** de la estructura identificada por *lpQuery*.

</dd> <dt>

<span id="MCI_DGV_WHERE_WINDOW"></span><span id="mci_dgv_where_window"></span>\_ventana de DGV MCI \_ \_
</dt> <dd>

Obtiene una descripción del marco de la ventana de presentación.

</dd> <dt>


</dt> <dd></dd> </dl>

En el caso de los dispositivos de vídeo digital, el parámetro *lpQuery* apunta a una **\_ DGV MCI \_ donde \_ parms** estructura. La estructura **MCI \_ DGV \_ donde \_ parms** es idéntica a la estructura [**MCI \_ DGV \_ Rect \_ parms**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) .

Se usan las siguientes marcas adicionales con el tipo de dispositivo **superpuesto** :

<dl> <dt>

<span id="MCI_OVLY_WHERE_DESTINATION"></span><span id="mci_ovly_where_destination"></span>MCI \_ OVLY \_ donde \_ destino
</dt> <dd>

Obtiene el rectángulo de presentación de destino. Las coordenadas del rectángulo se colocan en el miembro **RC** de la estructura identificada por *lpQuery*.

</dd> <dt>

<span id="MCI_OVLY_WHERE_FRAME"></span><span id="mci_ovly_where_frame"></span>\_OVLY MCI \_ donde \_ marco
</dt> <dd>

Obtiene el rectángulo del marco superpuesto. Las coordenadas del rectángulo se colocan en el miembro **RC** de la estructura identificada por *lpQuery*.

</dd> <dt>

<span id="MCI_OVLY_WHERE_SOURCE"></span><span id="mci_ovly_where_source"></span>MCI \_ OVLY \_ Where \_ source
</dt> <dd>

Obtiene el rectángulo de origen. Las coordenadas del rectángulo se colocan en el miembro **RC** de la estructura identificada por *lpQuery*.

</dd> <dt>

<span id="MCI_OVLY_WHERE_VIDEO"></span><span id="mci_ovly_where_video"></span>OVLY de MCI \_ \_ donde \_ vídeo
</dt> <dd>

Obtiene el rectángulo de vídeo. Las coordenadas del rectángulo se colocan en el miembro **RC** de la estructura identificada por *lpQuery*.

</dd> </dl>

En el caso de los dispositivos de superposición de vídeo, el parámetro *lpQuery* apunta a una estructura [**MCI \_ OVLY \_ Rect \_ parms**](mci-ovly-rect-parms.md) .

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

 


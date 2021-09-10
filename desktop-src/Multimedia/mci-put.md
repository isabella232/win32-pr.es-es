---
title: MCI_PUT comando (Mmsystem.h)
description: El comando PUT de MCI establece los rectángulos de \_ origen, destino y marco. Los dispositivos de superposición de vídeo digital y vídeo reconocen este comando.
ms.assetid: 9d81682b-6546-4e6d-a6df-e2de8c013b66
keywords:
- MCI_PUT comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_PUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fa4af30aa2b3aa6f7cdd50f453bc8edca83334
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369914"
---
# <a name="mci_put-command"></a>Comando PUT de MCI \_

El comando PUT de MCI establece los rectángulos de \_ origen, destino y marco. Los dispositivos de superposición de vídeo digital y vídeo reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PUT, 
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

MCI \_ NOTIFY, MCI \_ WAIT o, para dispositivos de vídeo digital, MCI \_ TEST. Para obtener información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*
</dt> <dd>

Puntero a una [**estructura \_ MCI GENERIC \_ PARMS.**](mci-generic-parms.md) (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Las siguientes marcas adicionales se usan con el **tipo de dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_PUT_CLIENT"></span><span id="mci_dgv_put_client"></span>MCI \_ DGV \_ PUT \_ CLIENT
</dt> <dd>

El rectángulo definido para MCI \_ DGV \_ RECT se aplica a la posición de la ventana de cliente. El rectángulo especificado es relativo a la ventana primaria de la ventana de presentación. MCI \_ DGV \_ PUT WINDOW debe \_ establecerse simultáneamente con esta marca.

</dd> <dt>

<span id="MCI_DGV_PUT_DESTINATION"></span><span id="mci_dgv_put_destination"></span>MCI \_ DGV \_ PUT \_ DESTINATION
</dt> <dd>

El rectángulo definido para MCI \_ DGV \_ RECT especifica un rectángulo de destino. El rectángulo de destino especifica la parte de la ventana de cliente asociada a esta instancia del controlador de dispositivo que muestra la imagen o el vídeo.

</dd> <dt>

<span id="MCI_DGV_PUT_FRAME"></span><span id="mci_dgv_put_frame"></span>MCI \_ DGV \_ PUT \_ FRAME
</dt> <dd>

El rectángulo definido para MCI \_ DGV \_ RECT se aplica al rectángulo de marco. El rectángulo de marco especifica la parte del búfer de fotogramas que se usa como destino de las imágenes de vídeo obtenidas del rectángulo de vídeo. El vídeo debe escalarse para ajustarse al rectángulo del búfer del marco.

El rectángulo se especifica en coordenadas de búfer de marco. El rectángulo predeterminado es el búfer de marco completo. La especificación de este rectángulo permite al dispositivo escalar la imagen a medida que digitaliza los datos. Los dispositivos que no pueden escalar la imagen rechazan este comando con MCIERR \_ UNSUPPORTED \_ FUNCTION. Puede usar la marca GETDEVCAPS CAN STRETCH de MCI con el comando \_ \_ \_ [ \_ GETDEVCAPS](mci-getdevcaps.md) de MCI para determinar si un dispositivo escala la imagen. Un dispositivo devuelve **FALSE si** no puede escalar la imagen.

</dd> <dt>

<span id="MCI_DGV_PUT_SOURCE"></span><span id="mci_dgv_put_source"></span>MCI \_ DGV \_ PUT \_ SOURCE
</dt> <dd>

El rectángulo definido para MCI \_ DGV \_ RECT especifica un rectángulo de origen. El rectángulo de origen especifica qué parte del búfer de marco se va a escalar para ajustarse al rectángulo de destino.

</dd> <dt>

<span id="MCI_DGV_PUT_VIDEO"></span><span id="mci_dgv_put_video"></span>VÍDEO PUT DE MCI \_ DGV \_ \_
</dt> <dd>

El rectángulo definido para MCI \_ DGV \_ RECT se aplica al rectángulo de vídeo. El rectángulo de vídeo especifica qué parte del origen de presentación actual se almacena en el búfer de fotogramas. El rectángulo se especifica mediante las coordenadas naturales del origen de la presentación. Permite especificar el recorte que se produce antes de almacenar imágenes y vídeo en el búfer de fotogramas. El rectángulo predeterminado es el área de examen activa completa o las imágenes y el vídeo descomprimidos completos.

</dd> <dt>

<span id="MCI_DGV_PUT_WINDOW"></span><span id="mci_dgv_put_window"></span>VENTANA \_ PUT de MCI DGV \_ \_
</dt> <dd>

El rectángulo definido para MCI \_ DGV \_ RECT se aplica a la ventana de presentación. Este rectángulo es relativo a la ventana primaria de la ventana de presentación (normalmente el escritorio). Si no se especifica la ventana, el valor predeterminado es el tamaño y la posición iniciales de la ventana.

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI \_ DGV \_ RECT
</dt> <dd>

El **miembro rc** de la estructura identificada por *lpDest* contiene un rectángulo válido.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, *lpDest* apunta a una estructura [**\_ MCI DGV \_ PUT \_ PARMS.**](/previous-versions//dd743397(v=vs.85))

Las siguientes marcas adicionales se usan con el tipo **de dispositivo superpuesto:**

<dl> <dt>

<span id="MCI_OVLY_PUT_DESTINATION"></span><span id="mci_ovly_put_destination"></span>MCI \_ OVLY \_ PUT \_ DESTINATION
</dt> <dd>

El rectángulo definido para MCI OVLY RECT especifica el área de la ventana \_ de cliente utilizada para mostrar una \_ imagen. El rectángulo contiene el desplazamiento y la extensión visible de la imagen con respecto al origen de la ventana. Si el marco se va a extender, el origen se extiende al rectángulo de destino.

</dd> <dt>

<span id="MCI_OVLY_PUT_FRAME"></span><span id="mci_ovly_put_frame"></span>MCI \_ OVLY \_ PUT \_ FRAME
</dt> <dd>

El rectángulo definido para MCI OVLY RECT especifica el área del búfer de vídeo que se \_ usa para recibir la imagen de \_ vídeo. El rectángulo contiene el desplazamiento y la extensión del área de búfer en relación con el origen del búfer de vídeo.

</dd> <dt>

<span id="MCI_OVLY_PUT_SOURCE"></span><span id="mci_ovly_put_source"></span>MCI \_ OVLY \_ PUT \_ SOURCE
</dt> <dd>

El rectángulo definido para MCI OVLY RECT especifica el área del búfer de vídeo que se usa como origen \_ \_ de la imagen digital. El rectángulo contiene el desplazamiento y la extensión del rectángulo de recorte para el búfer de vídeo con respecto a su origen.

</dd> <dt>

<span id="MCI_OVLY_PUT_VIDEO"></span><span id="mci_ovly_put_video"></span>VÍDEO \_ DE MCI OVLY \_ \_ PUT
</dt> <dd>

El rectángulo definido para MCI OVLY RECT especifica el área de la captura de origen de \_ vídeo por el búfer de \_ vídeo. El rectángulo contiene el desplazamiento y la extensión del rectángulo de recorte para el origen del vídeo en relación con su origen.

</dd> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ RECT
</dt> <dd>

El **miembro rc** de la estructura identificada por *lpDest* contiene un rectángulo de presentación válido. Si no se especifica esta marca, el rectángulo predeterminado coincide con las coordenadas del búfer de vídeo o la ventana que se va a recortar.

</dd> </dl>

En el caso de los dispositivos de superposición de vídeo, *lpDest* apunta a una estructura [**\_ \_ MCI OVLY RECT \_ PARMS.**](mci-ovly-rect-parms.md)

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

 


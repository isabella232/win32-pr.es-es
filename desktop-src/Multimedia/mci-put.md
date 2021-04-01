---
title: Comando MCI_PUT (mmsystem. h)
description: El \_ comando MCI Put establece los rectángulos de origen, de destino y de marco. Los dispositivos de vídeo digital y de superposición reconocen este comando.
ms.assetid: 9d81682b-6546-4e6d-a6df-e2de8c013b66
keywords:
- Comando de MCI_PUT de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151238"
---
# <a name="mci_put-command"></a>\_Comando MCI Put

El \_ comando MCI Put establece los rectángulos de origen, de destino y de marco. Los dispositivos de vídeo digital y de superposición reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_La notificación de MCI, la espera de MCI \_ o, para dispositivos de vídeo digital, la prueba de MCI \_ . Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) . (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Con el tipo de dispositivo **DigitalVideo** se usan las siguientes marcas adicionales:

<dl> <dt>

<span id="MCI_DGV_PUT_CLIENT"></span><span id="mci_dgv_put_client"></span>\_cliente de DGV de MCI \_ \_
</dt> <dd>

El rectángulo definido para MCI \_ DGV \_ Rect se aplica a la posición de la ventana del cliente. El rectángulo especificado es relativo a la ventana primaria de la ventana de presentación. \_ \_ \_ La ventana de colocación de MCI DGV debe establecerse simultáneamente con esta marca.

</dd> <dt>

<span id="MCI_DGV_PUT_DESTINATION"></span><span id="mci_dgv_put_destination"></span>\_ \_ destino put de MCI DGV \_
</dt> <dd>

El rectángulo definido para MCI \_ DGV \_ Rect especifica un rectángulo de destino. El rectángulo de destino especifica la parte de la ventana de cliente asociada a esta instancia de controlador de dispositivo que muestra la imagen o el vídeo.

</dd> <dt>

<span id="MCI_DGV_PUT_FRAME"></span><span id="mci_dgv_put_frame"></span>fotograma de DGV de MCI \_ \_ \_
</dt> <dd>

El rectángulo definido para MCI \_ DGV \_ Rect se aplica al rectángulo del marco. El rectángulo de marco especifica la parte del búfer de fotogramas que se usa como destino de las imágenes de vídeo obtenidas del rectángulo de vídeo. El vídeo se debe escalar para ajustarse al rectángulo de búfer de fotogramas.

El rectángulo se especifica en coordenadas de búfer de fotogramas. El rectángulo predeterminado es el búfer de marco completo. Especificar este rectángulo permite que el dispositivo escale la imagen a medida que digitaliza los datos. Los dispositivos que no pueden escalar la imagen rechazan este comando con la \_ función MCIERR no admitida \_ . Puede usar la marca MCI \_ GETDEVCAPS \_ Can \_ Stretch con el comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) para determinar si un dispositivo escala la imagen. Un dispositivo devuelve **false** si no puede escalar la imagen.

</dd> <dt>

<span id="MCI_DGV_PUT_SOURCE"></span><span id="mci_dgv_put_source"></span>\_origen de DGV de MCI \_ \_
</dt> <dd>

El rectángulo definido para MCI \_ DGV \_ Rect especifica un rectángulo de origen. El rectángulo de origen especifica qué parte del búfer de fotogramas se va a escalar para ajustarse al rectángulo de destino.

</dd> <dt>

<span id="MCI_DGV_PUT_VIDEO"></span><span id="mci_dgv_put_video"></span>\_vídeo de DGV de MCI \_ \_
</dt> <dd>

El rectángulo definido para MCI \_ DGV \_ Rect se aplica al rectángulo de vídeo. El rectángulo de vídeo especifica qué parte del origen de presentación actual se almacena en el búfer de fotogramas. El rectángulo se especifica mediante las coordenadas naturales del origen de presentación. Permite la especificación del recorte que se produce antes de almacenar imágenes y vídeo en el búfer de fotogramas. El rectángulo predeterminado es el área de análisis activa completa o las imágenes y el vídeo descomprimidos completos.

</dd> <dt>

<span id="MCI_DGV_PUT_WINDOW"></span><span id="mci_dgv_put_window"></span>\_ventana de \_ colocación de DGV de MCI \_
</dt> <dd>

El rectángulo definido para MCI \_ DGV \_ Rect se aplica a la ventana de presentación. Este rectángulo es relativo a la ventana primaria de la ventana de presentación (normalmente el escritorio). Si no se especifica la ventana, se toma como valor predeterminado el tamaño y la posición de la ventana inicial.

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV \_ Rect
</dt> <dd>

El miembro **RC** de la estructura identificada por *lpDest* contiene un rectángulo válido.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, *lpDest* apunta a una estructura [**MCI \_ DGV \_ Put \_ parms**](/previous-versions//dd743397(v=vs.85)) .

Se usan las siguientes marcas adicionales con el tipo de dispositivo **superpuesto** :

<dl> <dt>

<span id="MCI_OVLY_PUT_DESTINATION"></span><span id="mci_ovly_put_destination"></span>\_ \_ destino put de MCI OVLY \_
</dt> <dd>

El rectángulo definido para MCI \_ OVLY \_ Rect especifica el área de la ventana de cliente que se usa para mostrar una imagen. El rectángulo contiene el desplazamiento y la extensión visible de la imagen en relación con el origen de la ventana. Si se va a estirar el marco, el origen se ajusta al rectángulo de destino.

</dd> <dt>

<span id="MCI_OVLY_PUT_FRAME"></span><span id="mci_ovly_put_frame"></span>fotograma de OVLY de MCI \_ \_ \_
</dt> <dd>

El rectángulo definido para MCI \_ OVLY \_ Rect especifica el área del búfer de vídeo que se usa para recibir la imagen de vídeo. El rectángulo contiene el desplazamiento y la extensión del área del búfer en relación con el origen del búfer de vídeo.

</dd> <dt>

<span id="MCI_OVLY_PUT_SOURCE"></span><span id="mci_ovly_put_source"></span>\_origen de OVLY de MCI \_ \_
</dt> <dd>

El rectángulo definido para MCI \_ OVLY \_ Rect especifica el área del búfer de vídeo que se usa como origen de la imagen digital. El rectángulo contiene el desplazamiento y la extensión del rectángulo de recorte para el búfer de vídeo en relación con su origen.

</dd> <dt>

<span id="MCI_OVLY_PUT_VIDEO"></span><span id="mci_ovly_put_video"></span>\_vídeo de OVLY de MCI \_ \_
</dt> <dd>

El rectángulo definido para MCI \_ OVLY \_ Rect especifica el área de la captura de origen de vídeo por el búfer de vídeo. El rectángulo contiene el desplazamiento y la extensión del rectángulo de recorte para el origen de vídeo en relación con su origen.

</dd> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY \_ Rect
</dt> <dd>

El miembro **RC** de la estructura identificada por *lpDest* contiene un rectángulo de presentación válido. Si no se especifica esta marca, el rectángulo predeterminado coincide con las coordenadas del búfer de vídeo o de la ventana que se va a recortar.

</dd> </dl>

En el caso de los dispositivos de superposición de vídeo, *lpDest* apunta a una estructura [**MCI \_ OVLY \_ Rect \_ parms**](mci-ovly-rect-parms.md) .

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

 


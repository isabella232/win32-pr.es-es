---
title: Comando MCI_UPDATE (mmsystem. h)
description: El comando de actualización de MCI \_ actualiza el rectángulo de presentación. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 90a8c10f-61b9-49a1-bbcc-e0729aa8c454
keywords:
- Comando de MCI_UPDATE de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151029"
---
# <a name="mci_update-command"></a>Comando de actualización de MCI \_

El comando de actualización de MCI \_ actualiza el rectángulo de presentación. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

**MCI \_ NOTIFICAr**, **\_ espera de MCI** o, para dispositivos de vídeo digital **, \_ prueba de MCI**. Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) . (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Se usan las siguientes marcas adicionales con el tipo de dispositivo "DigitalVideo":

<dl> <dt>

<span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>actualización de DGV de MCI \_ \_ \_ HDC
</dt> <dd>

El miembro **HDC** de la estructura identificada por *lpDest* contiene una ventana válida del controlador de dominio que se va a pintar. Esta marca es obligatoria.

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV \_ Rect
</dt> <dd>

El miembro **RC** de la estructura identificada por *lpUnfreeze* contiene un rectángulo de presentación válido. El rectángulo especifica el rectángulo de recorte relativo al rectángulo de cliente.

</dd> <dt>

<span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>\_DGV MCI \_ actualizar \_ Paint
</dt> <dd>

Una aplicación usa esta marca cuando recibe un mensaje [**de \_ dibujo de WM**](/windows/desktop/gdi/wm-paint) diseñado para un controlador de dominio de pantalla. Normalmente, un dispositivo de búfer de fotogramas pinta el color de la clave. Si el dispositivo de pantalla no tiene un búfer de fotogramas, podría omitir el comando de actualización de MCI \_ cuando se use la marca de **\_ Paint de \_ actualización \_ de MCI DGV** , ya que la pantalla se volverá a dibujar durante la operación de reproducción.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, el parámetro *lpDest* apunta a una estructura [**MCI \_ DGV \_ Update \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms) .

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

 


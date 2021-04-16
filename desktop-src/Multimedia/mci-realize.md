---
title: Comando MCI_REALIZE (mmsystem. h)
description: El \_ comando MCI Observate hace que un dispositivo gráfico obtenga su paleta en un contexto de dispositivo (DC). Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: cbc9e6ef-a372-4ddb-b7f3-ea99ac14ec95
keywords:
- Comando de MCI_REALIZE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_REALIZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f2e59bfe9bbe1443f55ae0fbcf8819b932bb1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651394"
---
# <a name="mci_realize-command"></a>Comando de MCI \_

El \_ comando MCI Observate hace que un dispositivo gráfico obtenga su paleta en un contexto de dispositivo (DC). Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_REALIZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpRealize
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

<span id="lpRealize"></span><span id="lprealize"></span><span id="LPREALIZE"></span>*lpRealize*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) . (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Debe usar este comando cuando la aplicación reciba el mensaje [**de \_ QUERYNEWPALETTE de WM**](/windows/desktop/gdi/wm-querynewpalette) .

Se usan las siguientes marcas adicionales con el tipo de dispositivo "DigitalVideo":

<dl> <dt>

<span id="MCI_DGV_REALIZE_BKGD"></span><span id="mci_dgv_realize_bkgd"></span>MCI \_ DGV \_ obtener \_ BKGD
</dt> <dd>

Obtiene la paleta como una paleta de fondo.

</dd> <dt>

<span id="MCI_DGV_REALIZE_NORM"></span><span id="mci_dgv_realize_norm"></span>\_norma de DGV de MCI \_ \_
</dt> <dd>

Obtiene la paleta normalmente. Este es el valor predeterminado.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, el parámetro *lpRealize* apunta a una estructura de **MCI \_ \_ parms** . Para obtener más información, consulte comentarios en la estructura [**\_ \_ parms genérica de MCI**](mci-generic-parms.md) .

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

 


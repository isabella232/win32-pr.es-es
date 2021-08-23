---
title: MCI_REALIZE comando (Mmsystem.h)
description: El comando MCI REALIZE hace que un dispositivo gráfico se dé cuenta de \_ su paleta en un contexto de dispositivo (DC). Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: cbc9e6ef-a372-4ddb-b7f3-ea99ac14ec95
keywords:
- MCI_REALIZE comando Windows Multimedia
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
ms.openlocfilehash: e81204fe679d543438a0d0dcc7ec333462cb6a3d0c30212706969dc22a143df1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689836"
---
# <a name="mci_realize-command"></a>Comando MCI \_ REALIZE

El comando MCI REALIZE hace que un dispositivo gráfico se dé cuenta de \_ su paleta en un contexto de dispositivo (DC). Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

**MCI \_ NOTIFY**, **MCI \_ WAIT** o, para dispositivos de vídeo digital, **MCI \_ TEST**. Para obtener información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpRealize"></span><span id="lprealize"></span><span id="LPREALIZE"></span>*lpRealize*
</dt> <dd>

Puntero a una [**estructura \_ MCI GENERIC \_ PARMS.**](mci-generic-parms.md) (Los dispositivos con conjuntos de comandos extendidos pueden reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Comentarios

Debe usar este comando cuando la aplicación reciba el mensaje [**\_ WM QUERYNEWPALETTE.**](/windows/desktop/gdi/wm-querynewpalette)

Las siguientes marcas adicionales se usan con el tipo de dispositivo "digitalvideo":

<dl> <dt>

<span id="MCI_DGV_REALIZE_BKGD"></span><span id="mci_dgv_realize_bkgd"></span>MCI \_ DGV \_ REALIZE B \_ PROFIL
</dt> <dd>

Realiza la paleta como una paleta de fondo.

</dd> <dt>

<span id="MCI_DGV_REALIZE_NORM"></span><span id="mci_dgv_realize_norm"></span>MCI \_ DGV \_ REALIZE \_ NORM
</dt> <dd>

Realiza la paleta con normalidad. Este es el valor predeterminado.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, el *parámetro lpRealize* apunta a una **estructura \_ MCI REALIZE \_ PARMS.** Para obtener más información, vea comentarios en la estructura [**\_ MCI GENERIC \_ PARMS.**](mci-generic-parms.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 


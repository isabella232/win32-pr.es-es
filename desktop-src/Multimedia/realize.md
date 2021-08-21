---
title: comando realize
description: El comando realize indica a un dispositivo que seleccione y se dé cuenta de su paleta en el contexto de presentación de la ventana mostrada. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: ad3a52dc-5c8d-47fc-95bd-437b700fc029
keywords:
- realización del comando Windows Multimedia
topic_type:
- apiref
api_name:
- realize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc0aba1e610f4636c7dbfb71fbc959d9b4b8496cc23e91a97100ef6edce133b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371440"
---
# <a name="realize-command"></a>comando realize

El comando realize indica a un dispositivo que seleccione y se dé cuenta de su paleta en el contexto de presentación de la ventana mostrada. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("realize %s %s %s"), 
  lpszDeviceID, 
  lpszPalette, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszPalette"></span><span id="lpszpalette"></span><span id="LPSZPALETTE"></span>*lpszPalette*
</dt> <dd>

Una de las marcas siguientes.



| Valor      | Significado                                                                   |
|------------|---------------------------------------------------------------------------|
| background | Realiza la paleta como una paleta de fondo.                             |
| normal     | Realiza la paleta de una ventana de nivel superior. Esta es la configuración predeterminada. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o ambos. En el caso de los dispositivos de vídeo digital, también se puede especificar "prueba". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Comentarios

Use este comando solo si la aplicación usa un identificador de ventana y recibe un mensaje **\_ WM QUERYNEWPALVARIABLE** **o WM \_ PALETTECHANGED.**

## <a name="examples"></a>Ejemplos

El comando siguiente indica al dispositivo "myvideo" que se dé cuenta de su paleta.

``` syntax
realize myvideo normal
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Cadenas de comandos de MCI](mci-command-strings.md)
</dt> </dl>

 


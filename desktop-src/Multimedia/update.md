---
title: comando update
description: El comando update vuelve a dibujar el marco actual en el contexto de dispositivo (DC) especificado. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 51a83262-91d5-4852-ad17-bd62c14417b1
keywords:
- comando update Windows Multimedia
topic_type:
- apiref
api_name:
- update
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cb0fc96d404efd8e2f657985ffa5a8861d3b4f4
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370159"
---
# <a name="update-command"></a>comando update

El comando update vuelve a dibujar el marco actual en el contexto de dispositivo (DC) especificado. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("update %s %s %s"), 
  lpszDeviceID, 
  lpszHDC, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszHDC"></span><span id="lpszhdc"></span><span id="LPSZHDC"></span>*lpszHDC*
</dt> <dd>

Identificador de un controlador de dominio. En la tabla siguiente se enumeran los tipos de dispositivo que reconocen el comando **update** y las marcas usadas por cada tipo.



| Value        | Significado                       | Significado         |
|--------------|-------------------------------|-----------------|
| digitalvideo | hdc *hdc* hdc *hdc* at *rect* | paint hdc *hdc* |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el **parámetro lpszHDC** y sus significados.



| Value               | Significado                                                                                                |
|---------------------|--------------------------------------------------------------------------------------------------------|
| hdc *hdc*           | Especifica el identificador del controlador de dominio que se pintará.                                                               |
| hdc *hdc* at *rect* | Especifica el rectángulo de recorte relativo al rectángulo del cliente.                                     |
| paint hdc *hdc*     | Pinta el controlador de dominio cuando la aplicación recibe un [**mensaje \_ WM PAINT**](/windows/desktop/gdi/wm-paint) destinado a un controlador de dominio. |



 

Para especificar el identificador del controlador de dominio, use la cadena "hdc" seguida de una representación ASCII del identificador. El rectángulo se especifica como **X1 Y1 X2 Y2.** Las coordenadas **X1 Y1** especifican la esquina superior izquierda del rectángulo y las coordenadas **X2 Y2** especifican el ancho y el alto.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o ambos. En el caso de los dispositivos de vídeo digital, también se puede especificar "prueba". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="examples"></a>Ejemplos

El comando siguiente actualiza toda la ventana de presentación que usa el dispositivo "movie". El número 203 es un identificador de un controlador de dominio obtenido de la [**función BeginPaint.**](/windows/desktop/api/winuser/nf-winuser-beginpaint)

``` syntax
update movie hdc 203
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Cadenas de comandos de MCI](mci-command-strings.md)
</dt> </dl>

 


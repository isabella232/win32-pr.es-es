---
title: comando UPDATE
description: El comando UPDATE vuelve a dibujar el marco actual en el contexto de dispositivo (DC) especificado. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 51a83262-91d5-4852-ad17-bd62c14417b1
keywords:
- comando actualizar Windows multimedia
topic_type:
- apiref
api_name:
- update
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cb0fc96d404efd8e2f657985ffa5a8861d3b4f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535349"
---
# <a name="update-command"></a>comando UPDATE

El comando UPDATE vuelve a dibujar el marco actual en el contexto de dispositivo (DC) especificado. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

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

Identificador de un controlador de dominio. En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **Update** y las marcas usadas por cada tipo.



| Value        | Significado                       | Significado         |
|--------------|-------------------------------|-----------------|
| digitalvideo | HDC *HDC* HDC *HDC* en *Rect* | pintar HDC *HDC* |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszHDC** y su significado.



| Value               | Significado                                                                                                |
|---------------------|--------------------------------------------------------------------------------------------------------|
| HDC *HDC*           | Especifica el identificador del controlador de dominio que se va a pintar.                                                               |
| HDC *HDC* en *Rect* | Especifica el rectángulo de recorte relativo al rectángulo de cliente.                                     |
| pintar HDC *HDC*     | Pinta el controlador de dominio cuando la aplicación recibe un mensaje de [**\_ dibujo de WM**](/windows/desktop/gdi/wm-paint) diseñado para un controlador de dominio. |



 

Para especificar el identificador del controlador de dominio, use la cadena "HDC" seguida de una representación ASCII del identificador. El rectángulo se especifica como **x1 Y1 x2 Y2**. Las coordenadas **x1 Y1** especifican la esquina superior izquierda del rectángulo y las coordenadas **x2 Y2** especifican el ancho y el alto.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify" o ambos. En el caso de los dispositivos de vídeo digital, también se puede especificar "Test". Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="examples"></a>Ejemplos

El comando siguiente actualiza la ventana de presentación completa utilizada por el dispositivo "Movie". El número 203 es un identificador de un controlador de dominio Obtenido de la función [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) .

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

[Cadenas de comandos MCI](mci-command-strings.md)
</dt> </dl>

 


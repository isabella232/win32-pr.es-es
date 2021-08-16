---
title: comando restore
description: El comando restore copia una imagen fija de un archivo en el búfer de fotogramas. Esto es lo contrario del comando de captura. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: e84a478a-3e0f-4767-94d7-eb3c79c31b8b
keywords:
- comando restore Windows Multimedia
topic_type:
- apiref
api_name:
- restore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55e82fdec2480cfe2fc1b41901872aef7e41ee468d1adc3924df17a27e40031e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689195"
---
# <a name="restore-command"></a>comando restore

El comando restore copia una imagen fija de un archivo en el búfer de fotogramas. Esto es lo contrario del [comando de](capture.md) captura. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("restore %s %s %s"), 
  lpszDeviceID, 
  lpszRestore, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszRestore"></span><span id="lpszrestore"></span><span id="LPSZRESTORE"></span>*lpszRestore*
</dt> <dd>

Una o varias de las marcas siguientes.



| Valor           | Significado                                                                                                                                                                                                                                                                                                                         |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en *rectángulo*  | Especifica un rectángulo relativo al origen del búfer de marco. El *rectángulo* se especifica como *X1 Y1 X2 Y2*. Las coordenadas *X1 Y1 especifican* la esquina superior izquierda y las coordenadas *X2 Y2* especifican el ancho y el alto. Si no se usa esta marca, la imagen se copia en la esquina superior izquierda del búfer de fotogramas.<br/> |
| desde nombre *de archivo* | Especifica el nombre de archivo de la imagen que se recuperará. Esta marca es obligatoria.                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify", "test" o una combinación de estos. Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Comentarios

Los dispositivos pueden reconocer diversos formatos de imagen. un Windows mapa de bits independiente del dispositivo siempre se reconoce.

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
</dt> <dt>

[capturar](capture.md)
</dt> </dl>

 


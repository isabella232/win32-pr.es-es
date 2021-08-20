---
title: comando load
description: El comando load carga un archivo en un formato específico del dispositivo. Los dispositivos de superposición de vídeo y vídeo digital reconocen este comando.
ms.assetid: ae7bfe92-7957-4756-a408-e3ab60dd9aa4
keywords:
- comando load Windows Multimedia
topic_type:
- apiref
api_name:
- load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c66822de727ea45e93839c710dae19739cba8adaac8b571846c1fa23ef0083c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139360"
---
# <a name="load-command"></a>comando load

El comando load carga un archivo en un formato específico del dispositivo. Los dispositivos de superposición de vídeo y vídeo digital reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("load %s %s %s"), 
  lpszDeviceID, 
  lpszFilePos, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszFilePos"></span><span id="lpszfilepos"></span><span id="LPSZFILEPOS"></span>*lpszFilePos*
</dt> <dd>

Ruta de acceso y nombre de archivo que se cargarán. En el caso de los dispositivos de superposición de vídeo, también puede incluir un rectángulo de destino para los datos. Para especificar un rectángulo de destino, especifique "at" seguido de **X1 Y1 X2 Y2**, donde **X1 Y1** especifica la esquina superior izquierda del rectángulo y **X2 Y2** especifica el ancho y el alto. El rectángulo es relativo al origen del búfer de vídeo.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o ambos. En el caso de los dispositivos de vídeo digital, también se puede especificar "prueba". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Comentarios

El dispositivo "vidboard" envía un mensaje de notificación cuando se completa la carga.

## <a name="examples"></a>Ejemplos

El comando siguiente carga un archivo en el dispositivo "vidboard".

``` syntax
load vidboard c:\vid\fish.vid notify
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Cadenas de comandos de MCI](mci-command-strings.md)
</dt> </dl>

 


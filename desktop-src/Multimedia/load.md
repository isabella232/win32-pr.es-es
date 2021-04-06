---
title: comando LOAD
description: El comando LOAD carga un archivo en un formato específico del dispositivo. Los dispositivos de vídeo digital y de superposición reconocen este comando.
ms.assetid: ae7bfe92-7957-4756-a408-e3ab60dd9aa4
keywords:
- comando cargar Windows multimedia
topic_type:
- apiref
api_name:
- load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b199a6d3aea8a2697217eb75176c24b2b0bc2e2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803020"
---
# <a name="load-command"></a>comando LOAD

El comando LOAD carga un archivo en un formato específico del dispositivo. Los dispositivos de vídeo digital y de superposición reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

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

Ruta de acceso y nombre de archivo que se van a cargar. En el caso de los dispositivos de superposición de vídeo, también puede incluir un rectángulo de destino para los datos. Para especificar un rectángulo de destino, especifique "at" seguido de **x1 Y1 x2 Y2**, donde **x1 Y1** especifique la esquina superior izquierda del rectángulo y **x2 Y2** especifique el ancho y el alto. El rectángulo es relativo al origen del búfer de vídeo.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify" o ambos. En el caso de los dispositivos de vídeo digital, también se puede especificar "Test". Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

El dispositivo "vidboard" envía un mensaje de notificación cuando se completa la carga.

## <a name="examples"></a>Ejemplos

El comando siguiente carga un archivo en el dispositivo "vidboard".

``` syntax
load vidboard c:\vid\fish.vid notify
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

 


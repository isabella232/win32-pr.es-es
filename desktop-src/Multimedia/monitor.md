---
title: monitor (comando)
description: El comando monitor especifica el origen de la presentación. (El origen de presentación predeterminado es el área de trabajo). Al cambiar el origen de la presentación, se cambian todas las secuencias de audio y vídeo del origen. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 5cacbe88-b94e-4101-badf-2bb4796b19cf
keywords:
- comando supervisar Windows multimedia
topic_type:
- apiref
api_name:
- monitor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ccbe1d8919c232ab88d04081dad242944868893
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802221"
---
# <a name="monitor-command"></a>monitor (comando)

El comando monitor especifica el origen de la presentación. (El origen de presentación predeterminado es el área de trabajo). Al cambiar el origen de la presentación, se cambian todas las secuencias de audio y vídeo del origen. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("monitor %s %s %s"), 
  lpszDeviceID, 
  lpszMonitor, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszMonitor"></span><span id="lpszmonitor"></span><span id="LPSZMONITOR"></span>*lpszMonitor*
</dt> <dd>

Una o varias de las marcas siguientes.



| Value           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| archivo            | Especifica que el área de trabajo es el origen de la presentación. Este es el origen predeterminado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| input           | Especifica que la entrada externa es el origen de la presentación. Si un comando de [reproducción](play.md) está en curso, se pausa primero. Si [setvideo](setvideo.md) es "ON", esta marca muestra una ventana oculta predeterminada. Los dispositivos pueden limitar lo que pueden hacer otras instancias del dispositivo mientras se supervisa la entrada.                                                                                                                                                                                                                                                                                                                                                                    |
| método *Method* | Cuando se usa con el **monitor** "Input", esta marca selecciona el método de supervisión. El *método* es "pre", "post" o "Direct". La supervisión directa solicita que el dispositivo esté configurado para una calidad de visualización óptima durante la supervisión. El método de supervisión directa podría ser incompatible con la grabación de vídeo de movimiento. La supervisión previa y posterior permite la grabación de vídeo en movimiento. La supervisión previa muestra la entrada externa antes de la compresión, mientras que la supervisión posterior muestra la entrada externa después de la compresión. Normalmente, los distintos métodos de supervisión tienen implicaciones de hardware diferentes. El dispositivo selecciona el método de supervisión predeterminado.<br/> |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify", "Test" o una combinación de estos. Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

El origen de la presentación cambia automáticamente al área de trabajo después de un comando de [reproducción](play.md), [paso](step.md), [pausa](pause.md), [indicación](cue.md) "salida" o [búsqueda](seek.md) . El comando [grabar](record.md) no cambia automáticamente los orígenes de presentación, lo que proporciona a la aplicación la opción de no mostrar vídeo mientras se graba.

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
</dt> <dt>

[indicación](cue.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[reproducción](play.md)
</dt> <dt>

[record](record.md)
</dt> <dt>

[desean](seek.md)
</dt> <dt>

[pasar](step.md)
</dt> </dl>

 


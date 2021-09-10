---
title: comando capture
description: El comando capture copia el contenido del búfer de fotogramas y lo almacena en el archivo especificado. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: cdf177b9-874e-40d8-af3e-59070c55903d
keywords:
- comando capture Windows Multimedia
topic_type:
- apiref
api_name:
- capture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdf5edce248fc5402245e36e869cddc97ba3430a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369836"
---
# <a name="capture-command"></a>comando capture

El comando capture copia el contenido del búfer de fotogramas y lo almacena en el archivo especificado. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capture %s %s %s"), 
  lpszDeviceID, 
  lpszCapture, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszCapture"></span><span id="lpszcapture"></span><span id="LPSZCAPTURE"></span>*lpszCapture*
</dt> <dd>

Una o varias de las marcas siguientes:



| Value          | Significado                                                                                                                                                                                                                                                   |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| como *pathname*  | Especifica la ruta de acceso de destino y el nombre de archivo de la imagen capturada. Esta marca es obligatoria.                                                                                                                                                                |
| en *rectángulo* | Especifica la región rectangular dentro del búfer de fotogramas que el dispositivo recorta y guarda en el disco. Si se omite, la región recortada tiene como valor predeterminado el rectángulo especificado o el valor predeterminado en un comando [put](put.md) "source" anterior para esta instancia de dispositivo. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify", "test" o una combinación de estos. Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Este comando podría producir un error si el dispositivo está reproduciendo vídeo de movimiento o ejecutando alguna otra operación que consume muchos recursos. Si el búfer de fotogramas se actualiza en tiempo real, la actualización se pausa momentáneamente para capturar una imagen completa. Si el dispositivo pausa la actualización, puede haber un efecto visual o similar. Si no se han establecido el formato de archivo, el algoritmo de compresión y los niveles de calidad, se usan sus valores predeterminados.

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
</dt> <dt>

[Poner](put.md)
</dt> </dl>

 


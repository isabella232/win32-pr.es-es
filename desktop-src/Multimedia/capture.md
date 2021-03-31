---
title: comando de captura
description: El comando Capture copia el contenido del búfer de Marcos y lo almacena en el archivo especificado. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: cdf177b9-874e-40d8-af3e-59070c55903d
keywords:
- comando de captura de Windows multimedia
topic_type:
- apiref
api_name:
- capture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdf5edce248fc5402245e36e869cddc97ba3430a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151032"
---
# <a name="capture-command"></a>comando de captura

El comando Capture copia el contenido del búfer de Marcos y lo almacena en el archivo especificado. Los dispositivos de vídeo digital reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

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
| como *nombreruta*  | Especifica la ruta de acceso de destino y el nombre de archivo de la imagen capturada. Esta marca es obligatoria.                                                                                                                                                                |
| en el *rectángulo* | Especifica la región rectangular dentro del búfer de fotogramas que el dispositivo recorta y guarda en el disco. Si se omite, la región recortada tiene como valor predeterminado el rectángulo especificado o predeterminado en un comando [Put](put.md) "Source" anterior para esta instancia de dispositivo. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify", "Test" o una combinación de estos. Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Este comando podría producir un error si el dispositivo está reproduciendo el vídeo de movimiento o ejecuta otra operación que consume muchos recursos. Si el búfer de fotogramas se actualiza en tiempo real, la actualización se pausa momentáneamente para que se capture una imagen completa. Si el dispositivo pone en pausa la actualización, puede haber un efecto visual o audible. Si no se han establecido el formato de archivo, el algoritmo de compresión y los niveles de calidad, se usan los valores predeterminados.

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

[pondrán](put.md)
</dt> </dl>

 


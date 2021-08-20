---
title: Comando mark
description: El comando mark controla la grabación y el borrado de marcas en la cinta de vídeo. Los dispositivos VCR reconocen este comando.
ms.assetid: d5f7a546-dc46-459c-b5dc-0651bca842cb
keywords:
- Comando mark Windows Multimedia
topic_type:
- apiref
api_name:
- mark
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f59f56a6d542120d088d764d1b301329a7f0b167f25952587a9e743878643e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138756"
---
# <a name="mark-command"></a>Comando mark

El comando mark controla la grabación y el borrado de marcas en la cinta de vídeo. Los dispositivos VCR reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("mark %s %s %s"), 
  lpszDeviceID, 
  lpszMark, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszMark"></span><span id="lpszmark"></span><span id="LPSZMARK"></span>*lpszMark*
</dt> <dd>

Una de las marcas siguientes.



| Valor | Significado                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| erase | Borra una marca en la posición actual, si existe una. Para borrar una marca, primero busque la marca y, a continuación, emita el comando mark "erase". |
| escritura | Escribe una marca en la posición actual. Es posible que el VCR tenga que estar en modo de reproducción o registro para que este comando se pueda ejecutar correctamente.                    |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o "test". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Comentarios

Las marcas son señales especiales escritas en el contenido que el VCR puede detectar durante las búsquedas de alta velocidad. Las marcas son específicas de VCR.

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

 


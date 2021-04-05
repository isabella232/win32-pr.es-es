---
title: index (comando)
description: El comando index controla la presentación en pantalla de un VCR. Los dispositivos VCR reconocen este comando.
ms.assetid: 16066acf-37aa-4bff-b97e-5eb2420ac3c4
keywords:
- comando de índice multimedia de Windows
topic_type:
- apiref
api_name:
- index
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da652b1a7a48dffd9850c435345fcfcb11c2e674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997160"
---
# <a name="index-command"></a>index (comando)

El comando index controla la presentación en pantalla de un VCR. Los dispositivos VCR reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("index %s %s %s"), 
  lpszDeviceID, 
  lpszIndex, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszIndex"></span><span id="lpszindex"></span><span id="LPSZINDEX"></span>*lpszIndex*
</dt> <dd>

Una de las marcas siguientes.



| Value | Significado                                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------------------|
| apagado   | Desactiva la presentación en pantalla.                                                                                         |
| on    | Activa la presentación en pantalla. El elemento que se va a mostrar se especifica mediante la marca "índice" del comando [set](set.md) . |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify" o "Test". Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

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

[set](set.md)
</dt> </dl>

 


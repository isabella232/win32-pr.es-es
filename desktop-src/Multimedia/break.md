---
title: comando break
description: El comando break especifica una clave para anular un comando que se invocó mediante \ 0034;wait \ 0034; Bandera. Este comando es un comando del sistema MCI; MCI la interpreta directamente.
ms.assetid: 959df85f-5020-4e37-952b-15ba5e6fb672
keywords:
- comando break Windows Multimedia
topic_type:
- apiref
api_name:
- break
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f727fb6cf375e09a260ee68f62eac83816ff5d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062933"
---
# <a name="break-command"></a>comando break

El comando break especifica una clave para anular un comando que se invocó mediante la marca "wait". Este comando es un comando del sistema MCI; MCI la interpreta directamente.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("break %s %s %s"), 
  lpszDeviceID, 
  lpszVirtKey, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszVirtKey"></span><span id="lpszvirtkey"></span><span id="LPSZVIRTKEY"></span>*lpszVirtKey*
</dt> <dd>

Una de las marcas siguientes.



| Value                 | Significado                                                                         |
|-----------------------|---------------------------------------------------------------------------------|
| en *el código de clave virtual* | Especifica la clave que anula un comando que se inició con la marca "wait". |
| apagado                   | Deshabilita la clave de interrupción actual.                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o ambos. En el caso de los dispositivos de vídeo digital y VCR, también se puede especificar "prueba". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Cuando la tecla de interrupción está habilitada y el usuario presiona la tecla identificada por el código de clave virtual especificado en el parámetro *lpszVirtKey,* el dispositivo devuelve el control a la aplicación. Si es posible, el comando continúa la ejecución.

## <a name="examples"></a>Ejemplos

El comando siguiente establece F2 como clave de interrupción para el dispositivo "my sound".

``` syntax
break mysound on 113
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Cadenas de comandos de MCI](mci-command-strings.md)
</dt> </dl>

 


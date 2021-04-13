---
title: Break (comando)
description: El comando break especifica una clave para anular un comando que se invocó mediante \ 0034; wait \ 0034; marcas. Este comando es un comando del sistema MCI; lo interpreta directamente MCI.
ms.assetid: 959df85f-5020-4e37-952b-15ba5e6fb672
keywords:
- comando interrumpir Windows multimedia
topic_type:
- apiref
api_name:
- break
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f727fb6cf375e09a260ee68f62eac83816ff5d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492826"
---
# <a name="break-command"></a>Break (comando)

El comando break especifica una clave para anular un comando que se invocó mediante la marca "Wait". Este comando es un comando del sistema MCI; lo interpreta directamente MCI.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

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
| en *código de tecla virtual* | Especifica la clave que anula un comando que se inició con la marca "Wait". |
| apagado                   | Deshabilita la clave de interrupción actual.                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify" o ambos. En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba". Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Cuando la tecla interrumpir está habilitada y el usuario presiona la clave identificada por el código de clave virtual especificado en el parámetro *lpszVirtKey* , el dispositivo devuelve el control a la aplicación. Si es posible, el comando continúa la ejecución.

## <a name="examples"></a>Ejemplos

El siguiente comando establece F2 como tecla de interrupción para el dispositivo "de".

``` syntax
break mysound on 113
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

 


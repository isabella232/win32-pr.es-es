---
description: El método resume reinicia una captura en pausa.
ms.assetid: 685dfdee-3bd0-44b3-ac4f-c9960cf77c5c
title: 'IRTC:: resume (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 991f70944b44ce13641318219788d9d6122b15c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677645"
---
# <a name="irtcresume-method"></a>IRTC:: resume (método)

El método **resume** reinicia una captura en pausa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                                | Descripción                                                                                                                   |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**la captura de NMERR no está en \_ \_ \_ pausa**</dt> </dl> | La captura no está en pausa. Llame a [IRTC::P ause](irtc-pause.md) para pausar la captura.<br/>                                |
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl>       | NPP no está conectado a la red. Llame a [IRTC:: Connect](irtc-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ no es en \_ tiempo real**</dt> </dl>        | NPP está conectado a la red, pero no con el método [IRTC:: Connect](irtc-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Observaciones

Mientras la captura está en un estado de pausa, los nuevos datos no se capturan hasta que una llamada al método [IRTC:: resume](idelaydc-resume.md) reinicie la captura.

Al usar los métodos **pausar** y **reanudar** para controlar la captura, monitor de red continúa agregando [*estadísticas de conversación*](c.md) a las estadísticas existentes para la captura actual.

Para detener la captura, llame al método [IRTC:: Stop](irtc-stop.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC:: Connect](irtc-connect.md)
</dt> <dt>

[IRTC::P ause](irtc-pause.md)
</dt> <dt>

[IRTC:: Stop](irtc-stop.md)
</dt> </dl>

 

 





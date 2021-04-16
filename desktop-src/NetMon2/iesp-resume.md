---
description: El método resume reinicia una captura en pausa.
ms.assetid: 047ea5f8-de3d-40db-ada3-fc0ef4deccef
title: 'IESP:: resume (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 01bbb748fc91bcc5a78b281ec9ebdd2a6d479888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686557"
---
# <a name="iespresume-method"></a>IESP:: resume (método)

El método **resume** reinicia una captura en pausa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                                | Descripción                                                                                                               |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**la captura de NMERR no está en \_ \_ \_ pausa**</dt> </dl> | La captura no está en pausa. Llame a [**iesp::P ause**](iesp-pause.md) para pausar la captura.<br/>                        |
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl>       | NPP no está conectado a la red. Llame a [**iesp:: Connect**](iesp-connect.md) para conectarse a la red.<br/> |
| <dl> <dt>**NMERR \_ no \_ ESP**</dt> </dl>             | NPP está conectado a la red, pero no con el método [**iesp:: Connect**](iesp-connect.md) .<br/>            |



 

## <a name="remarks"></a>Observaciones

Mientras la captura está en un estado de pausa, los datos nuevos no se agregan al [*archivo de captura*](c.md) actual hasta que se llama a **iesp:: resume** para reiniciar la captura. Cuando se usan **pausar** y **reanudar** para detener y reiniciar la captura, toda la información capturada se coloca en el mismo archivo de captura.

Al usar **pausar** y **reanudar** para controlar la captura, monitor de red continúa agregando [*estadísticas de conversación*](c.md) a las estadísticas existentes para la captura actual.

Para detener la captura, llame a [**iesp:: Stop**](iesp-stop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[**IESP:: Connect**](iesp-connect.md)
</dt> <dt>

[**IESP::P ause**](iesp-pause.md)
</dt> <dt>

[**IESP:: Stop**](iesp-stop.md)
</dt> </dl>

 

 





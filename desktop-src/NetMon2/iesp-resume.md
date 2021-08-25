---
description: 'Método IESP::Resume: el método Resume reinicia una captura en pausa.'
ms.assetid: 047ea5f8-de3d-40db-ada3-fc0ef4deccef
title: Método IESP::Resume (Netmon.h)
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
ms.openlocfilehash: dd39cb83c90c566f0022679e70680e916daeb2a43a4d62e993e096930ee2f14e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890475"
---
# <a name="iespresume-method"></a>IESP::Resume (método)

El **método Resume** reinicia una captura en pausa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                                | Descripción                                                                                                               |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CAPTURA DE NMERR \_ \_ NO EN \_ PAUSA**</dt> </dl> | La captura no está en pausa. Llame [**a IESP::P ause para**](iesp-pause.md) pausar la captura.<br/>                        |
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl>       | El NPP no está conectado a la red. Llame [**a IESP::Conectar**](iesp-connect.md) para conectarse a la red.<br/> |
| <dl> <dt>**NMERR \_ NOT \_ ESP**</dt> </dl>             | El NPP está conectado a la red, pero no con el [**método IESP::Conectar.**](iesp-connect.md)<br/>            |



 

## <a name="remarks"></a>Comentarios

Mientras la captura está en estado en pausa, no [](c.md) se agregan nuevos datos al archivo de captura actual hasta que se llama a **IESP::Resume** para reiniciar la captura. Cuando **se** usan **Pausar y reanudar** para detener y reiniciar la captura, toda la información capturada se coloca en el mismo archivo de captura.

Al usar **Pausar** **y reanudar** para controlar la captura, Monitor de red continúa agregando estadísticas de conversación a las [*estadísticas*](c.md) existentes para la captura actual.

Para detener la captura, llame a [**IESP::Stop**](iesp-stop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[**IESP::Conectar**](iesp-connect.md)
</dt> <dt>

[**IESP::P ause**](iesp-pause.md)
</dt> <dt>

[**IESP::Stop**](iesp-stop.md)
</dt> </dl>

 

 





---
description: 'Método IRTC::Resume: el método Resume reinicia una captura en pausa.'
ms.assetid: 685dfdee-3bd0-44b3-ac4f-c9960cf77c5c
title: Método IRTC::Resume (Netmon.h)
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
ms.openlocfilehash: f8b8cebaf14f5e6a42a938a8fe585934137a899f8afaeb2d28533c0c0cfa18b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742985"
---
# <a name="irtcresume-method"></a>IRTC::Resume (método)

El **método Resume** reinicia una captura en pausa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                                | Descripción                                                                                                                   |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CAPTURA DE NMERR \_ \_ NO \_ PAUSADA**</dt> </dl> | La captura no está en pausa. Llame [a IRTC::P ause para](irtc-pause.md) pausar la captura.<br/>                                |
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl>       | El NPP no está conectado a la red. Llame [a IRTC::Conectar](irtc-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ NOT \_ REALTIME**</dt> </dl>        | El NPP está conectado a la red, pero no con el [método IRTC::Conectar.](irtc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Comentarios

Mientras la captura está en estado en pausa, los nuevos datos no se capturan hasta que una llamada al método [IRTC::Resume](idelaydc-resume.md) reinicia la captura.

Al usar los  **métodos Pausar** y Reanudar para controlar la captura, Monitor de red sigue agregando [*estadísticas*](c.md) de conversación a las estadísticas existentes para la captura actual.

Para detener la captura, llame al [método IRTC::Stop.](irtc-stop.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Conectar](irtc-connect.md)
</dt> <dt>

[IRTC::P ause](irtc-pause.md)
</dt> <dt>

[IRTC::Stop](irtc-stop.md)
</dt> </dl>

 

 





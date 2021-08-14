---
description: 'Método IRTC::P ause: el método Pause pausa la captura actual.'
ms.assetid: 8c7b310e-de04-4bd8-9c96-3c5948e610be
title: Método IRTC::P ause (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1ad7ce342c1e0053622bfb77161ecd1e5d81c25d09af179108065b445dd4dc35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365080"
---
# <a name="irtcpause-method"></a>IRTC::P ause (método)

El **método Pause** pausa la captura actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                           | Descripción                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CAPTURA DE NMERR \_ \_ EN PAUSA**</dt> </dl> | La captura ya está en pausa.<br/>                                                                                     |
| <dl> <dt>**NMERR \_ NO \_ CAPTURA**</dt> </dl>  | El NPP no captura datos. Llame [a IRTC::Start](irtc-start.md) para iniciar la captura.<br/>                            |
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl>  | El NPP no está conectado a la red. Llame [a IRTC::Conectar](irtc-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ NOT \_ REALTIME**</dt> </dl>   | El NPP está conectado a la red, pero no con el [método IRTC::Conectar.](irtc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Comentarios

Mientras la captura está en estado en pausa, no se capturan nuevos fotogramas hasta que se llama al método [IRTC::Resume](irtc-resume.md) para reiniciar la captura.

Cuando usa los métodos **IRTC::P ause** e **IRTC::Resume** para controlar la captura, Monitor de red continúa agregando [*estadísticas*](c.md) de conversación cada vez que se ejecuta la captura.

Para reiniciar la llamada de captura [IRTC::Resume](irtc-resume.md). Para detener la captura, llame [a IRTC::Stop](irtc-stop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Conectar](irtc-connect.md)
</dt> <dt>

[IRTC::Resume](irtc-resume.md)
</dt> <dt>

[IRTC::Start](irtc-start.md)
</dt> <dt>

[IRTC::Stop](irtc-stop.md)
</dt> </dl>

 

 





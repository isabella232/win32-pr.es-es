---
description: El método resume reinicia una captura en pausa.
ms.assetid: 4fa47220-d323-407b-9dae-704969f66bdd
title: 'IDelaydC:: resume (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ba0deef666c2e9829cb5a71d91e73da9c1b7d780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808695"
---
# <a name="idelaydcresume-method"></a>IDelaydC:: resume (método)

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



| Código devuelto                                                                                                | Descripción                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**la captura de NMERR no está en \_ \_ \_ pausa**</dt> </dl> | La captura no está en pausa. Llame a [**IDelaydC::P ause**](idelaydc-pause.md) para pausar la captura.<br/>                                |
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl>       | NPP no está conectado a la red. Llame a [**IDelaydC:: Connect**](idelaydc-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ no \_ retrasado**</dt> </dl>         | NPP está conectado a la red, pero no con el método [**IDelaydC:: Connect**](idelaydc-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Observaciones

Mientras se pausa la captura, los nuevos datos no se agregan al [*archivo de captura*](c.md) actual hasta que se llama al método **IDelaydC:: resume** para reiniciar la captura. Cuando se usan [**pausar**](idelaydc-pause.md) y **reanudar** para detener y reiniciar la captura, toda la información capturada se coloca en el mismo archivo de captura.

Al usar [**pausar**](idelaydc-pause.md) y **reanudar** para controlar la captura, monitor de red continúa agregando [*estadísticas de conversación*](c.md) a las estadísticas existentes para la captura actual.

Para detener la captura, llame a [**IDelaydC:: Stop**](idelaydc-stop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[**IDelaydC:: Connect**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC::P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC:: Stop**](idelaydc-stop.md)
</dt> </dl>

 

 





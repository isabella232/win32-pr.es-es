---
description: 'IDelaydC::P ause: el método Pause pausa la captura actual.'
ms.assetid: 9d5e11d1-8c45-4cf5-9fea-10c9e7a6fe86
title: Método IDelaydC::P ause (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: dfe48afce1e8fd2350f1d1b696eb426a326ade1b30151e872afee30c0ed997f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910515"
---
# <a name="idelaydcpause-method"></a>IDelaydC::P ause (método)

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



| Código devuelto                                                                                           | Descripción                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CAPTURA DE NMERR \_ \_ EN PAUSA**</dt> </dl> | La captura ya está en estado en pausa.<br/>                                                                                  |
| <dl> <dt>**NMERR \_ NO \_ CAPTURA**</dt> </dl>  | El NPP no captura datos. Llame [a IDelaydC::Start para](idelaydc-start.md) iniciar la captura.<br/>                            |
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl>  | El NPP no está conectado a la red. Llame [a IDelaydC::Conectar](idelaydc-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ NO \_ RETRASADO**</dt> </dl>    | El NPP está conectado a la red, pero no con [el método IDelaydC::Conectar.](idelaydc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Comentarios

Mientras la captura está en estado en pausa, no [](c.md) se agregan nuevos datos al archivo de captura actual hasta que se llama al método **IDelaydC::Resume** para reiniciar la captura. Cuando **se** usan **Pausar y reanudar** para detener y reiniciar la captura, toda la información capturada se coloca en el mismo archivo de captura.

Al usar **IDelaydC::P ause** e **IDelaydC::Resume** para controlar la captura, Monitor de red continúa agregando [*estadísticas*](c.md) de conversación cada vez que se ejecuta la captura.

Para reiniciar la captura, llame a [IDelaydC::Resume](idelaydc-resume.md).

Para detener la captura, llame a [IDelaydC::Stop](idelaydc-stop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC::Conectar](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::Resume](idelaydc-resume.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> <dt>

[IDelaydC::Stop](idelaydc-stop.md)
</dt> </dl>

 

 





---
description: El método PAUSE pausa la captura actual.
ms.assetid: 9d5e11d1-8c45-4cf5-9fea-10c9e7a6fe86
title: IDelaydC::P método ause (Netmon. h)
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
ms.openlocfilehash: d44ae7792388d9ca637232b45e63d618a37acb6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907663"
---
# <a name="idelaydcpause-method"></a>IDelaydC::P método ause

El método **PAUSE pausa** la captura actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                           | Descripción                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR en \_ \_ pausa**</dt> </dl> | La captura ya está en un estado de pausa.<br/>                                                                                  |
| <dl> <dt>**NMERR \_ no se \_ captura**</dt> </dl>  | NPP no está capturando datos. Llame a [IDelaydC:: Start](idelaydc-start.md) para iniciar la captura.<br/>                            |
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl>  | NPP no está conectado a la red. Llame a [IDelaydC:: Connect](idelaydc-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ no \_ retrasado**</dt> </dl>    | NPP está conectado a la red, pero no con el método [IDelaydC:: Connect](idelaydc-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Observaciones

Mientras la captura está en un estado de pausa, los datos nuevos no se agregan al [*archivo de captura*](c.md) actual hasta que se llama al método **IDelaydC:: resume** para reiniciar la captura. Cuando se usan **pausar** y **reanudar** para detener y reiniciar la captura, toda la información capturada se coloca en el mismo archivo de captura.

Al usar **IDelaydC::P ause** y **IDelaydC:: resume** para controlar la captura, monitor de red continúa agregando [*estadísticas de conversación*](c.md) cada vez que se ejecuta la captura.

Para reiniciar la captura, llame a [IDelaydC:: resume](idelaydc-resume.md).

Para detener la captura, llame a [IDelaydC:: Stop](idelaydc-stop.md).

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

[IDelaydC:: Connect](idelaydc-connect.md)
</dt> <dt>

[IDelaydC:: resume](idelaydc-resume.md)
</dt> <dt>

[IDelaydC:: Start](idelaydc-start.md)
</dt> <dt>

[IDelaydC:: Stop](idelaydc-stop.md)
</dt> </dl>

 

 





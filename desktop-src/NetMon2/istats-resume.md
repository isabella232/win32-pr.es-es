---
description: El método resume reinicia una captura en pausa.
ms.assetid: 128e38c4-7459-4376-a3d7-2c6944fcf535
title: 'IStas:: resume (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: db84f51d2a2a2c2d15e3b4164fe1fac09e72bf20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911638"
---
# <a name="istatsresume-method"></a>IStas:: resume (método)

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



| Código devuelto                                                                                                | Descripción                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl>       | NPP no está conectado a la red.<br/>                                                                                          |
| <dl> <dt>**la captura de NMERR no está en \_ \_ \_ pausa**</dt> </dl> | La captura no está en pausa. Llame al método [istas::P ause](istats-pause.md) para detener temporalmente la captura.<br/>                     |
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl>       | NPP no está conectado a la red. Llame al método [istas:: Connect](istats-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ no \_ solo estadísticas \_**</dt> </dl>     | NPP está conectado a la red, pero no con el método [istas:: Connect](istats-connect.md) .<br/>                                |



 

## <a name="remarks"></a>Observaciones

Mientras la captura está en un estado de pausa, los nuevos datos no se capturan hasta que se llama al método IStas:: resume para reiniciar la captura.

Al usar los métodos **pausar** y **reanudar** para controlar la captura, monitor de red continúa agregando [*estadísticas de conversación*](c.md) a las estadísticas existentes para la captura actual.

Para detener la captura, llame a [istas:: Stop](istats-stop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IStas](istats.md)
</dt> <dt>

[ISta:: Connect](istats-connect.md)
</dt> <dt>

[IStas::P ause](istats-pause.md)
</dt> <dt>

[IStas:: Stop](istats-stop.md)
</dt> </dl>

 

 





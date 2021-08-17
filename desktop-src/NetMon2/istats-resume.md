---
description: 'Método IStats::Resume: el método Resume reinicia una captura en pausa.'
ms.assetid: 128e38c4-7459-4376-a3d7-2c6944fcf535
title: Método IStats::Resume (Netmon.h)
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
ms.openlocfilehash: 72c73107ea4bf4662d4251a7c9e06ed1844feca88cb0ce6700887e65f6f08021
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063825"
---
# <a name="istatsresume-method"></a>IStats::Resume (método)

El **método Resume** reinicia una captura en pausa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                                | Descripción                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl>       | El NPP no está conectado a la red.<br/>                                                                                          |
| <dl> <dt>**CAPTURA DE NMERR \_ \_ NO \_ PAUSADA**</dt> </dl> | La captura no está en pausa. Llame al [método IStats::P ause](istats-pause.md) para detener temporalmente la captura.<br/>                     |
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl>       | El NPP no está conectado a la red. Llame al [método IStats::Conectar](istats-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ NO \_ SOLO \_ ESTADÍSTICAS**</dt> </dl>     | El NPP está conectado a la red, pero no con el [método IStats::Conectar.](istats-connect.md)<br/>                                |



 

## <a name="remarks"></a>Comentarios

Mientras la captura está en estado en pausa, no se capturan nuevos datos hasta que se llama al método IStats::Resume para reiniciar la captura.

Al usar los  **métodos Pausar** y Reanudar para controlar la captura, Monitor de red sigue agregando [*estadísticas*](c.md) de conversación a las estadísticas existentes para la captura actual.

Para detener la captura, llame a [IStats::Stop](istats-stop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats::Conectar](istats-connect.md)
</dt> <dt>

[IStats::P ause](istats-pause.md)
</dt> <dt>

[IStats::Stop](istats-stop.md)
</dt> </dl>

 

 





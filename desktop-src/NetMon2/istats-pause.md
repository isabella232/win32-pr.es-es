---
description: El método Pause detiene temporalmente la captura actual.
ms.assetid: 43176e9e-1502-484c-a8af-4e7bbf5f6474
title: Método IStats::P ause (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d9e9f04ce3d25399866c711dad7a853f2c43c2ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071543"
---
# <a name="istatspause-method"></a>IStats::P ause (método)

El **método Pause** detiene temporalmente la captura actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                            | Descripción                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CAPTURA DE NMERR \_ \_ EN PAUSA**</dt> </dl>  | La captura ya está en pausa.<br/>                                                                                                    |
| <dl> <dt>**NMERR \_ NO \_ CAPTURA**</dt> </dl>   | El NPP no captura datos. Llame al [método IStats::Start](istats-start.md) para iniciar la captura.<br/>                            |
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl>   | El NPP no está conectado a la red. Llame al [método IStats::Conectar](istats-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ NO \_ SOLO \_ ESTADÍSTICAS**</dt> </dl> | El NPP está conectado a la red, pero no con el [método IStats::Conectar.](istats-connect.md)<br/>                                |



 

## <a name="remarks"></a>Observaciones

Mientras la captura está en pausa, los fotogramas nuevos no se capturan hasta que una llamada al método [IStats::Resume](istats-resume.md) reinicia la captura.

Cuando se usan los **métodos IStats::P ause** e **IStats::Resume** para controlar la captura, Monitor de red continúa agregando [*estadísticas*](c.md) de conversación cada vez que se ejecuta la captura.

Para reiniciar la llamada de [captura, llame a IStats::Resume.](istats-resume.md) Para detener la captura, llame a [IStats::Stop](istats-stop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats::Conectar](istats-connect.md)
</dt> <dt>

[IStats::Resume](istats-resume.md)
</dt> <dt>

[IStats::Start](istats-start.md)
</dt> <dt>

[IStats::Stop](istats-stop.md)
</dt> </dl>

 

 





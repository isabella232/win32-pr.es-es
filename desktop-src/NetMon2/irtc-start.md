---
description: El método Start inicia la captura.
ms.assetid: 1f676e19-18ff-4c34-a83f-2723ff356be2
title: Método IRTC::Start (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 3ee30112baf7813c983230fb90cd15ea7f52e2bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074116"
---
# <a name="irtcstart-method"></a>IRTC::Start (método)

El **método Start** inicia la captura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                           | Descripción                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CAPTURA DE NMERR \_ \_ EN PAUSA**</dt> </dl> | La captura está en estado en pausa y debe detenerse antes de poder reiniciarse. Llame [a IRTC::Stop](idelaydc-stop.md) para detener la captura.<br/> |
| <dl> <dt>**CAPTURA DE \_ NMERR**</dt> </dl>       | La captura ya se ha iniciado.<br/>                                                                                                            |
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl>  | El NPP no está conectado a la red. Llame [a IRTC::Conectar](irtc-connect.md) para conectar el NPP a la red.<br/>                         |
| <dl> <dt>**NMERR \_ NOT \_ REALTIME**</dt> </dl>   | El NPP está conectado a la red, pero no con el [método IRTC::Conectar.](irtc-connect.md)<br/>                                             |



 

## <a name="remarks"></a>Observaciones

Al reiniciar la captura mediante los métodos IRTC::Start e [IRTC::Stop,](irtc-stop.md) debe llamar al método [IRTC::Configure](irtc-configure.md) para volver a configurar la conexión cada vez que llame a IRTC::Start para reiniciar la captura de datos.

> [!Note]  
> También puede iniciar y detener la captura mediante los métodos [IRTC::P ause](irtc-pause.md) [e IRTC::Resume.](irtc-resume.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Configure](irtc-configure.md)
</dt> <dt>

[IRTC::Conectar](irtc-connect.md)
</dt> <dt>

[IRTC::P ause](irtc-pause.md)
</dt> <dt>

[IRTC::Resume](irtc-resume.md)
</dt> <dt>

[IRTC::Stop](irtc-stop.md)
</dt> </dl>

 

 





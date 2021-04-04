---
description: El método start inicia la captura.
ms.assetid: 1f676e19-18ff-4c34-a83f-2723ff356be2
title: 'IRTC:: Start (método) (Netmon. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908698"
---
# <a name="irtcstart-method"></a>IRTC:: Start (método)

El método **Start** inicia la captura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                           | Descripción                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR en \_ \_ pausa**</dt> </dl> | La captura está en un estado de pausa y debe detenerse antes de que se pueda reiniciar. Llame a [IRTC:: Stop](idelaydc-stop.md) para detener la captura.<br/> |
| <dl> <dt>**captura de NMERR \_**</dt> </dl>       | La captura ya se ha iniciado.<br/>                                                                                                            |
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl>  | NPP no está conectado a la red. Llame a [IRTC:: Connect](irtc-connect.md) para conectar el NPP a la red.<br/>                         |
| <dl> <dt>**NMERR \_ no es en \_ tiempo real**</dt> </dl>   | NPP está conectado a la red, pero no con el método [IRTC:: Connect](irtc-connect.md) .<br/>                                             |



 

## <a name="remarks"></a>Observaciones

Cuando reinicie la captura mediante los métodos IRTC:: Start y [IRTC:: Stop](irtc-stop.md) , debe llamar al método [IRTC:: configure](irtc-configure.md) para volver a configurar la conexión cada vez que llame a IRTC:: Start para reiniciar la captura de datos.

> [!Note]  
> También puede iniciar y detener la captura mediante los métodos [IRTC::P ause](irtc-pause.md) y [IRTC:: resume](irtc-resume.md) .

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC:: configure](irtc-configure.md)
</dt> <dt>

[IRTC:: Connect](irtc-connect.md)
</dt> <dt>

[IRTC::P ause](irtc-pause.md)
</dt> <dt>

[IRTC:: resume](irtc-resume.md)
</dt> <dt>

[IRTC:: Stop](irtc-stop.md)
</dt> </dl>

 

 





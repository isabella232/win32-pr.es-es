---
description: El método start inicia una captura.
ms.assetid: d4086e30-e5ed-4f29-90f0-d65125d9af6d
title: 'IStas:: Start (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d58821ecc06e0a25d6a260bb2ba9393162dcdca8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908183"
---
# <a name="istatsstart-method"></a>IStas:: Start (método)

El método **Start** inicia una captura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                            | Descripción                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR en \_ \_ pausa**</dt> </dl>  | La captura se ha pausado y debe detenerse antes de que se pueda reiniciar. Llame al método [istas:: Stop](istats-stop.md) para detener la captura.<br/> |
| <dl> <dt>**captura de NMERR \_**</dt> </dl>        | La captura ya se ha iniciado.<br/>                                                                                                            |
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl>   | NPP no está conectado a la red. Llame al método [istas:: Connect](istats-connect.md) para conectar el NPP a la red.<br/>           |
| <dl> <dt>**NMERR \_ no \_ solo estadísticas \_**</dt> </dl> | NPP está conectado a la red, pero no con el método [istas:: Connect](istats-connect.md) .<br/>                                          |



 

## <a name="remarks"></a>Observaciones

Al reiniciar la captura mediante los métodos IStas:: Start y [istas:: Stop](istats-stop.md) , debe llamar al método [istas:: configure](istats-configure.md) para volver a configurar la conexión cada vez que llame a los ISTA:: Start para reiniciar la captura de datos.

> [!Note]  
> También puede iniciar y detener la captura mediante los [istas::P ause](istats-pause.md) y [istas:: resume](istats-resume.md) (métodos). Cuando se usan estos métodos, los datos capturados se almacenan en el mismo archivo de captura.

 

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

[ISta:: configurar](istats-configure.md)
</dt> <dt>

[ISta:: Connect](istats-connect.md)
</dt> <dt>

[IStas::P ause](istats-pause.md)
</dt> <dt>

[IStas:: resume](istats-resume.md)
</dt> <dt>

[IStas:: Stop](istats-stop.md)
</dt> </dl>

 

 





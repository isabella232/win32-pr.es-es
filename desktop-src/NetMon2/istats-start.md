---
description: 'Método IStats::Start: el método Start inicia una captura.'
ms.assetid: d4086e30-e5ed-4f29-90f0-d65125d9af6d
title: Método IStats::Start (Netmon.h)
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
ms.openlocfilehash: 64f02529ba10d98092eb30a1bcc350d5c72049fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071535"
---
# <a name="istatsstart-method"></a>IStats::Start (método)

El **método Start** inicia una captura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                            | Descripción                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CAPTURA DE NMERR \_ \_ EN PAUSA**</dt> </dl>  | La captura se ha pausado y debe detenerse antes de poder reiniciarse. Llame al [método IStats::Stop](istats-stop.md) para detener la captura.<br/> |
| <dl> <dt>**CAPTURA DE \_ NMERR**</dt> </dl>        | La captura ya se ha iniciado.<br/>                                                                                                            |
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl>   | El NPP no está conectado a la red. Llame al [método IStats::Conectar](istats-connect.md) para conectar el NPP a la red.<br/>           |
| <dl> <dt>**NMERR \_ NO \_ SOLO \_ ESTADÍSTICAS**</dt> </dl> | El NPP está conectado a la red, pero no con el [método IStats::Conectar.](istats-connect.md)<br/>                                          |



 

## <a name="remarks"></a>Observaciones

Al reiniciar la captura mediante los métodos IStats::Start e [IStats::Stop,](istats-stop.md) debe llamar al método [IStats::Configure](istats-configure.md) para volver a configurar la conexión cada vez que llame a IStats::Start para reiniciar la captura de datos.

> [!Note]  
> También puede iniciar y detener la captura mediante los [métodos IStats::P ause](istats-pause.md) [e IStats::Resume.](istats-resume.md) Cuando se usan estos métodos, los datos capturados se almacenan en el mismo archivo de captura.

 

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

[IStats::Configure](istats-configure.md)
</dt> <dt>

[IStats::Conectar](istats-connect.md)
</dt> <dt>

[IStats::P ause](istats-pause.md)
</dt> <dt>

[IStats::Resume](istats-resume.md)
</dt> <dt>

[IStats::Stop](istats-stop.md)
</dt> </dl>

 

 





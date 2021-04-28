---
description: 'Método IStats::GetControlState: el método GetControlState recupera el estado de la captura, lo que indica si la captura se está ejecutando o en pausa.'
ms.assetid: 0faf2300-d9ff-4fe0-9d50-18beafd1daea
title: Método IStats::GetControlState (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 25532293335756a872ef5104d5eef66027fe2ae4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098473"
---
# <a name="istatsgetcontrolstate-method"></a>IStats::GetControlState (método)

El **método GetControlState** recupera el estado de [*la*](c.md)captura , lo que indica si la captura se está ejecutando o en pausa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IsRunnning* \[ out\]
</dt> <dd>

Indicador de que la captura actual se está ejecutando, incluido si la captura está en pausa.

</dd> <dt>

*IsPaused* \[ out\]
</dt> <dd>

Indicador de que la captura actual está en pausa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                            | Descripción                                                                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl>   | El NPP no está conectado a la red. Llame [a IStats::Connect](istats-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ NO SOLO \_ \_ ESTADÍSTICAS**</dt> </dl> | El NPP está conectado a la red, pero no con el [método IStats::Connect.](istats-connect.md)<br/>                     |



 

## <a name="remarks"></a>Comentarios

Se puede llamar a este método cada vez que el NPP está conectado a la red. Puede usar este método para averiguar si se está ejecutando una captura, si la captura está en pausa o si la captura se ha detenido pero el NPP no está desconectado.

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

[IStats::Connect](istats-connect.md)
</dt> <dt>

[IStats::P ause](istats-pause.md)
</dt> <dt>

[IStatsC::Start](istats-start.md)
</dt> <dt>

[IStatsC::Stop](istats-stop.md)
</dt> </dl>

 

 





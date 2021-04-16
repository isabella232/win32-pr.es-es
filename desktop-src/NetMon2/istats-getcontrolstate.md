---
description: El método GetControlState recupera el estado de la captura, que indica si la captura se está ejecutando o está en pausa.
ms.assetid: 0faf2300-d9ff-4fe0-9d50-18beafd1daea
title: 'IStas:: GetControlState (método) (Netmon. h)'
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
ms.openlocfilehash: a83b5d20461b28b7022bfdc3ddbf3d5d92149c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689562"
---
# <a name="istatsgetcontrolstate-method"></a>IStas:: GetControlState (método)

El método **GetControlState** recupera el estado de la [*captura*](c.md), que indica si la captura se está ejecutando o está en pausa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IsRunnning* \[ enuncia\]
</dt> <dd>

Indicador de que la captura actual se está ejecutando, incluido si la captura está en pausa.

</dd> <dt>

*IsPaused* \[ enuncia\]
</dt> <dd>

Indicador de que la captura actual está en pausa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                            | Descripción                                                                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl>   | NPP no está conectado a la red. Llame a los [istas:: Connect](istats-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ no \_ solo estadísticas \_**</dt> </dl> | NPP está conectado a la red, pero no con el método [istas:: Connect](istats-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Observaciones

Se puede llamar a este método cada vez que el NPP esté conectado a la red. Puede usar este método para averiguar si se está ejecutando una captura, si la captura está en pausa, o si se ha detenido la captura pero el NPP no está desconectado.

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

[IStatsC:: Start](istats-start.md)
</dt> <dt>

[IStatsC:: Stop](istats-stop.md)
</dt> </dl>

 

 





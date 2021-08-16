---
description: 'Método IDelaydC::GetControlState: el método GetControlState recupera el estado de la captura, que indica si la captura se está ejecutando o en pausa.'
ms.assetid: 21b7faaa-591f-4e15-b4e9-453ea690ab4a
title: Método IDelaydC::GetControlState (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 34302215cf0e773d7713f56233d38462071f1dde725a85478688cfb9ca2a4f45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365898"
---
# <a name="idelaydcgetcontrolstate-method"></a>IDelaydC::GetControlState (método)

El **método GetControlState** recupera el estado de [*la*](c.md)captura , que indica si la captura se está ejecutando o en pausa.

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

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                          | Descripción                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl> | El NPP no está conectado a la red. Llame [a IDelaydC::Conectar](idelaydc-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ NO \_ RETRASADA**</dt> </dl>   | El NPP está conectado a la red, pero no con [el método IDelaydC::Conectar.](idelaydc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Comentarios

Se puede llamar a este método cada vez que el NPP se conecta a la red mediante la [interfaz IDelaydC.](idelaydc.md) Puede usar este método para averiguar si se está ejecutando una captura, si la captura está en pausa o si la captura se ha detenido pero el NPP no está desconectado.

Los métodos usados para iniciar, pausar y detener la captura se enumeran en la lista Vea también a continuación.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC::Conectar](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::P ause](idelaydc-pause.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> <dt>

[IDelaydC::Stop](idelaydc-stop.md)
</dt> </dl>

 

 





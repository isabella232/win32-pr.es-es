---
description: 'Método IESP::GetControlState: el método GetControlState recupera el estado de la captura, lo que indica si la captura se está ejecutando o en pausa.'
ms.assetid: 19cc3095-3aa3-4482-95f5-959b19f76cea
title: Método IESP::GetControlState (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 8ef791d4d892713c9bd07a693b9aa57651e2e7cf75635a1c8642ceb4a45b0776
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779205"
---
# <a name="iespgetcontrolstate-method"></a>IESP::GetControlState (método)

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



| Código devuelto                                                                                          | Descripción                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl> | El NPP no está conectado a la red. Llame [a IESP::Conectar](iesp-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ NOT \_ ESP**</dt> </dl>       | El NPP está conectado a la red, pero no con el [método IESP::Conectar.](iesp-connect.md)<br/>                     |



 

## <a name="remarks"></a>Comentarios

Se puede llamar a este método cada vez que el NPP está conectado a la red. Puede usar este método para averiguar si se está ejecutando una captura, si la captura está en pausa o si la captura se ha detenido pero el NPP todavía está conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[IESP::Conectar](iesp-connect.md)
</dt> <dt>

[IESP::P ause](iesp-pause.md)
</dt> <dt>

[IESP::Start](iesp-start.md)
</dt> <dt>

[IESP::Stop](iesp-stop.md)
</dt> </dl>

 

 





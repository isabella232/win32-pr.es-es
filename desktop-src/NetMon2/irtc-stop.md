---
description: El método Stop detiene la captura actual.
ms.assetid: 64a80ff1-5a48-4be8-835d-a3d304ebb324
title: 'IRTC:: STOP (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: f25bf9d56a6f41acefad9a552dd2f591158bc74e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677646"
---
# <a name="irtcstop-method"></a>IRTC:: STOP (método)

El método **Stop** detiene la captura actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                          | Descripción                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl> | NPP no está conectado a la red. Llame a [IRTC:: Connect](irtc-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ no se \_ captura**</dt> </dl> | NPP no está capturando datos. Llame a [IRTC:: Start](irtc-start.md) para iniciar la captura.<br/>                            |
| <dl> <dt>**NMERR \_ no es en \_ tiempo real**</dt> </dl>  | NPP está conectado a la red, pero no con el método [IRTC:: Connect](irtc-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Observaciones

Cuando reinicie la captura después de llamar al método **IRTC:: Stop** , asegúrese de llamar a [IRTC:: configure](irtc-configure.md) cada vez que llame a [IRTC:: Start](irtc-start.md) para reiniciar la captura.

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

[IRTC:: Connect](irtc-connect.md)
</dt> <dt>

[IRTC:: configure](irtc-configure.md)
</dt> <dt>

[IRTC:: Start](irtc-start.md)
</dt> </dl>

 

 





---
description: 'Método IESP::Stop: el método Stop detiene la captura actual.'
ms.assetid: d2d4e51a-c6a4-4aec-a805-929af621ffb3
title: Método IESP::Stop (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d22333bcaad688fa9ebb805857db3673f48e70591e1d8953274598acef2b368b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037515"
---
# <a name="iespstop-method"></a>IESP::Stop (método)

El **método Stop** detiene la captura actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpStats* \[ out\]
</dt> <dd>

Puntero a una [estructura STATISTICS que](statistics.md) contiene estadísticas de red, como fotogramas totales y bytes totales capturados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                          | Descripción                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl> | El NPP no está conectado a la red. Llame [a IESP::Conectar](iesp-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ NO \_ CAPTURA**</dt> </dl> | El NPP no captura datos. Llame [a IESP::Start](iesp-start.md) para iniciar la captura.<br/>                            |
| <dl> <dt>**NMERR \_ NOT \_ ESP**</dt> </dl>       | El NPP está conectado a la red, pero no con el [método IESP::Conectar.](iesp-connect.md)<br/>                     |



 

## <a name="remarks"></a>Comentarios

Cuando se **llama al método IESP::Stop,** Monitor de red detiene la captura de datos y cierra el [*archivo de captura.*](c.md) (El nombre del archivo de captura se devolvió cuando se llamó a [IESP::Start).](iesp-start.md) Ahora puede ver el contenido del archivo de captura.

Cuando detenga y reinicie la captura, asegúrese de llamar al método [IESP::Configure](iesp-configure.md) cada vez que llame a [IESP::Start](iesp-start.md) para reiniciar la captura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

[IESP::Start](iesp-start.md)
</dt> <dt>

[Estadísticas](statistics.md)
</dt> </dl>

 

 





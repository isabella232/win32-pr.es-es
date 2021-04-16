---
description: El método Stop detiene la captura actual.
ms.assetid: d2d4e51a-c6a4-4aec-a805-929af621ffb3
title: 'IESP:: STOP (método) (Netmon. h)'
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
ms.openlocfilehash: 50dfb274e1355af93c473609f95607e6b3faf1fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686556"
---
# <a name="iespstop-method"></a>IESP:: STOP (método)

El método **Stop** detiene la captura actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpStats* \[ enuncia\]
</dt> <dd>

Puntero a una estructura de [estadísticas](statistics.md) que contiene estadísticas de red como el total de tramas y el total de bytes capturados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                          | Descripción                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl> | NPP no está conectado a la red. Llame a [iesp:: Connect](iesp-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ no se \_ captura**</dt> </dl> | NPP no está capturando datos. Llame a [iesp:: Start](iesp-start.md) para iniciar la captura.<br/>                            |
| <dl> <dt>**NMERR \_ no \_ ESP**</dt> </dl>       | NPP está conectado a la red, pero no con el método [iesp:: Connect](iesp-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Observaciones

Cuando se llama al método **iesp:: Stop** , monitor de red detiene la captura de datos y cierra el [*archivo de captura.*](c.md) (El nombre del archivo de captura se devolvió cuando se llamó a [iesp:: Start](iesp-start.md) ). Ahora puede examinar el contenido del archivo de captura.

Cuando detenga y reinicie la captura, asegúrese de llamar al método [iesp:: configure](iesp-configure.md) cada vez que llame a [iesp:: Start](iesp-start.md) para reiniciar la captura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[IESP:: Connect](iesp-connect.md)
</dt> <dt>

[IESP:: Start](iesp-start.md)
</dt> <dt>

[¡](statistics.md)
</dt> </dl>

 

 





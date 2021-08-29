---
description: 'Método IStats::Stop: el método Stop detiene la captura actual.'
ms.assetid: 3aeeb29e-e174-46a2-82bb-44c466b8db98
title: Método IStats::Stop (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 5ba7d2d9b3506b11da6ad25e2d6484f6440e9ed92b506d325138860fc1fc5ca1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742695"
---
# <a name="istatsstop-method"></a>IStats::Stop (método)

El **método Stop** detiene la captura actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                            | Descripción                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl>   | El NPP no está conectado a la red. Llame al [método IStats::Conectar](istats-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ NO \_ CAPTURA**</dt> </dl>   | El NPP no captura datos. Llame al [método IStats::Start](istats-start.md) para iniciar la captura.<br/>                            |
| <dl> <dt>**NMERR \_ NO \_ SOLO \_ ESTADÍSTICAS**</dt> </dl> | El NPP está conectado a la red, pero no con el [método IStats::Conectar.](istats-connect.md)<br/>                                |



 

## <a name="remarks"></a>Comentarios

Al reiniciar la captura después de llamar a **IStats::Stop,** asegúrese de llamar al método [IStats::Configure](istats-configure.md) cada vez que llame a [IStats::Start](istats-start.md) para reiniciar la captura.

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

[IStats::Conectar](istats-connect.md)
</dt> <dt>

[IStats::Configure](istats-configure.md)
</dt> <dt>

[IStats::Start](istats-start.md)
</dt> </dl>

 

 





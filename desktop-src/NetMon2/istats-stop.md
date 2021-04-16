---
description: El método Stop detiene la captura actual.
ms.assetid: 3aeeb29e-e174-46a2-82bb-44c466b8db98
title: 'IStas:: STOP (método) (Netmon. h)'
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
ms.openlocfilehash: 7b7b58527e7bde0c3bbdec4fc162b705dd178c10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652458"
---
# <a name="istatsstop-method"></a>IStas:: STOP (método)

El método **Stop** detiene la captura actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                            | Descripción                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl>   | NPP no está conectado a la red. Llame al método [istas:: Connect](istats-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ no se \_ captura**</dt> </dl>   | NPP no está capturando datos. Llame al método [istas:: Start](istats-start.md) para iniciar la captura.<br/>                            |
| <dl> <dt>**NMERR \_ no \_ solo estadísticas \_**</dt> </dl> | NPP está conectado a la red, pero no con el método [istas:: Connect](istats-connect.md) .<br/>                                |



 

## <a name="remarks"></a>Observaciones

Al reiniciar la captura después de llamar a los autores de la llamada **:: Stop** , asegúrese de llamar al método [istas:: configure](istats-configure.md) cada vez que llame a los [ISTA:: Start](istats-start.md) para reiniciar la captura.

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

[ISta:: configurar](istats-configure.md)
</dt> <dt>

[ISta:: Start](istats-start.md)
</dt> </dl>

 

 





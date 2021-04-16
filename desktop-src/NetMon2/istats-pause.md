---
description: El método PAUSE detiene temporalmente la captura actual.
ms.assetid: 43176e9e-1502-484c-a8af-4e7bbf5f6474
title: IStas::P método ause (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d9e9f04ce3d25399866c711dad7a853f2c43c2ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678576"
---
# <a name="istatspause-method"></a>IStas::P método ause

El método **PAUSE** detiene temporalmente la captura actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                            | Descripción                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR en \_ \_ pausa**</dt> </dl>  | La captura ya está en pausa.<br/>                                                                                                    |
| <dl> <dt>**NMERR \_ no se \_ captura**</dt> </dl>   | NPP no está capturando datos. Llame al método [istas:: Start](istats-start.md) para iniciar la captura.<br/>                            |
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl>   | NPP no está conectado a la red. Llame al método [istas:: Connect](istats-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ no \_ solo estadísticas \_**</dt> </dl> | NPP está conectado a la red, pero no con el método [istas:: Connect](istats-connect.md) .<br/>                                |



 

## <a name="remarks"></a>Observaciones

Mientras se pausa la captura, no se capturan nuevos fotogramas hasta que una llamada al método [istas:: resume](istats-resume.md) reinicie la captura.

Cuando se usan los **istas::P ause** y **istas:: resume** (métodos) para controlar la captura, monitor de red continúa agregando [*estadísticas de conversación*](c.md) cada vez que se ejecuta la captura.

Para reiniciar los autores de la llamada de captura [:: resume](istats-resume.md). Para detener la captura, llame a [istas:: Stop](istats-stop.md).

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

[IStas:: resume](istats-resume.md)
</dt> <dt>

[ISta:: Start](istats-start.md)
</dt> <dt>

[IStas:: Stop](istats-stop.md)
</dt> </dl>

 

 





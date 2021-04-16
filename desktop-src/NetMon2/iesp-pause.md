---
description: El método PAUSE pausa la captura actual.
ms.assetid: efbc8947-b9fe-4dbd-8097-375b5f99845e
title: IESP::P método ause (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0558c5dfe36f26e3aad9f31101364d2e8e5c4967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540182"
---
# <a name="iesppause-method"></a>IESP::P método ause

El método **PAUSE pausa** la captura actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Pause(
   LPSTATISTICS lpStats
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpStats* 
</dt> <dd>

Obsoleto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                           | Descripción                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR en \_ \_ pausa**</dt> </dl> | La captura ya está en pausa.<br/>                                                                                     |
| <dl> <dt>**NMERR \_ no se \_ captura**</dt> </dl>  | NPP no está capturando datos. Llame a [iesp:: Start](iesp-start.md) para iniciar la captura.<br/>                            |
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl>  | NPP no está conectado a la red. Llame a [iesp:: Connect](iesp-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ no \_ ESP**</dt> </dl>        | NPP está conectado a la red, pero no con el método [iesp:: Connect](iesp-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Observaciones

Mientras la captura está en un estado de pausa, los datos nuevos no se agregan al [*archivo de captura*](c.md) actual hasta que se llama al método [iesp:: resume](iesp-resume.md) para reiniciar la captura. Cuando se usan **pausar** y **reanudar** para detener y reiniciar la captura, toda la información capturada se coloca en el mismo archivo de captura.

Cuando se usan los métodos **iesp::P ause** y **iesp:: resume** para controlar la captura, monitor de red continúa agregando [*estadísticas de conversación*](c.md) cada vez que se ejecuta la captura.

Para reiniciar la captura, llame a [iesp:: resume](iesp-resume.md). Para detener la captura, llame a [iesp:: Stop](iesp-stop.md).

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

[IESP:: resume](iesp-resume.md)
</dt> <dt>

[IESP:: Start](iesp-start.md)
</dt> <dt>

[IESP:: Stop](iesp-stop.md)
</dt> </dl>

 

 





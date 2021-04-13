---
description: El método PAUSE pausa la captura actual.
ms.assetid: 8c7b310e-de04-4bd8-9c96-3c5948e610be
title: IRTC::P método ause (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d2593c380d0fea52d030586da2f473a3f3fa9446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276277"
---
# <a name="irtcpause-method"></a>IRTC::P método ause

El método **PAUSE pausa** la captura actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                           | Descripción                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR en \_ \_ pausa**</dt> </dl> | La captura ya está en pausa.<br/>                                                                                     |
| <dl> <dt>**NMERR \_ no se \_ captura**</dt> </dl>  | NPP no está capturando datos. Llame a [IRTC:: Start](irtc-start.md) para iniciar la captura.<br/>                            |
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl>  | NPP no está conectado a la red. Llame a [IRTC:: Connect](irtc-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ no es en \_ tiempo real**</dt> </dl>   | NPP está conectado a la red, pero no con el método [IRTC:: Connect](irtc-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Observaciones

Mientras la captura está en un estado de pausa, no se capturan nuevos fotogramas hasta que se llama al método [IRTC:: resume](irtc-resume.md) para reiniciar la captura.

Cuando se usan los métodos **IRTC::P ause** y **IRTC:: resume** para controlar la captura, monitor de red continúa agregando [*estadísticas de conversación*](c.md) cada vez que se ejecuta la captura.

Para reiniciar la llamada de captura [IRTC:: resume](irtc-resume.md). Para detener la captura, llame a [IRTC:: Stop](irtc-stop.md).

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

[IRTC:: resume](irtc-resume.md)
</dt> <dt>

[IRTC:: Start](irtc-start.md)
</dt> <dt>

[IRTC:: Stop](irtc-stop.md)
</dt> </dl>

 

 





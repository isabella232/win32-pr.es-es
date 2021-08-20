---
description: 'Método IDelaydC::Resume: el método Resume reinicia una captura en pausa.'
ms.assetid: 4fa47220-d323-407b-9dae-704969f66bdd
title: Método IDelaydC::Resume (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 224961408fc349cf3f7ebb55ba0f95ee248e680945a88b04cebbbda3391d03e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117981239"
---
# <a name="idelaydcresume-method"></a>IDelaydC::Resume (método)

El **método Resume** reinicia una captura en pausa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                                | Descripción                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CAPTURA DE NMERR \_ \_ NO EN \_ PAUSA**</dt> </dl> | La captura no está en pausa. Llame [**a IDelaydC::P ause para**](idelaydc-pause.md) pausar la captura.<br/>                                |
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl>       | El NPP no está conectado a la red. Llame [**a IDelaydC::Conectar**](idelaydc-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ NO \_ RETRASADO**</dt> </dl>         | El NPP está conectado a la red, pero no con [**el método IDelaydC::Conectar.**](idelaydc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Comentarios

Mientras la captura está en pausa, no se [](c.md) agregan nuevos datos al archivo de captura actual hasta que se llama al método **IDelaydC::Resume** para reiniciar la captura. Cuando [**se**](idelaydc-pause.md) usan **Pausar y reanudar** para detener y reiniciar la captura, toda la información capturada se coloca en el mismo archivo de captura.

Al usar [**Pausar**](idelaydc-pause.md) **y reanudar** para controlar la captura, Monitor de red continúa agregando estadísticas de conversación a las [*estadísticas*](c.md) existentes para la captura actual.

Para detener la captura, llame a [**IDelaydC::Stop**](idelaydc-stop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[**IDelaydC::Conectar**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC::P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC::Stop**](idelaydc-stop.md)
</dt> </dl>

 

 





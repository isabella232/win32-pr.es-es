---
description: 'Método IRTC::Stop: el método Stop detiene la captura actual.'
ms.assetid: 64a80ff1-5a48-4be8-835d-a3d304ebb324
title: Método IRTC::Stop (Netmon.h)
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
ms.openlocfilehash: 10bf0886032c93288435ade05fec46077d53753c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113523"
---
# <a name="irtcstop-method"></a>IRTC::Stop (método)

El **método Stop** detiene la captura actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                          | Descripción                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl> | El NPP no está conectado a la red. Llame [a IRTC::Connect](irtc-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ NO \_ CAPTURA**</dt> </dl> | El NPP no captura datos. Llame [a IRTC::Start](irtc-start.md) para iniciar la captura.<br/>                            |
| <dl> <dt>**NMERR \_ NOT \_ REALTIME**</dt> </dl>  | El NPP está conectado a la red, pero no con el [método IRTC::Connect.](irtc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Comentarios

Cuando reinicie la captura después de llamar al método **IRTC::Stop,** asegúrese de llamar a [IRTC::Configure](irtc-configure.md) cada vez que llame a [IRTC::Start](irtc-start.md) para reiniciar la captura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Connect](irtc-connect.md)
</dt> <dt>

[IRTC::Configure](irtc-configure.md)
</dt> <dt>

[IRTC::Start](irtc-start.md)
</dt> </dl>

 

 





---
description: 'Método IESP::D isconnect: el método Disconnect desconecta el NPP de la red.'
ms.assetid: 962e033d-a51c-47a2-83dc-cee1e7150ab8
title: Método IESP::D isconnect (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d0a07748781a567c889e879e2e99462d8cfb876a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110763"
---
# <a name="iespdisconnect-method"></a>Método IESP::D isconnect

El **método Disconnect** desconecta el NPP de la red.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                          | Descripción                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CAPTURA DE \_ NMERR**</dt> </dl>      | El NPP captura datos. No se puede desconectar de la red mientras la captura de datos está en curso.<br/> |
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl> | El NPP no está conectado a la red.<br/>                                                             |
| <dl> <dt>**NMERR \_ NOT \_ ESP**</dt> </dl>       | El NPP está conectado a la red, pero no con el [método IESP::Connect.](iesp-connect.md)<br/>       |



 

## <a name="remarks"></a>Comentarios

No se puede llamar a este método cuando el NPP captura datos. Debe llamar al método **IESP::Stop** antes de llamar a **IESP::D isconnect**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[IESP::Connect](iesp-connect.md)
</dt> <dt>

[IESP::Stop](iesp-stop.md)
</dt> </dl>

 

 





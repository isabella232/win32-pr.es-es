---
description: Desconecta el NPP de la red.
ms.assetid: 01ff8fc2-aa27-4df8-a499-c7b00c1fa2e8
title: IStas::D método Ulta (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a5fa56c05036380b5dba42089979b43d776a4b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652883"
---
# <a name="istatsdisconnect-method"></a>IStas::D método Ulta

El método **Disconnect** desconecta el NPP de la red.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                            | Descripción                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR \_**</dt> </dl>        | NPP está capturando datos actualmente. No se puede desconectar de la red mientras haya una captura de datos en curso.<br/> |
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl>   | NPP no está conectado a la red.<br/>                                                                         |
| <dl> <dt>**NMERR \_ no \_ solo estadísticas \_**</dt> </dl> | NPP está conectado a la red, pero no con el método [**istas:: Connect**](istats-connect.md) .<br/>          |



 

## <a name="remarks"></a>Observaciones

No se puede llamar a este método cuando NPP está capturando datos. Llame primero al método **istas::D Ulta** y, a continuación, llame a los [**ISTA:: Stop**](istats-stop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IStas**](istats.md)
</dt> <dt>

[**ISta:: Connect**](istats-connect.md)
</dt> <dt>

[**IStas:: Stop**](istats-stop.md)
</dt> </dl>

 

 





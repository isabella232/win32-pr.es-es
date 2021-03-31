---
description: El método QueryStatus recupera el estado de NPP.
ms.assetid: 86b1c1ee-3a35-4603-9e93-fe09f886c32f
title: 'IStas:: QueryStatus (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 02e013d87734b61ad26b6563c402db1b8d4cb4f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819475"
---
# <a name="istatsquerystatus-method"></a>IStas:: QueryStatus (método)

El método **QueryStatus** recupera el estado de NPP.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNetworkStatus* \[ enuncia\]
</dt> <dd>

Puntero a una estructura [NETWORKSTATUS](networkstatus.md) devuelta que indica el estado actual (captura, en pausa, detenido, etc.) del NPP. Es responsabilidad de la aplicación asignar y liberar la memoria de la estructura **NETWORKSTATUS** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es el siguiente código de error:



| Código devuelto                                                                                              | Descripción                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ parámetro no válido \_**</dt> </dl> | El parámetro *pNetworkStatus* no está señalando a una estructura [NETWORKSTATUS](networkstatus.md) válida. Asigne memoria para esta estructura y llame de nuevo al método **istas:: QueryStatus** .<br/> |



 

## <a name="remarks"></a>Observaciones

Se puede llamar a este método en cualquier momento después de llamar al método [CreateNPPInterface](createnppinterface.md) . Se puede llamar a para ver si el NPP está conectado a la red, para averiguar el estado de la captura actual y para ver si hay algún desencadenador pendiente. Sin embargo, antes de llamar a este método, debe asignar la memoria necesaria para la estructura [NETWORKSTATUS](networkstatus.md) y liberar esa memoria cuando la estructura ya no se necesite.

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

[CreateNPPInterface](createnppinterface.md)
</dt> <dt>

[NETWORKSTATUS](networkstatus.md)
</dt> </dl>

 

 





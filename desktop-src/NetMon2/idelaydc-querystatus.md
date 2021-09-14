---
description: 'Método IDelaydC::QueryStatus: el método QueryStatus recupera el estado del NPP.'
ms.assetid: b035d495-a078-4436-9501-0a30fbfa7268
title: Método IDelaydC::QueryStatus (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 13d1e34b57302d263b81ed64df0b136dc01177b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074137"
---
# <a name="idelaydcquerystatus-method"></a>IDelaydC::QueryStatus (método)

El **método QueryStatus** recupera el estado del NPP.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNetworkStatus* \[ out\]
</dt> <dd>

Puntero a una estructura [NETWORKSTATUS devuelta](networkstatus.md) que indica el estado actual (captura, pausada, detenida, y así sucesivamente) del NPP. Es su responsabilidad asignar y liberar la memoria asociada a la **estructura NETWORKSTATUS.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no se realiza correctamente, el valor devuelto es el código de error siguiente:



| Código devuelto                                                                                              | Descripción                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ INVALID \_ PARAMETER**</dt> </dl> | El *parámetro pNetworkStatus* no apunta a una estructura [NETWORKSTATUS](networkstatus.md) válida. Asigne memoria para esta estructura y llame de nuevo **al método IDelaydC::QueryStatus.**<br/> |



 

## <a name="remarks"></a>Observaciones

Se puede llamar a este método en cualquier momento después de llamar a [CreateNPPInterface.](createnppinterface.md) Se puede llamar para ver si el NPP está conectado a la red, para averiguar el estado de la captura actual y para ver si hay algún desencadenador pendiente.

Antes de llamar a este método, debe asignar la memoria necesaria para la estructura [NETWORKSTATUS](networkstatus.md) y liberar esa memoria cuando la estructura ya no sea necesaria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[CreateNPPInterface](createnppinterface.md)
</dt> <dt>

[NETWORKSTATUS](networkstatus.md)
</dt> </dl>

 

 





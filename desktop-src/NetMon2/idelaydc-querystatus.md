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
ms.openlocfilehash: 623601fc295c0f4bf91539c222e7c4986f35010a120086380d06d496a7756b92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910495"
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

Puntero a una estructura [NETWORKSTATUS](networkstatus.md) devuelta que indica el estado actual (captura, pausado, detenido, y así sucesivamente) del NPP. Es su responsabilidad asignar y liberar la memoria asociada a la **estructura NETWORKSTATUS.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no es correcto, el valor devuelto es el código de error siguiente:



| Código devuelto                                                                                              | Descripción                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ INVALID \_ PARAMETER**</dt> </dl> | El *parámetro pNetworkStatus* no apunta a una estructura [NETWORKSTATUS](networkstatus.md) válida. Asigne memoria para esta estructura y vuelva a llamar al **método IDelaydC::QueryStatus.**<br/> |



 

## <a name="remarks"></a>Comentarios

Se puede llamar a este método en cualquier momento después de llamar a [CreateNPPInterface.](createnppinterface.md) Se puede llamar a para ver si el NPP está conectado a la red, para averiguar el estado de la captura actual y para ver si hay algún desencadenador pendiente.

Antes de llamar a este método, debe asignar la memoria necesaria para la estructura [NETWORKSTATUS](networkstatus.md) y liberar esa memoria cuando la estructura ya no sea necesaria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[CreateNPPInterface](createnppinterface.md)
</dt> <dt>

[NETWORKSTATUS](networkstatus.md)
</dt> </dl>

 

 





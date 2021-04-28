---
description: 'Método IRTC::QueryStatus: el método QueryStatus recupera el estado del NPP.'
ms.assetid: 4517eb34-087a-491c-97b5-cbe9190fa7a2
title: Método IRTC::QueryStatus (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 6dd8c18d19df7d577ad219742520630f00122a41
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110613"
---
# <a name="irtcquerystatus-method"></a>IrTC::QueryStatus (método)

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

Puntero a una estructura [NETWORKSTATUS](networkstatus.md) devuelta que indica el estado actual (captura, pausado, detenido, y así sucesivamente) del NPP. Es responsabilidad de la aplicación asignar y liberar la memoria para la **estructura NETWORKSTATUS.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no es correcto, el valor devuelto es el código de error siguiente:



| Código devuelto                                                                                              | Descripción                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ INVALID \_ PARAMETER**</dt> </dl> | El *parámetro pNetworkStatus* no apunta a una estructura [NETWORKSTATUS](networkstatus.md) válida. Asigne memoria para esta estructura y vuelva **a llamar a IRTC::QueryStatus.**<br/> |



 

## <a name="remarks"></a>Comentarios

Se puede llamar a este método en cualquier momento después de llamar al [método CreateNPPInterface.](createnppinterface.md) Puede llamar a este método para ver si el NPP está conectado a la red, para averiguar el estado de la captura actual y para ver si hay algún desencadenador pendiente. Sin embargo, antes de llamar a este método, debe asignar la memoria necesaria para la estructura [NETWORKSTATUS](networkstatus.md) y liberar esa memoria cuando la estructura ya no sea necesaria.

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

[CreateNPPInterface](createnppinterface.md)
</dt> <dt>

[NETWORKSTATUS](networkstatus.md)
</dt> </dl>

 

 





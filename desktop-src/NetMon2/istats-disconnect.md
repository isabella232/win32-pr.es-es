---
description: Desconecta el NPP de la red.
ms.assetid: 01ff8fc2-aa27-4df8-a499-c7b00c1fa2e8
title: Método IStats::D isconnect (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071551"
---
# <a name="istatsdisconnect-method"></a>Método IStats::D isconnect

El **método Disconnect** desconecta el NPP de la red.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                            | Descripción                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CAPTURA DE \_ NMERR**</dt> </dl>        | El NPP está capturando datos actualmente. No se puede desconectar de la red mientras hay una captura de datos en curso.<br/> |
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl>   | El NPP no está conectado a la red.<br/>                                                                         |
| <dl> <dt>**NMERR \_ NO SOLO \_ \_ ESTADÍSTICAS**</dt> </dl> | El NPP está conectado a la red, pero no con el [**método IStats::Conectar.**](istats-connect.md)<br/>          |



 

## <a name="remarks"></a>Observaciones

No se puede llamar a este método cuando el NPP captura datos. Llame primero **al método IStats::D isconnect** y, a continuación, llame a [**IStats::Stop**](istats-stop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IStats**](istats.md)
</dt> <dt>

[**IStats::Conectar**](istats-connect.md)
</dt> <dt>

[**IStats::Stop**](istats-stop.md)
</dt> </dl>

 

 





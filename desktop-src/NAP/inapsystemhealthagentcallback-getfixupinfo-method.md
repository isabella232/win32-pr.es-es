---
title: Método INapSystemHealthAgentCallback GetFixupInfo (NapSystemHealthAgent. h)
description: El NapAgent llama a este método para determinar el estado del agente de mantenimiento del sistema mientras está procesando un SoHResponse.
ms.assetid: cf919b56-3d40-4c49-9c91-25c20ae5ccda
keywords:
- Método GetFixupInfo NAP
- Método GetFixupInfo NAP, interfaz INapSystemHealthAgentCallback
- Interfaz INapSystemHealthAgentCallback NAP, método GetFixupInfo
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetFixupInfo
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227cbe870c722189c995bff0c967eb187548cd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150439"
---
# <a name="inapsystemhealthagentcallbackgetfixupinfo-method"></a>INapSystemHealthAgentCallback:: GetFixupInfo (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El NapAgent llama al método **INapSystemHealthAgentCallback:: GetFixupInfo** para determinar el estado del agente de mantenimiento del sistema mientras está procesando un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetFixupInfo(
  [out] FixupInfo **info
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*información* \[ de enuncia\]
</dt> <dd>

Un puntero a un puntero a una estructura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) que contiene el estado de corrección del agente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                          | Descripción                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | Indica que se completó correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método de devolución de llamada lo declara el sistema NAP y se va a implementar con SHA Writer.

El agente de mantenimiento del sistema debe devolver **S \_ OK** inmediatamente sin bloquearse.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 






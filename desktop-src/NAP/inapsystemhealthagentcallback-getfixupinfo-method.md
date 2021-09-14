---
title: Método INapSystemHealthAgentCallback GetFixupInfo (NapSystemHealthAgent.h)
description: NapAgent llama a este método para determinar el estado del agente de mantenimiento del sistema mientras procesa soHResponse.
ms.assetid: cf919b56-3d40-4c49-9c91-25c20ae5ccda
keywords:
- Método NAP getFixupInfo
- Método NAP de GetFixupInfo, interfaz INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP , GetFixupInfo method
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071643"
---
# <a name="inapsystemhealthagentcallbackgetfixupinfo-method"></a>INapSystemHealthAgentCallback::GetFixupInfo (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

NapAgent llama al método **INapSystemHealthAgentCallback::GetFixupInfo** para determinar el estado del agente de mantenimiento del sistema, mientras procesa [**soHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetFixupInfo(
  [out] FixupInfo **info
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*información* \[ out\]
</dt> <dd>

Puntero a un puntero a una [**estructura FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) que contiene el estado de corrección del agente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                          | Descripción                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Indica que se completó correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

El sistema NAP declara este método de devolución de llamada y lo va a implementar el escritor SHA.

El agente de mantenimiento del sistema debe devolver **S \_ OK** inmediatamente sin bloquear.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 






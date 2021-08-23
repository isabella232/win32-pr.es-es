---
title: Método INapServerInfo GetNapServerInfo (NapServerManagement.h)
description: Recupera información sobre el servidor NAP.
ms.assetid: 02f7ce40-3443-4263-86b2-4276cbc7b694
keywords:
- Método NAP de GetNapServerInfo
- Método NAP de GetNapServerInfo, interfaz INapServerInfo
- Nap de interfaz INapServerInfo , método GetNapServerInfo
topic_type:
- apiref
api_name:
- INapServerInfo.GetNapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eec9926e1a0bf94a1e3dac38c01a169d596c1c00bf032b8f6954f6331d5a4d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626135"
---
# <a name="inapserverinfogetnapserverinfo-method"></a>Método INapServerInfo::GetNapServerInfo

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapServerInfo::GetNapServerInfo** recupera información sobre el servidor NAP.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNapServerInfo(
  [out] CountedString **serverName,
  [out] CountedString **serverDescription,
  [out] CountedString **protocolVersion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*serverName* \[ out\]
</dt> <dd>

Puntero a un puntero a una [**estructura CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene el nombre del servidor.

</dd> <dt>

*serverDescription* \[ out\]
</dt> <dd>

Puntero a un puntero a una [**estructura CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene la descripción del servidor.

</dd> <dt>

*protocolVersion* \[ out\]
</dt> <dd>

Puntero a un puntero a una [**estructura CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene la versión del protocolo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                               |
| Header<br/>                   | <dl> <dt>NapServerManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapServerManagement.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapServerInfo**](inapserverinfo.md)
</dt> <dt>

[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)
</dt> </dl>

 

 






---
title: Método INapClientManagement GetSystemIsolationInfo (NapManagement.h)
description: Recupera información sobre el estado de aislamiento de NapClient.
ms.assetid: e1f69e66-71ca-402e-9c94-8af159d00b21
keywords:
- Método NAP getSystemIsolationInfo
- Método NAP de GetSystemIsolationInfo, interfaz INapClientManagement
- INapClientManagement interface NAP , GetSystemIsolationInfo method
topic_type:
- apiref
api_name:
- INapClientManagement.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9414bb5f2d193aa8f7636b94925914afb7eb123d3b497fdc50d20498fa104fc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368709"
---
# <a name="inapclientmanagementgetsystemisolationinfo-method"></a>INapClientManagement::GetSystemIsolationInfo (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método GetSystemIsolationInfo** recupera información sobre el estado de aislamiento de NapClient.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
) const;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*isolationInfo* \[ out\]
</dt> <dd>

Puntero a un puntero a una estructura [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) que contiene información de estado de aislamiento.

</dd> <dt>

*unknownConnections* \[ out\]
</dt> <dd>

Puntero a una marca que indica si alguna de las conexiones está en un estado desconocido. Si alguno de ellos lo es, la marca se establece en **TRUE**; De lo contrario, la marca se establece **en FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un código de estado HRESULT que incluye, entre otros, uno de los siguientes.



| Código devuelto                                                                                         | Descripción                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Operación correcta.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | El límite de recursos del sistema no pudo realizar la operación.<br/> |
| <dl> <dt>**RPC \_ E \_ DESCONECTADO**</dt> </dl> | NapAgent no se está ejecutando.<br/>                            |



 

## <a name="remarks"></a>Comentarios

La información de aislamiento que se recupera no refleja estados desconocidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                         |
| Header<br/>                   | <dl> <dt>NapManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 






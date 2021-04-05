---
title: Método INapClientManagement2 GetSystemIsolationInfoEx (NapManagement. h)
description: Recupera información sobre el estado de aislamiento y el estado de aislamiento extendido de NapClient.
ms.assetid: 614bcf19-873e-4043-98b2-dcb152bae3e2
keywords:
- Método GetSystemIsolationInfoEx NAP
- Método GetSystemIsolationInfoEx NAP, interfaz INapClientManagement2
- Interfaz INapClientManagement2 NAP, método GetSystemIsolationInfoEx
topic_type:
- apiref
api_name:
- INapClientManagement2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e75a6554ea7e55c3bebe35b797f888494a55627
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079170"
---
# <a name="inapclientmanagement2getsystemisolationinfoex-method"></a>INapClientManagement2:: GetSystemIsolationInfoEx (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **GetSystemIsolationInfoEx** recupera información sobre el estado de aislamiento y el estado de aislamiento extendido de NapClient.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*isolationInfo* \[ enuncia\]
</dt> <dd>

Un puntero a un puntero a una estructura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) que contiene información de estado de aislamiento.

</dd> <dt>

*unknownConnections* \[ enuncia\]
</dt> <dd>

Un puntero a un valor BOOLEANO que es **true** si alguna de las conexiones tiene un estado desconocido y **false** en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un código de estado HRESULT, incluido pero no limitado a uno de los siguientes.



| Código devuelto                                                                                         | Descripción                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                | Operación correcta.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |
| <dl> <dt>**RPC \_ E \_ desconectado**</dt> </dl> | NapAgent no se está ejecutando.<br/>                            |



 

## <a name="remarks"></a>Observaciones

La información de aislamiento que se recupera no refleja Estados desconocidos.

SHA debe liberar la estructura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) llamando a [**FreeIsolationInfoEx**](freeisolationinfoex.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                         |
| Encabezado<br/>                   | <dl> <dt>NapManagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapManagement. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapClientManagement2**](inapclientmanagement2.md)
</dt> </dl>

 

 






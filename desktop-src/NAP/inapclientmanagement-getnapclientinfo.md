---
title: Método INapClientManagement GetNapClientInfo (NapManagement. h)
description: Recupera información sobre el cliente de NAP.
ms.assetid: c0b57cab-729b-40b2-81d2-32a961e377a5
keywords:
- Método GetNapClientInfo NAP
- Método GetNapClientInfo NAP, interfaz INapClientManagement
- Interfaz INapClientManagement NAP, método GetNapClientInfo
topic_type:
- apiref
api_name:
- INapClientManagement.GetNapClientInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11fc496374f2a7f0b7842e22212013149f44f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534630"
---
# <a name="inapclientmanagementgetnapclientinfo-method"></a>INapClientManagement:: GetNapClientInfo (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **GetNapClientInfo** recupera información sobre el cliente NAP.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNapClientInfo(
  [out] BOOL          *isNapEnabled,
  [out] CountedString **clientName,
  [out] CountedString **clientDescription,
  [out] CountedString **protocolVersion
) const;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*isNapEnabled* \[ enuncia\]
</dt> <dd>

Un puntero a un valor BOOLEANO que se establece en **true** si NAP está habilitado; en caso contrario, se establece en **false**.

</dd> <dt>

*nombrecliente* \[ enuncia\]
</dt> <dd>

Un puntero a un puntero a una estructura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene el nombre del cliente.

</dd> <dt>

*clientDescription* \[ enuncia\]
</dt> <dd>

Un puntero a un puntero a una estructura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene la descripción del cliente.

</dd> <dt>

*protocolVersion* \[ enuncia\]
</dt> <dd>

Un puntero a un puntero a una estructura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene la versión del protocolo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un código de estado HRESULT, incluido pero no limitado a uno de los siguientes.



| Código devuelto                                                                                         | Descripción                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                | Operación correcta.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |
| <dl> <dt>**RPC \_ E \_ desconectado**</dt> </dl> | NapAgent no se está ejecutando.<br/>                            |



 

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

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 






---
title: Método INapClientManagement GetNapClientInfo (NapManagement.h)
description: Recupera información sobre el cliente NAP.
ms.assetid: c0b57cab-729b-40b2-81d2-32a961e377a5
keywords:
- Método NAP de GetNapClientInfo
- Método NAP de GetNapClientInfo, interfaz INapClientManagement
- INapClientManagement interface NAP , Método GetNapClientInfo
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161306"
---
# <a name="inapclientmanagementgetnapclientinfo-method"></a>INapClientManagement::GetNapClientInfo (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método GetNapClientInfo** recupera información sobre el cliente NAP.

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

*isNapEnabled* \[ out\]
</dt> <dd>

Puntero a un bool que se establece en **TRUE** si NAP está habilitado; de lo contrario, se establece en **FALSE.**

</dd> <dt>

*clientName* \[ out\]
</dt> <dd>

Puntero a un puntero a una [**estructura CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene el nombre del cliente.

</dd> <dt>

*clientDescription* \[ out\]
</dt> <dd>

Puntero a un puntero a una [**estructura CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene la descripción del cliente.

</dd> <dt>

*protocolVersion* \[ out\]
</dt> <dd>

Puntero a un puntero a una [**estructura CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene la versión del protocolo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un código de estado HRESULT que incluye, entre otros, uno de los siguientes.



| Código devuelto                                                                                         | Descripción                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Operación correcta.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | El límite de recursos del sistema no pudo realizar la operación.<br/> |
| <dl> <dt>**RPC \_ E \_ DESCONECTADO**</dt> </dl> | NapAgent no se está ejecutando.<br/>                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                         |
| Encabezado<br/>                   | <dl> <dt>NapManagement.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapManagement.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 






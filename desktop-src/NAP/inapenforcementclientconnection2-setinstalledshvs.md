---
title: Método INapEnforcementClientConnection2 SetInstalledShvs (NapEnforcementClient.h)
description: Lo usa el agente NAP para establecer los validadores de estado del sistema (SHV) instalados en el cliente.
ms.assetid: 38aa99b9-a15a-414d-91fc-128de8f5a654
keywords:
- Método NAP de SetInstalledShvs
- Método NAP setInstalledShvs , interfaz INapEnforcementClientConnection2
- INapEnforcementClientConnection2 interfaz NAP , Método SetInstalledShvs
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.SetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6651cd5248094f82d9faa1862492f82648e94125
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473789"
---
# <a name="inapenforcementclientconnection2setinstalledshvs-method"></a>Método INapEnforcementClientConnection2::SetInstalledShvs

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El agente NAP usa el método **SetInstalledShvs** para establecer los validadores de estado del sistema (SHV) instalados en el cliente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetInstalledShvs(
  [in] SystemHealthEntityCount count,
  [in] SystemHealthEntityId    *ids
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*count* \[ En\]
</dt> <dd>

Valor [SystemHealthEntityCount](nap-datatypes.md) que especifica el número de SHV que se instalarán en *los identificadores*.

</dd> <dt>

*ids* \[ En\]
</dt> <dd>

Puntero a un [valor SystemHealthEntityId](nap-datatypes.md) que contiene una lista de los id. de SHV que se instalarán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                  | Descripción                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>        | Método realizado correctamente.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El *parámetro count* era 0 (cero).<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 






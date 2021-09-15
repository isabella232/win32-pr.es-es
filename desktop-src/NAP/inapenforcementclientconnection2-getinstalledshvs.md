---
title: Método INapEnforcementClientConnection2 GetInstalledShvs (NapEnforcementClient.h)
description: Lo usa el agente NAP para consultar los validadores de estado del sistema (SHV) instalados en el cliente.
ms.assetid: b2e3ab29-90bf-4117-bc2e-2ff2827ee15c
keywords:
- Método NAP getInstalledShvs
- Método Nap de GetInstalledShvs , interfaz INapEnforcementClientConnection2
- Nap de interfaz INapEnforcementClientConnection2 , método GetInstalledShvs
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa54d09a0c3d3c524262231982f662c497920a0b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473793"
---
# <a name="inapenforcementclientconnection2getinstalledshvs-method"></a>Método INapEnforcementClientConnection2::GetInstalledShvs

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El agente NAP usa el método **GetInstalledShvs** para consultar los validadores de estado del sistema (SHV) instalados en el cliente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetInstalledShvs(
  [out] SystemHealthEntityCount *count,
  [out] SystemHealthEntityId    **ids
) const;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*count* \[ out\]
</dt> <dd>

Puntero a un [valor SystemHealthEntityCount](nap-datatypes.md) que especifica el número de SHV instalados en *los identificadores*.

</dd> <dt>

*ids* \[ out\]
</dt> <dd>

Puntero a una matriz de [valores SystemHealthEntityId](nap-datatypes.md) que contienen los id. de SHV instalados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                   | Descripción                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>         | Operación realizada correctamente.<br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Se pasó un argumento no válido al método .<br/> |



 

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

 

 






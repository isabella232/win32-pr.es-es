---
title: Método INapEnforcementClientConnection2 SetInstalledShvs (NapEnforcementClient. h)
description: Lo usa el agente NAP para establecer los validadores de mantenimiento del sistema (SHV) instalados en el cliente.
ms.assetid: 38aa99b9-a15a-414d-91fc-128de8f5a654
keywords:
- Método SetInstalledShvs NAP
- Método SetInstalledShvs NAP, interfaz INapEnforcementClientConnection2
- Interfaz INapEnforcementClientConnection2 NAP, método SetInstalledShvs
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151230"
---
# <a name="inapenforcementclientconnection2setinstalledshvs-method"></a>INapEnforcementClientConnection2:: SetInstalledShvs (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El agente NAP usa el método **SetInstalledShvs** para establecer los validadores de mantenimiento del sistema (SHV) instalados en el cliente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetInstalledShvs(
  [in] SystemHealthEntityCount count,
  [in] SystemHealthEntityId    *ids
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*recuento* \[ de\]
</dt> <dd>

Valor [SystemHealthEntityCount](nap-datatypes.md) que especifica el número de SHV que se van a instalar en los *identificadores*.

</dd> <dt>

*identificadores* \[ de\]
</dt> <dd>

Un puntero a un valor de [SystemHealthEntityId](nap-datatypes.md) que contiene una lista de identificadores de SHV que se van a instalar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                  | Descripción                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>        | Método realizado correctamente.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El parámetro *Count* era 0 (cero).<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 






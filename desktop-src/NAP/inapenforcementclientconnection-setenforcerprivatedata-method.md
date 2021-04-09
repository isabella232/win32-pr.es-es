---
title: Método INapEnforcementClientConnection SetEnforcerPrivateData (NapEnforcementClient. h)
description: Lo utiliza el aplicador para establecer datos privados.
ms.assetid: 56f6fec7-47ec-4b2c-b8c8-a4d519ba0f91
keywords:
- Método SetEnforcerPrivateData NAP
- Método SetEnforcerPrivateData NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método SetEnforcerPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetEnforcerPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5773294e229a59ff07db8ef546d9d691b369b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079166"
---
# <a name="inapenforcementclientconnectionsetenforcerprivatedata-method"></a>INapEnforcementClientConnection:: SetEnforcerPrivateData (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El forzado usa el método **INapEnforcementClientConnection:: SetEnforcerPrivateData** para establecer datos privados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetEnforcerPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*privateData* \[ de\]
</dt> <dd>

Un puntero a un BLOB de datos opacos de [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que solo puede interpretar el aplicador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

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

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 






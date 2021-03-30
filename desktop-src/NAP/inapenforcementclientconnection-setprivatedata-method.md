---
title: Método INapEnforcementClientConnection SetPrivateData (NapEnforcementClient. h)
description: Lo usa NapAgent para establecer datos privados.
ms.assetid: 2559a612-8857-4e60-b5bc-dd8235ff69f9
keywords:
- Método SetPrivateData NAP
- Método SetPrivateData NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método SetPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3e73248e546b1f0e48438553877f0523bd30b56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079164"
---
# <a name="inapenforcementclientconnectionsetprivatedata-method"></a>INapEnforcementClientConnection:: SetPrivateData (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

NapAgent usa el método **INapEnforcementClientConnection:: SetPrivateData** para establecer datos privados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*privateData* \[ de\]
</dt> <dd>

Un puntero a un BLOB de datos [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que solo el NapAgent puede interpretar.

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

 

 






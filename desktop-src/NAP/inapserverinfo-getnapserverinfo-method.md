---
title: Método INapServerInfo GetNapServerInfo (NapServerManagement. h)
description: Recupera información acerca del servidor NAP.
ms.assetid: 02f7ce40-3443-4263-86b2-4276cbc7b694
keywords:
- Método GetNapServerInfo NAP
- Método GetNapServerInfo NAP, interfaz INapServerInfo
- Interfaz INapServerInfo NAP, método GetNapServerInfo
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
ms.openlocfilehash: 5b182b9e1a5c8d7974128b062fd284c5af3f060f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804064"
---
# <a name="inapserverinfogetnapserverinfo-method"></a>INapServerInfo:: GetNapServerInfo (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapServerInfo:: GetNapServerInfo** recupera información sobre el servidor NAP.

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

*nombreDeServidor* \[ enuncia\]
</dt> <dd>

Un puntero a un puntero a una estructura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene el nombre del servidor.

</dd> <dt>

*serverDescription* \[ enuncia\]
</dt> <dd>

Un puntero a un puntero a una estructura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene la descripción del servidor.

</dd> <dt>

*protocolVersion* \[ enuncia\]
</dt> <dd>

Un puntero a un puntero a una estructura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene la versión del protocolo.

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
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                               |
| Encabezado<br/>                   | <dl> <dt>NapServerManagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapServerManagement. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapServerInfo**](inapserverinfo.md)
</dt> <dt>

[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)
</dt> </dl>

 

 






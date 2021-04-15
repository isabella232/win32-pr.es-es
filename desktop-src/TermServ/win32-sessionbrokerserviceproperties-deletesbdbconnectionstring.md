---
title: Método DeleteSBDbConnectionString de la clase Win32_SessionBrokerServiceProperties
description: Elimina las cadenas de conexión de base de datos (principal o secundaria) del registro.
ms.assetid: 275dd790-bdc7-46d1-a07d-54ec6fa33e44
ms.tgt_platform: multiple
keywords:
- Método DeleteSBDbConnectionString Servicios de Escritorio remoto
- Método DeleteSBDbConnectionString Servicios de Escritorio remoto, clase Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties de clase Servicios de Escritorio remoto, método DeleteSBDbConnectionString
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.DeleteSBDbConnectionString
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a9701afebe150f0c8dc0e4bf437dd23586c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676749"
---
# <a name="deletesbdbconnectionstring-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Método DeleteSBDbConnectionString de la \_ clase SessionBrokerServiceProperties de Win32

Elimina las cadenas de conexión de base de datos (principal o secundaria) del registro.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DeleteSBDbConnectionString(
  [in] boolean IsSecondaryConnString
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IsSecondaryConnString* \[ de\]
</dt> <dd>

Si es **true**, se quita la cadena de conexión secundaria. Si es **false**, se quita la cadena de conexión principal.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                         |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ SessionBrokerServiceProperties**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 






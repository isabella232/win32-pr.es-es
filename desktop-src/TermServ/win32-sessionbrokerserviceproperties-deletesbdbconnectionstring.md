---
title: Método DeleteSBDbConnectionString de la Win32_SessionBrokerServiceProperties clase
description: Elimina las cadenas de conexión de base de datos (principal o secundaria) del Registro.
ms.assetid: 275dd790-bdc7-46d1-a07d-54ec6fa33e44
ms.tgt_platform: multiple
keywords:
- Método DeleteSBDbConnectionString Servicios de Escritorio remoto
- Método DeleteSBDbConnectionString Servicios de Escritorio remoto , Win32_SessionBrokerServiceProperties clase
- Win32_SessionBrokerServiceProperties clase Servicios de Escritorio remoto , método DeleteSBDbConnectionString
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
ms.openlocfilehash: fc468da2af7afc3b963c8990ae662b15a6d1037a6509ab983681e0f51c08305e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118848470"
---
# <a name="deletesbdbconnectionstring-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Método DeleteSBDbConnectionString de la clase \_ SessionBrokerServiceProperties de Win32

Elimina las cadenas de conexión de base de datos (principal o secundaria) del Registro.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DeleteSBDbConnectionString(
  [in] boolean IsSecondaryConnString
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IsSecondaryConnString* \[ En\]
</dt> <dd>

Si **es True,** se quita la cadena de conexión secundaria. Si **es False,** se quita la cadena de conexión principal.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                         |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SessionBrokerServiceProperties de Win32 \_**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 






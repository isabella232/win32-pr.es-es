---
title: Método IsDbReachable de la Win32_SessionBrokerServiceProperties clase
description: Comprueba si la base de datos es accesible.
ms.assetid: c9774d6d-1b78-4ec1-bae2-80d41d4c9b06
ms.tgt_platform: multiple
keywords:
- Método IsDbReachable Servicios de Escritorio remoto
- Método IsDbReachable Servicios de Escritorio remoto , Win32_SessionBrokerServiceProperties clase
- Win32_SessionBrokerServiceProperties clase Servicios de Escritorio remoto método , IsDbReachable
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.IsDbReachable
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1cd7aaf2035251c503d85683f9aa9e9fe7b7f6285084a97133f0573ba41d79c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118848422"
---
# <a name="isdbreachable-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Método IsDbReachable de la clase SessionBrokerServiceProperties de Win32 \_

Comprueba si la base de datos es accesible.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsDbReachable(
  [in] string connStringToDb,
  [in] string connSecondaryStringToDb,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*connStringToDb* \[ En\]
</dt> <dd>

La cadena de conexión a la base de datos.

</dd> <dt>

*connSecondaryStringToDb* \[ En\]
</dt> <dd>

Cadena de conexión secundaria a la base de datos central.

**Windows Server 2012 R2 y Windows Server 2012:** Este parámetro no está disponible antes de Windows Server 2016.

</dd> <dt>

*activeBrokerName* \[ En\]
</dt> <dd>

Nombre del agente activo.

**Windows Server 2012 R2 y Windows Server 2012:** Este parámetro no está disponible antes de Windows Server 2016.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                         |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SessionBrokerServiceProperties de Win32 \_**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 






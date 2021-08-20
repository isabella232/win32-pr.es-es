---
title: Método SetSBDbConnectionStrings de la Win32_SessionBrokerServiceProperties clase
description: Guarda las cadenas de conexión de base de datos, tanto principales como secundarias, en el Registro.
ms.assetid: a9a20eca-22d9-495c-b976-2952c97be67e
ms.tgt_platform: multiple
keywords:
- Método SetSBDbConnectionStrings Servicios de Escritorio remoto
- Método SetSBDbConnectionStrings Servicios de Escritorio remoto , Win32_SessionBrokerServiceProperties clase
- Win32_SessionBrokerServiceProperties clase Servicios de Escritorio remoto , método SetSBDbConnectionStrings
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetSBDbConnectionStrings
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b89baa40d25e6ecf316ac6904cc89091fa581d87be1018c52fa31c2b7ab358d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058423"
---
# <a name="setsbdbconnectionstrings-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Método SetSBDbConnectionStrings de la clase SessionBrokerServiceProperties de Win32 \_

Guarda las cadenas de conexión de base de datos, tanto principales como secundarias, en el Registro.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetSBDbConnectionStrings(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*connStringToCentralDBRdcms* \[ En\]
</dt> <dd>

Cadena de conexión principal.

</dd> <dt>

*secondaryConnStringToCentralDBRdcms* \[ En\]
</dt> <dd>

Cadena de conexión secundaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                         |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SessionBrokerServiceProperties de Win32 \_**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 






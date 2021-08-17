---
title: Método InstallBrokerDatabase de la Win32_SessionBrokerServiceProperties clase
description: Instala una base de datos del agente de conexión a Escritorio remoto en un servidor SQL central.
ms.assetid: 9cc6fa4a-f1eb-49eb-bec4-acaff73190e8
ms.tgt_platform: multiple
keywords:
- Método InstallBrokerDatabase Servicios de Escritorio remoto
- Método InstallBrokerDatabase Servicios de Escritorio remoto , Win32_SessionBrokerServiceProperties clase
- Win32_SessionBrokerServiceProperties clase Servicios de Escritorio remoto , método InstallBrokerDatabase
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.InstallBrokerDatabase
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e77a34c70fbf06bac5501c8cacddce9feb9211d1fe21c1ef30fe429d3e75308
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422455"
---
# <a name="installbrokerdatabase-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Método InstallBrokerDatabase de la clase SessionBrokerServiceProperties de Win32 \_

Instala una base de datos del agente de conexión a Escritorio remoto en un servidor SQL central.

## <a name="syntax"></a>Sintaxis


```mof
uint32 InstallBrokerDatabase(
  [in] string newDbFilePath,
  [in] string connStringToCentralDBMaster,
  [in] string centralRdcmsDbName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newDbFilePath* \[ En\]
</dt> <dd>

nueva ruta de acceso del archivo de base de datos.

</dd> <dt>

*connStringToCentralDBMaster* \[ En\]
</dt> <dd>

Cadena de conexión al maestro de base de datos central.

</dd> <dt>

*centralRdcmsDbName* \[ En\]
</dt> <dd>

Nombre de la base de datos central.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 






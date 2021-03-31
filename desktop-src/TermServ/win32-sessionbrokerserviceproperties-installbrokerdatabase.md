---
title: Método InstallBrokerDatabase de la clase Win32_SessionBrokerServiceProperties
description: Instala una base de datos de agente de conexión a escritorio remoto en un servidor SQL Server central.
ms.assetid: 9cc6fa4a-f1eb-49eb-bec4-acaff73190e8
ms.tgt_platform: multiple
keywords:
- Método InstallBrokerDatabase Servicios de Escritorio remoto
- Método InstallBrokerDatabase Servicios de Escritorio remoto, clase Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties de clase Servicios de Escritorio remoto, método InstallBrokerDatabase
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
ms.openlocfilehash: da560bd4746c41864b3c56438f841efebe71ecd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801298"
---
# <a name="installbrokerdatabase-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Método InstallBrokerDatabase de la \_ clase SessionBrokerServiceProperties de Win32

Instala una base de datos de agente de conexión a escritorio remoto en un servidor SQL Server central.

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

*newDbFilePath* \[ de\]
</dt> <dd>

nueva ruta de acceso del archivo de base de datos.

</dd> <dt>

*connStringToCentralDBMaster* \[ de\]
</dt> <dd>

Cadena de conexión al maestro de base de datos central.

</dd> <dt>

*centralRdcmsDbName* \[ de\]
</dt> <dd>

Nombre de la base de datos central.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                         |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ SessionBrokerServiceProperties**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 






---
title: Método SetSBDbConnectionStrings de la clase Win32_SessionBrokerServiceProperties
description: Guarda las cadenas de conexión de base de datos, tanto las principales como las secundarias, en el registro.
ms.assetid: a9a20eca-22d9-495c-b976-2952c97be67e
ms.tgt_platform: multiple
keywords:
- Método SetSBDbConnectionStrings Servicios de Escritorio remoto
- Método SetSBDbConnectionStrings Servicios de Escritorio remoto, clase Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties de clase Servicios de Escritorio remoto, método SetSBDbConnectionStrings
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
ms.openlocfilehash: 2e4aa02cabe89e434fb8b24b308bbe2ec51fa5f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490577"
---
# <a name="setsbdbconnectionstrings-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Método SetSBDbConnectionStrings de la \_ clase SessionBrokerServiceProperties de Win32

Guarda las cadenas de conexión de base de datos, tanto las principales como las secundarias, en el registro.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetSBDbConnectionStrings(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*connStringToCentralDBRdcms* \[ de\]
</dt> <dd>

Cadena de conexión principal.

</dd> <dt>

*secondaryConnStringToCentralDBRdcms* \[ de\]
</dt> <dd>

La cadena de conexión secundaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                         |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ SessionBrokerServiceProperties**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 






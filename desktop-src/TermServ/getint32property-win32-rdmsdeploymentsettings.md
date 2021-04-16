---
title: Método GetInt32Property de la clase Win32_RDMSDeploymentSettings (Microsoft. Diagnostics. appanalysis. h)
description: Recupera una propiedad de entero para la configuración de implementación de una colección de escritorios virtuales.
ms.assetid: 6b8174bb-ffb7-4699-a3fb-d32ab0b202fc
ms.tgt_platform: multiple
keywords:
- Método GetInt32Property Servicios de Escritorio remoto
- Método GetInt32Property Servicios de Escritorio remoto, clase Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de clase Servicios de Escritorio remoto, método GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f96374c610084c8ef7973d4ac4db603d9c28cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686038"
---
# <a name="getint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método GetInt32Property de la \_ clase RDMSDeploymentSettings de Win32

Recupera una propiedad de entero para la configuración de implementación de una colección de escritorios virtuales.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clave* \[ de de\]
</dt> <dd>

El alias de la colección de escritorios virtuales.

</dd> <dt>

*Valor* \[ de enuncia\]
</dt> <dd>

Entero que recibe el valor recuperado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                                 |
| Espacio de nombres<br/>                | RDMs raíz de \\ CIMv2 \\<br/>                                                                                   |
| Encabezado<br/>                   | <dl> <dt>Microsoft. Diagnostics. appanalysis. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl>                    |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ RDMSDeploymentSettings**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 






---
title: Método SetInt32Property de la clase Win32_RDMSDeploymentSettings
description: Actualiza una propiedad de entero para la configuración de implementación de una colección de escritorios virtuales.
ms.assetid: c5e6dbd5-7db7-4409-bf53-c2680e4a5319
ms.tgt_platform: multiple
keywords:
- Método SetInt32Property Servicios de Escritorio remoto
- Método SetInt32Property Servicios de Escritorio remoto, clase Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de clase Servicios de Escritorio remoto, método SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fecdc42031514d5219fc03172b951602ad021ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686165"
---
# <a name="setint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método SetInt32Property de la \_ clase RDMSDeploymentSettings de Win32

Actualiza una propiedad de entero para la configuración de implementación de una colección de escritorios virtuales.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clave* \[ de de\]
</dt> <dd>

El alias de la colección de escritorios virtuales.

</dd> <dt>

*Valor* \[ de de\]
</dt> <dd>

Nuevo valor de propiedad.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Espacio de nombres<br/>                | RDMs raíz de \\ CIMv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ RDMSDeploymentSettings**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 






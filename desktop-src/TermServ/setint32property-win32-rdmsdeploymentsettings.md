---
title: Método SetInt32Property de la Win32_RDMSDeploymentSettings clase
description: Actualiza una propiedad de entero para la configuración de implementación de una colección de escritorios virtuales.
ms.assetid: c5e6dbd5-7db7-4409-bf53-c2680e4a5319
ms.tgt_platform: multiple
keywords:
- Método SetInt32Property Servicios de Escritorio remoto
- Método SetInt32Property Servicios de Escritorio remoto , Win32_RDMSDeploymentSettings clase
- Win32_RDMSDeploymentSettings clase Servicios de Escritorio remoto , método SetInt32Property
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
ms.openlocfilehash: 73fa8f9ad7560e4d0eeeb8708feb547da00a8e9804e242ceb94666da211b03a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865385"
---
# <a name="setint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método SetInt32Property de la clase RDMSDeploymentSettings de Win32 \_

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

*Clave* \[ En\]
</dt> <dd>

Alias de la colección de escritorios virtuales.

</dd> <dt>

*Valor* \[ En\]
</dt> <dd>

Nuevo valor de propiedad.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Espacio de nombres<br/>                | Rdms \\ de CIMv2 \\ raíz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RDMSDeploymentSettings de Win32 \_**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 






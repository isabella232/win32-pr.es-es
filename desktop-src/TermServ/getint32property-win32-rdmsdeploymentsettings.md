---
title: Método GetInt32Property de la clase Win32_RDMSDeploymentSettings (Microsoft.diagnostics.appanalysis.h)
description: Recupera una propiedad de entero para la configuración de implementación de una colección de escritorios virtuales.
ms.assetid: 6b8174bb-ffb7-4699-a3fb-d32ab0b202fc
ms.tgt_platform: multiple
keywords:
- Método GetInt32Property Servicios de Escritorio remoto
- Método GetInt32Property Servicios de Escritorio remoto , Win32_RDMSDeploymentSettings clase
- Win32_RDMSDeploymentSettings clase Servicios de Escritorio remoto método , GetInt32Property
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968496"
---
# <a name="getint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método GetInt32Property de la clase RDMSDeploymentSettings de Win32 \_

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

*Clave* \[ En\]
</dt> <dd>

Alias de la colección de escritorios virtuales.

</dd> <dt>

*Valor* \[ out\]
</dt> <dd>

Entero que recibe el valor recuperado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                                 |
| Espacio de nombres<br/>                | Rdms \\ de CIMv2 \\ raíz<br/>                                                                                   |
| Encabezado<br/>                   | <dl> <dt>Microsoft.diagnostics.appanalysis.h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl>                    |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>                            |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**RDMSDeploymentSettings de Win32 \_**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 






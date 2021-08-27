---
title: Método GetStringProperty de la Win32_RDSHServer clase
description: Recupera un valor de propiedad de cadena de un objeto \_ RDSHServer de Win32.
ms.assetid: 136cd213-86a6-472a-8853-8d05f992309a
ms.tgt_platform: multiple
keywords:
- Método GetStringProperty Servicios de Escritorio remoto
- Método GetStringProperty Servicios de Escritorio remoto , Win32_RDSHServer clase
- Win32_RDSHServer clase Servicios de Escritorio remoto método , GetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee7540a93e5172ac45fe57527eaa4a105af82e7ad8f73b4a3a25a9fe356ed688
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099495"
---
# <a name="getstringproperty-method-of-the-win32_rdshserver-class"></a>Método GetStringProperty de la clase RDSHServer de Win32 \_

Recupera un valor de propiedad de cadena de [**un objeto \_ RDSHServer de Win32.**](win32-rdshserver.md)

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clave* \[ En\]
</dt> <dd>

Clave que identifica la propiedad que se debe recuperar.

</dd> <dt>

*Valor* \[ out\]
</dt> <dd>

Recibe el valor de propiedad recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error WMI.

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

[**RdsHServer de Win32 \_**](win32-rdshserver.md)
</dt> </dl>

 

 






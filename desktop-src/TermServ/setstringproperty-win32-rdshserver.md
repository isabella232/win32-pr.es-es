---
title: Método SetStringProperty de la Win32_RDSHServer (Certenroll.h)
description: Actualiza un valor de propiedad de cadena de un objeto \_ RDSHServer de Win32.
ms.assetid: 9a338872-27fc-4e37-afd6-20a42c7859e5
ms.tgt_platform: multiple
keywords:
- Método SetStringProperty Servicios de Escritorio remoto
- Método SetStringProperty Servicios de Escritorio remoto , Win32_RDSHServer clase
- Win32_RDSHServer clase Servicios de Escritorio remoto , método SetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDSHServer.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d30812c0df943175f96c8ae43a4fe094725c74
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374395"
---
# <a name="setstringproperty-method-of-the-win32_rdshserver-class"></a>Método SetStringProperty de la clase \_ RDSHServer de Win32

Actualiza un valor de propiedad de cadena de [**un objeto \_ RDSHServer de Win32.**](win32-rdshserver.md)

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clave* \[ En\]
</dt> <dd>

Clave que identifica la propiedad que se debe actualizar.

</dd> <dt>

*Valor* \[ En\]
</dt> <dd>

Nuevo valor de propiedad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Espacio de nombres<br/>                | Rdms \\ de CIMv2 \\ raíz<br/>                                                                |
| Encabezado<br/>                   | <dl> <dt>Certenroll.h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RdsHServer de Win32 \_**](win32-rdshserver.md)
</dt> </dl>

 

 






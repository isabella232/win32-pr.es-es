---
title: Método KeyValueGet de la clase Win32_RDSHCollection clave
description: Recupera el valor asociado a la clave especificada en la colección.
ms.assetid: 69d309a4-b32e-4dbc-bd28-be79d395ac26
ms.tgt_platform: multiple
keywords:
- Método KeyValueGet Servicios de Escritorio remoto
- Método KeyValueGet Servicios de Escritorio remoto , Win32_RDSHCollection clase
- Win32_RDSHCollection clase Servicios de Escritorio remoto método , KeyValueGet
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueGet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 943db8db044758e7f78e7d79b4ae5280c6ce51281b5858237a24e5f83add33a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422685"
---
# <a name="keyvalueget-method-of-the-win32_rdshcollection-class"></a>Método KeyValueGet de la clase RDSHCollection win32 \_

Recupera el valor asociado a la clave especificada en la colección.

## <a name="syntax"></a>Sintaxis


```mof
uint32 KeyValueGet(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clave* \[ En\]
</dt> <dd>

Clave que identifica el valor que desea recuperar.

</dd> <dt>

*Valor* \[ out\]
</dt> <dd>

Si se ejecuta correctamente, devuelve el valor asociado a la clave especificada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                              |
| Espacio de nombres<br/>                | Rdms \\ cimv2 \\ raíz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RDSHCollection de Win32 \_**](win32-rdshcollection.md)
</dt> </dl>

 

 






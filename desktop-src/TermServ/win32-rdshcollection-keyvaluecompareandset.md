---
title: Método KeyValueCompareAndSet de la Win32_RDSHCollection clave
description: Compara la clave especificada de la colección con un comparador; Si coinciden, la clave se establece en un nuevo valor. Si la clave no existe, el método insertará la clave en la colección.
ms.assetid: ea6195b3-1a20-4d5b-b9a3-796976818b4f
ms.tgt_platform: multiple
keywords:
- Método KeyValueCompareAndSet Servicios de Escritorio remoto
- Método KeyValueCompareAndSet Servicios de Escritorio remoto , Win32_RDSHCollection clase
- Win32_RDSHCollection clase Servicios de Escritorio remoto método , KeyValueCompareAndSet
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueCompareAndSet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52e1aaaf90313c8c1434a65c4ffd1045933ad503245f0dacbf78c2b7e1ca054a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422715"
---
# <a name="keyvaluecompareandset-method-of-the-win32_rdshcollection-class"></a>Método KeyValueCompareAndSet de la clase \_ RDSHCollection de Win32

Compara la clave especificada de la colección con un comparador; Si coinciden, la clave se establece en un nuevo valor. Si la clave no existe, el método insertará la clave en la colección.

## <a name="syntax"></a>Sintaxis


```mof
uint32 KeyValueCompareAndSet(
  [in]  string Key,
  [in]  string NewValue,
  [in]  string Comparand,
  [out] string InitialValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clave* \[ En\]
</dt> <dd>

Clave que se va a comparar.

</dd> <dt>

*NewValue* \[ En\]
</dt> <dd>

Nuevo valor.

</dd> <dt>

*Comparand* \[ En\]
</dt> <dd>

Cadena con la que se compara la clave.

</dd> <dt>

*InitialValue* \[ out\]
</dt> <dd>

En caso de éxito o error, contiene el valor inicial de la clave.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Tenga en cuenta que este método puede recuperar el valor de la clave y, como tal, encapsula la funcionalidad [**de KeyValueGet**](win32-rdshcollection-keyvalueget.md).

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

[**RdsHCollection de Win32 \_**](win32-rdshcollection.md)
</dt> </dl>

 

 






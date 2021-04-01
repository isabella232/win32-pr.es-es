---
title: Método KeyValueCompareAndSet de la clase Win32_RDSHCollection
description: Compara la clave especificada de la colección con un comparand; Si coinciden, la clave se establece en un valor nuevo. Si la clave no existe, el método insertará la clave en la colección.
ms.assetid: ea6195b3-1a20-4d5b-b9a3-796976818b4f
ms.tgt_platform: multiple
keywords:
- Método KeyValueCompareAndSet Servicios de Escritorio remoto
- Método KeyValueCompareAndSet Servicios de Escritorio remoto, clase Win32_RDSHCollection
- Win32_RDSHCollection de clase Servicios de Escritorio remoto, método KeyValueCompareAndSet
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
ms.openlocfilehash: 20b90d703b40cf76f59cc3caf5d8f197f387cfe8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905155"
---
# <a name="keyvaluecompareandset-method-of-the-win32_rdshcollection-class"></a>Método KeyValueCompareAndSet de la \_ clase RDSHCollection de Win32

Compara la clave especificada de la colección con un comparand; Si coinciden, la clave se establece en un valor nuevo. Si la clave no existe, el método insertará la clave en la colección.

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

*Clave* \[ de de\]
</dt> <dd>

Clave que se va a comparar.

</dd> <dt>

*Nuevovalor* \[ de\]
</dt> <dd>

Nuevo valor.

</dd> <dt>

*Comparand* \[ de\]
</dt> <dd>

Cadena a la que se va a comparar la clave.

</dd> <dt>

*InitialValue* \[ enuncia\]
</dt> <dd>

En caso de éxito o error, contiene el valor inicial de la clave.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Tenga en cuenta que este método puede recuperar el valor de la clave y, como tal, encapsula la funcionalidad de [**KeyValueGet**](win32-rdshcollection-keyvalueget.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                              |
| Espacio de nombres<br/>                | RDMs raíz de \\ cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ RDSHCollection**](win32-rdshcollection.md)
</dt> </dl>

 

 






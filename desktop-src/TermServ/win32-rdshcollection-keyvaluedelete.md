---
title: Método KeyValueDelete de la Win32_RDSHCollection clase
description: Elimina la clave especificada (y el valor asociado) de la colección.
ms.assetid: 968d6744-7b4a-45e5-87fb-90c408dbc771
ms.tgt_platform: multiple
keywords:
- Método KeyValueDelete Servicios de Escritorio remoto
- Método KeyValueDelete Servicios de Escritorio remoto , Win32_RDSHCollection clase
- Win32_RDSHCollection clase Servicios de Escritorio remoto método , KeyValueDelete
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueDelete
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64efd9beb6aaca70cd92d8eefe8e7b93b91aea9fbbecb6377d76f8c69b7f85c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118849080"
---
# <a name="keyvaluedelete-method-of-the-win32_rdshcollection-class"></a>Método KeyValueDelete de la clase \_ RDSHCollection de Win32

Elimina la clave especificada (y el valor asociado) de la colección.

## <a name="syntax"></a>Sintaxis


```mof
uint32 KeyValueDelete(
  [in] string Key
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clave* \[ En\]
</dt> <dd>

Clave que se debe eliminar.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 






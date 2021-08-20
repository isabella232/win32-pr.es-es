---
title: Método SetInt32Property de la Win32_RDSHCollection clase
description: Actualiza un valor de propiedad de entero de un objeto \_ RDSHCollection de Win32.
ms.assetid: 2a9a5d83-d147-43b3-b57c-6c744da0923d
ms.tgt_platform: multiple
keywords:
- Método SetInt32Property Servicios de Escritorio remoto
- Método SetInt32Property Servicios de Escritorio remoto , Win32_RDSHCollection clase
- Win32_RDSHCollection clase Servicios de Escritorio remoto método , SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d19af81a807d6a2eb27693b88428df925644675093d3fbb80cb809a6011fb22b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127460"
---
# <a name="setint32property-method-of-the-win32_rdshcollection-class"></a>Método SetInt32Property de la clase RDSHCollection de Win32 \_

Actualiza un valor de propiedad de entero de [**un objeto \_ RDSHCollection de Win32.**](win32-rdshcollection.md)

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
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RDSHCollection de Win32 \_**](win32-rdshcollection.md)
</dt> </dl>

 

 






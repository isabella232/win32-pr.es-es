---
description: Especifica los permisos de control de acceso para un directorio en una tarjeta inteligente.
ms.assetid: 361d9fa0-286e-4d2c-8452-3b5f48e77779
title: Enumeración CARD_DIRECTORY_ACCESS_CONDITION (Cardmod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_DIRECTORY_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: 9879fa73f6bb45b56f433d7bca7765ab5fc0daef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275334"
---
# <a name="card_directory_access_condition-enumeration"></a>\_ \_ Enumeración de condiciones de acceso al directorio de tarjeta \_

La enumeración **\_ condición de \_ acceso \_ al directorio** de la tarjeta especifica los permisos de control de acceso para un directorio en una [*tarjeta inteligente*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintaxis


```C++
typedef enum  { 
  InvalidAc               = 0,
  UserCreateDeleteDirAc   = 1,
  AdminCreateDeleteDirAc  = 2
} CARD_DIRECTORY_ACCESS_CONDITION;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**
</dt> <dd>

Este valor no es válido.

</dd> <dt>

<span id="UserCreateDeleteDirAc"></span><span id="usercreatedeletedirac"></span><span id="USERCREATEDELETEDIRAC"></span>**UserCreateDeleteDirAc**
</dt> <dd>

Los usuarios específicos pueden leer, escribir y eliminar el directorio.

</dd> <dt>

<span id="AdminCreateDeleteDirAc"></span><span id="admincreatedeletedirac"></span><span id="ADMINCREATEDELETEDIRAC"></span>**AdminCreateDeleteDirAc**
</dt> <dd>

Los administradores pueden leer, escribir y eliminar el directorio.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, \[ solo aplicaciones de escritorio de Windows XP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Server 2003, solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>            |
| Encabezado<br/>                   | <dl> <dt>Cardmod. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Proveedor de servicios criptográficos de tarjeta inteligente base de Microsoft](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[**CardCreateDirectory**](/previous-versions/windows/desktop/secsmart/cardcreatedirectory)
</dt> <dt>

[**CardDeleteDirectory**](/previous-versions/windows/desktop/secsmart/carddeletedirectory)
</dt> </dl>

 

 

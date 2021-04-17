---
description: Especifica los permisos de control de acceso para un archivo en una tarjeta inteligente.
ms.assetid: 995d959f-30dc-4e5c-be2d-6b447499415a
title: Enumeración CARD_FILE_ACCESS_CONDITION (Cardmod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_FILE_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: d3ef9fc81c9ab3bff5f3992c3aedeb3f923648ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666459"
---
# <a name="card_file_access_condition-enumeration"></a>\_ \_ Enumeración de condiciones de acceso a archivos de tarjeta \_

La enumeración de la **\_ \_ \_ condición de acceso a archivos de tarjeta** especifica los permisos de control de acceso para un archivo en una [*tarjeta inteligente*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintaxis


```C++
typedef enum  { 
  InvalidAc                 = 0,
  EveryoneReadUserWriteAc   = 1,
  UserWriteExecuteAc        = 2,
  EveryoneReadAdminWriteAc  = 3,
  UnknownAc                 = 4
} CARD_FILE_ACCESS_CONDITION;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**
</dt> <dd>

Este valor no es válido.

</dd> <dt>

<span id="EveryoneReadUserWriteAc"></span><span id="everyonereaduserwriteac"></span><span id="EVERYONEREADUSERWRITEAC"></span>**EveryoneReadUserWriteAc**
</dt> <dd>

Todo el mundo puede leer el archivo. Los usuarios específicos pueden escribir en el archivo.

</dd> <dt>

<span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**UserWriteExecuteAc**
</dt> <dd>

Solo los usuarios específicos pueden leer o escribir en el archivo.

</dd> <dt>

<span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**EveryoneReadAdminWriteAc**
</dt> <dd>

Todo el mundo puede leer el archivo. Los administradores pueden escribir en el archivo.

</dd> <dt>

<span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**UnknownAc**
</dt> <dd>

Los permisos de acceso para el archivo son desconocidos.

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

[**\_información del archivo de tarjeta \_**](/previous-versions/windows/desktop/secsmart/card-file-info)
</dt> <dt>

[**CardCreateFile**](/previous-versions/windows/desktop/secsmart/cardcreatefile)
</dt> </dl>

 

 

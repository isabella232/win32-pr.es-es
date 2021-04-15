---
title: WM_BACKUP_RESTORE_STATUS estructura (wmdrmsdk. h)
description: La estructura de estado de restauración de copia de seguridad de WM \_ \_ \_ contiene información sobre una operación de restauración o copia de seguridad de licencias pendiente.
ms.assetid: 74e94bc6-376b-4848-a9f9-11c9cb4005f2
keywords:
- WM_BACKUP_RESTORE_STATUS estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- WM_BACKUP_RESTORE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476cd4ddab42ec9f8f44ff51b492bd3913824cf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709074"
---
# <a name="wm_backup_restore_status-structure"></a>\_Estructura de \_ Estado de restauración de copia de seguridad de WM \_

La estructura de **Estado de restauración de copia de seguridad de WM \_ \_ \_** contiene información sobre una operación de restauración o copia de seguridad de licencias pendiente.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct WM_BACKUP_RESTORE_STATUS {
  MSDRM_STATUS eStatus;
  BSTR         bstrError;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**eStatus**
</dt> <dd>

Miembro de la enumeración de [**\_ Estado MSDRM**](msdrm-status.md) que especifica el estado.

</dd> <dt>

**bstrError**
</dt> <dd>

Cadena que contiene el error.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se recibe cuando se llama al método [**IWMDRMLicenseBackupRestoreStatus:: getStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) . Contiene el estado de la operación de copia de seguridad o restauración pendiente en el momento de la llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 






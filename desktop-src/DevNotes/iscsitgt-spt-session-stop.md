---
description: Se usa con el código de \_ \_ control IOCTL SCSI MINIPORT IOCTL y el código de control CTLCODE \_ ISCSITGT \_ SPT SESSION END \_ (0x101) para detener una \_ sesión.
ms.assetid: 74DAA560-A5BA-475C-AA36-7E6F0EA82EFE
title: ISCSITGT_SPT_SESSION_STOP estructura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCSITGT_SPT_SESSION_STOP
api_type:
- NA
api_location: ''
ms.openlocfilehash: dba4c54e6fbae3ef947ec5ac5f5c4b178434566d15cc0591104dd38a8e456fb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001494"
---
# <a name="iscsitgt_spt_session_stop-structure"></a>Estructura ISCSITGT \_ SPT \_ SESSION \_ STOP

\[La siguiente estructura está disponible para su uso en Windows Server 2012 R2. En versiones posteriores podría modificarse o no estar disponible.\]

Se usa con el código de control [**\_ \_ IOCTL SCSI MINIPORT**](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_miniport) IOCTL y el código de control CTLCODE \_ ISCSITGT \_ SPT \_ SESSION END (0x101) para detener una \_ sesión.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _ISCSITGT_SPT_SESSION_STOP {
  SRB_IO_CONTROL Header;
  SESSION_COOKIE ITNexusHandle;
} ISCSITGT_SPT_SESSION_STOP, *PISCSITGT_SPT_SESSION_STOP;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Header**
</dt> <dd>

Encabezado obligatorio.

</dd> <dt>

**ITNexusHandle**
</dt> <dd>

Identificador opaco que representa una sesión.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                               |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/> |
| Fin de compatibilidad de cliente<br/>    | No se admite ninguno<br/>                               |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2012 R2<br/>                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Paso a través de destino iSCSI](/powershell/module/iscsi)
</dt> <dt>

[**SRB \_ IO \_ CONTROL**](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_srb_io_control)
</dt> </dl>

 

 

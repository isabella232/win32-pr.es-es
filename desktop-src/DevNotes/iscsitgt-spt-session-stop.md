---
description: Se usa con el \_ IOCTL del minipuerto SCSI de ioctl \_ y el código de control del extremo de la sesión de CTLCODE \_ ISCSITGT de un solo \_ \_ \_ controlador de sesión (0x101) para detener una sesión.
ms.assetid: 74DAA560-A5BA-475C-AA36-7E6F0EA82EFE
title: Estructura de ISCSITGT_SPT_SESSION_STOP
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
ms.openlocfilehash: e4501fbe2d1bbf884448d6b6a9476ee4782d3da7
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "103914290"
---
# <a name="iscsitgt_spt_session_stop-structure"></a>\_Estructura de \_ detención de sesión de ISCSITGT \_

\[La siguiente estructura está disponible para su uso en Windows Server 2012 R2. En versiones posteriores podría modificarse o no estar disponible.\]

Se usa con el IOCTL del [**\_ \_ minipuerto SCSI de ioctl**](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_miniport) y el código de control del extremo de la sesión de CTLCODE \_ ISCSITGT de un solo \_ \_ \_ controlador de sesión (0x101) para detener una sesión.

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

Un identificador opaco que representa una sesión.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | No se admite ninguno<br/>                               |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2012 R2<br/>                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Paso a través de destino iSCSI](/powershell/module/iscsi)
</dt> <dt>

[**\_control de e/s SRB \_**](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_srb_io_control)
</dt> </dl>

 

 

---
title: Método ProvisioningJobCancel de la Win32_RDMSVirtualDesktopCollection clase
description: Cancela un trabajo de aprovisionamiento de escritorio virtual.
ms.assetid: 933ea0f3-b916-4e70-89de-597f9eb23976
ms.tgt_platform: multiple
keywords:
- Método ProvisioningJobCancel Servicios de Escritorio remoto
- Método ProvisioningJobCancel Servicios de Escritorio remoto , Win32_RDMSVirtualDesktopCollection clase
- Win32_RDMSVirtualDesktopCollection clase Servicios de Escritorio remoto método , ProvisioningJobCancel
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobCancel
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e62e3305cdb544d0a45ee299c8bc5508bbef4915134fbf2d09f1c0b4884cc51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866085"
---
# <a name="provisioningjobcancel-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Método ProvisioningJobCancel de la clase \_ RDMSVirtualDesktopCollection de Win32

Cancela un trabajo de aprovisionamiento de escritorio virtual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ProvisioningJobCancel(
  [in] string JobGuid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*JobGuid* \[ En\]
</dt> <dd>

GUID **que** identifica de forma única el trabajo de aprovisionamiento que se debe cancelar.

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

[**RDMSVirtualDesktopCollection de Win32 \_**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 






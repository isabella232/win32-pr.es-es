---
title: Método ProvisioningJobExecute de la Win32_RDMSVirtualDesktopCollection clase
description: Ejecuta un trabajo de aprovisionamiento de escritorios virtuales.
ms.assetid: 69f0cc6a-7eef-4cd9-94ac-f0c7e52d02d8
ms.tgt_platform: multiple
keywords:
- Método ProvisioningJobExecute Servicios de Escritorio remoto
- Método ProvisioningJobExecute Servicios de Escritorio remoto , Win32_RDMSVirtualDesktopCollection clase
- Win32_RDMSVirtualDesktopCollection clase Servicios de Escritorio remoto método , ProvisioningJobExecute
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobExecute
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd22c40ea19ce6e30f7e2accd2414f134a5a622ef29d605e2abe2183091eb538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117940609"
---
# <a name="provisioningjobexecute-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Método ProvisioningJobExecute de la clase \_ RDMSVirtualDesktopCollection de Win32

Ejecuta un trabajo de aprovisionamiento de escritorios virtuales.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ProvisioningJobExecute(
  [in]  string JobInputXml,
  [out] string JobGuid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*JobInputXml* \[ En\]
</dt> <dd>

Cadena que contiene la información de aprovisionamiento en formato XML.

</dd> <dt>

*JobGuid* \[ out\]
</dt> <dd>

GUID **que identifica** de forma única el trabajo de aprovisionamiento que se ejecutará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error WMI.

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

 

 






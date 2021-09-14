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
ms.openlocfilehash: c632a6bdc5fc5c4a128941d8a6c8b4379ddf9629
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073319"
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

 

 






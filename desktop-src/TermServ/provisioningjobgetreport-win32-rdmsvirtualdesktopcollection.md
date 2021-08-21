---
title: Método ProvisioningJobGetReport de la Win32_RDMSVirtualDesktopCollection clase
description: Obtiene un informe sobre el estado de un trabajo de aprovisionamiento de escritorios virtuales.
ms.assetid: 8fc03fed-0838-4530-9b0f-0f561d76769d
ms.tgt_platform: multiple
keywords:
- Método ProvisioningJobGetReport Servicios de Escritorio remoto
- Método ProvisioningJobGetReport Servicios de Escritorio remoto , Win32_RDMSVirtualDesktopCollection clase
- Win32_RDMSVirtualDesktopCollection clase Servicios de Escritorio remoto método , ProvisioningJobGetReport
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobGetReport
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 095caab3b98cdcbd6f451e021f835482a5cb3f1c1c995f1eae685f45a18920a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118852620"
---
# <a name="provisioningjobgetreport-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Método ProvisioningJobGetReport de la clase \_ RDMSVirtualDesktopCollection de Win32

Obtiene un informe sobre el estado de un trabajo de aprovisionamiento de escritorios virtuales.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ProvisioningJobGetReport(
  [in]  string JobGuid,
  [out] string JobReportXml
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*JobGuid* \[ En\]
</dt> <dd>

GUID **que** identifica de forma única el trabajo de aprovisionamiento.

</dd> <dt>

*JobReportXml* \[ out\]
</dt> <dd>

Cadena que contiene el informe en formato XML.

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

 

 






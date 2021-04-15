---
title: Método ProvisioningJobGetReport de la clase Win32_RDMSVirtualDesktopCollection
description: Obtiene un informe sobre el estado de un trabajo de aprovisionamiento de escritorio virtual.
ms.assetid: 8fc03fed-0838-4530-9b0f-0f561d76769d
ms.tgt_platform: multiple
keywords:
- Método ProvisioningJobGetReport Servicios de Escritorio remoto
- Método ProvisioningJobGetReport Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de clase Servicios de Escritorio remoto, método ProvisioningJobGetReport
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
ms.openlocfilehash: 9d6605402c6ed6c0269b9971922bdefd48f265c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676809"
---
# <a name="provisioningjobgetreport-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Método ProvisioningJobGetReport de la \_ clase RDMSVirtualDesktopCollection de Win32

Obtiene un informe sobre el estado de un trabajo de aprovisionamiento de escritorio virtual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ProvisioningJobGetReport(
  [in]  string JobGuid,
  [out] string JobReportXml
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*JobGuid* \[ de\]
</dt> <dd>

**GUID** que identifica de forma única el trabajo de aprovisionamiento.

</dd> <dt>

*JobReportXml* \[ enuncia\]
</dt> <dd>

Cadena que contiene el informe en formato XML.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Espacio de nombres<br/>                | RDMs raíz de \\ CIMv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktopCollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 






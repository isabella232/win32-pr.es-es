---
title: Método ProvisioningEnumerateJobs de la clase Win32_RDMSVirtualDesktopCollection
description: Enumera los trabajos de aprovisionamiento de escritorio virtual para este servicio.
ms.assetid: 4bd2b03f-ba8c-483e-af09-270424f9b1ed
ms.tgt_platform: multiple
keywords:
- Método ProvisioningEnumerateJobs Servicios de Escritorio remoto
- Método ProvisioningEnumerateJobs Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de clase Servicios de Escritorio remoto, método ProvisioningEnumerateJobs
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningEnumerateJobs
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa2b54a0599c2bbcaf6b0f9a9acb3ab3028389b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535385"
---
# <a name="provisioningenumeratejobs-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Método ProvisioningEnumerateJobs de la \_ clase RDMSVirtualDesktopCollection de Win32

Enumera los trabajos de aprovisionamiento de escritorio virtual para este servicio.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ProvisioningEnumerateJobs(
  [in]  uint32 JobType,
  [in]  string CollectionAlias,
  [out] string JobGuids[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*JobType* \[ de\]
</dt> <dd>

Entero que especifica el tipo de trabajo que se va a enumerar.

Este parámetro se puede establecer en uno de los siguientes valores:

<dt>

0
</dt> <dd>

Trabajos en ejecución

</dd> <dt>

1
</dt> <dd>

Trabajos completados

</dd> </dl> </dd> <dt>

*CollectionAlias* \[ de\]
</dt> <dd>

El alias de la colección de escritorios virtuales que se va a enumerar. El valor predeterminado de este parámetro es FALSE, que especifica que se deben enumerar todos los trabajos en ejecución.

</dd> <dt>

*JobGuids* \[ enuncia\]
</dt> <dd>

Una matriz que contiene los **GUID** de los trabajos de aprovisionamiento que se van a enumerar.

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

 

 






---
title: Método ProvisioningEnumerateJobs de la Win32_RDMSVirtualDesktopCollection clase
description: Enumera los trabajos de aprovisionamiento de escritorios virtuales para este servicio.
ms.assetid: 4bd2b03f-ba8c-483e-af09-270424f9b1ed
ms.tgt_platform: multiple
keywords:
- Método ProvisioningEnumerateJobs Servicios de Escritorio remoto
- Método ProvisioningEnumerateJobs Servicios de Escritorio remoto , Win32_RDMSVirtualDesktopCollection clase
- Win32_RDMSVirtualDesktopCollection clase Servicios de Escritorio remoto método , ProvisioningEnumerateJobs
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
ms.openlocfilehash: 5b24ef80acdb29c75327447f61db7dae1689a883f69c9e19ef199710de216fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118350227"
---
# <a name="provisioningenumeratejobs-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Método ProvisioningEnumerateJobs de la clase \_ RDMSVirtualDesktopCollection de Win32

Enumera los trabajos de aprovisionamiento de escritorios virtuales para este servicio.

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

*JobType* \[ En\]
</dt> <dd>

Entero que especifica el tipo de trabajo que se enumerará.

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

*CollectionAlias* \[ En\]
</dt> <dd>

Alias de la colección de escritorios virtuales que se enumerará. El valor predeterminado de este parámetro es FALSE, que especifica que se van a enumerar todos los trabajos en ejecución.

</dd> <dt>

*JobGuids* \[ out\]
</dt> <dd>

Matriz que contiene los **GUID de los** trabajos de aprovisionamiento que se enumerará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Espacio de nombres<br/>                | Rdms \\ de CIMv2 \\ raíz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**RDMSVirtualDesktopCollection de Win32 \_**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 






---
title: Método GetPatchProperties de la Win32_RDMSVirtualDesktopCollection clase
description: Recupera las propiedades de un trabajo de aprovisionamiento de actualizaciones de software para las máquinas virtuales de una colección de escritorios virtuales.
ms.assetid: 9f228d89-0613-49c7-8169-48491c3a2d9b
ms.tgt_platform: multiple
keywords:
- Método GetPatchProperties Servicios de Escritorio remoto
- Método GetPatchProperties Servicios de Escritorio remoto , Win32_RDMSVirtualDesktopCollection clase
- Win32_RDMSVirtualDesktopCollection clase Servicios de Escritorio remoto método , GetPatchProperties
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetPatchProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f0ca45c97512818aa5f8a9ea851d18fa5554c32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968479"
---
# <a name="getpatchproperties-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Método GetPatchProperties de la clase \_ RDMSVirtualDesktopCollection de Win32

Recupera las propiedades de un trabajo de aprovisionamiento de actualizaciones de software para las máquinas virtuales de una colección de escritorios virtuales.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetPatchProperties(
  [out] DATETIME StartTime,
  [out] DATETIME ForceLogOffTime,
  [out] string   JobGuid,
  [out] uint32   State
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StartTime* \[ out\]
</dt> <dd>

Fecha y hora en que se instalarán las actualizaciones.

</dd> <dt>

*ForceLogOffTime* \[ out\]
</dt> <dd>

Fecha y hora en que el sistema cerrará la sesión de los usuarios de las máquinas virtuales.

</dd> <dt>

*JobGuid* \[ out\]
</dt> <dd>

GUID **que** identifica de forma única el trabajo de aprovisionamiento.

</dd> <dt>

*Estado* \[ out\]
</dt> <dd>

Estado del trabajo de aprovisionamiento.

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**RDMSVirtualDesktopCollection de Win32 \_**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 






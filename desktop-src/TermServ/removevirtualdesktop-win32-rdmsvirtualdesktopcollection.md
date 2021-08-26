---
title: Método RemoveVirtualDesktop de la Win32_RDMSVirtualDesktopCollection clase
description: Quita un escritorio virtual de la colección de escritorios virtuales.
ms.assetid: 287ebbb2-86db-4b4a-8dbb-ac5472789e72
ms.tgt_platform: multiple
keywords:
- Método RemoveVirtualDesktop Servicios de Escritorio remoto
- Método RemoveVirtualDesktop Servicios de Escritorio remoto , Win32_RDMSVirtualDesktopCollection clase
- Win32_RDMSVirtualDesktopCollection clase Servicios de Escritorio remoto , método RemoveVirtualDesktop
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.RemoveVirtualDesktop
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3deefa38d7c7fcfc3f7942eb809b2ca14e96ea14ee4f2e014cdf3e0069a6ab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009185"
---
# <a name="removevirtualdesktop-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Método RemoveVirtualDesktop de la clase \_ RDMSVirtualDesktopCollection de Win32

Quita un escritorio virtual de la colección de escritorios virtuales.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RemoveVirtualDesktop(
  [in] string VMName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VMName* \[ En\]
</dt> <dd>

Nombre de la máquina virtual que hospeda el escritorio virtual.

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

 

 






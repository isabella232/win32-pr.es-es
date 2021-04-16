---
title: Método RemoveVirtualDesktop de la clase Win32_RDMSVirtualDesktopCollection
description: Quita un escritorio virtual de la colección de escritorios virtuales.
ms.assetid: 287ebbb2-86db-4b4a-8dbb-ac5472789e72
ms.tgt_platform: multiple
keywords:
- Método RemoveVirtualDesktop Servicios de Escritorio remoto
- Método RemoveVirtualDesktop Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de clase Servicios de Escritorio remoto, método RemoveVirtualDesktop
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
ms.openlocfilehash: a468de22d571fa52d37c2ad51d40d492af35384a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533915"
---
# <a name="removevirtualdesktop-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Método RemoveVirtualDesktop de la \_ clase RDMSVirtualDesktopCollection de Win32

Quita un escritorio virtual de la colección de escritorios virtuales.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RemoveVirtualDesktop(
  [in] string VMName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VMName* \[ de\]
</dt> <dd>

El nombre de la máquina virtual que hospeda el escritorio virtual.

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

 

 






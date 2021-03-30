---
title: Método SchedulePatch de la clase Win32_RDMSVirtualDesktopCollection
description: Programa un trabajo de aprovisionamiento de actualizaciones de software que instala las actualizaciones de software en las máquinas virtuales de una colección de escritorios virtuales.
ms.assetid: 780d5709-9e7d-41d9-a4d0-b5d021615655
ms.tgt_platform: multiple
keywords:
- Método SchedulePatch Servicios de Escritorio remoto
- Método SchedulePatch Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de clase Servicios de Escritorio remoto, método SchedulePatch
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SchedulePatch
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d9585e3d13ea1f02115506741c153d62c33fcc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490313"
---
# <a name="schedulepatch-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Método SchedulePatch de la \_ clase RDMSVirtualDesktopCollection de Win32

Programa un trabajo de aprovisionamiento de actualizaciones de software que instala las actualizaciones de software en las máquinas virtuales de una colección de escritorios virtuales.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SchedulePatch(
  [in] DATETIME StartTime,
  [in] DATETIME ForceLogOffTime,
  [in] string   JobInputXml
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StartTime* \[ de\]
</dt> <dd>

> [!Note]  
> El sistema no cerrará la sesión de los usuarios de las máquinas virtuales hasta la hora especificada en el parámetro *ForceLogOffTime* .

 

Fecha y hora de instalación de las actualizaciones.

</dd> <dt>

*ForceLogOffTime* \[ de\]
</dt> <dd>

Fecha y hora en que el sistema cerrará la sesión de los usuarios de las máquinas virtuales.

</dd> <dt>

*JobInputXml* \[ de\]
</dt> <dd>

Cadena con formato XML que contiene la información del trabajo de actualización de software.

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

 

 






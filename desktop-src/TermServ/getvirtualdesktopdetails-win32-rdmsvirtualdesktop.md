---
title: Método GetVirtualDesktopDetails de la clase Win32_RDMSVirtualDesktop
description: Recupera la información adicional sobre el escritorio virtual.
ms.assetid: 487e3a02-4306-4639-a44e-5b9519163a67
ms.tgt_platform: multiple
keywords:
- Método GetVirtualDesktopDetails Servicios de Escritorio remoto
- Método GetVirtualDesktopDetails Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop de clase Servicios de Escritorio remoto, método GetVirtualDesktopDetails
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopDetails
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7382a7ea10b3e557cd7317bdf1ddb0c4bcea55d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491338"
---
# <a name="getvirtualdesktopdetails-method-of-the-win32_rdmsvirtualdesktop-class"></a>Método GetVirtualDesktopDetails de la \_ clase RDMSVirtualDesktop de Win32

Recupera la información adicional sobre el escritorio virtual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetVirtualDesktopDetails(
  [out] uint32  RAMSizeInMB,
  [out] boolean RemoteFXEnabled,
  [out] string  OSVersion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RAMSizeInMB* \[ enuncia\]
</dt> <dd>

Recibe la cantidad de RAM asignada al escritorio virtual, en bytes.

</dd> <dt>

*RemoteFXEnabled* \[ enuncia\]
</dt> <dd>

Recibe un valor que indica si RemoteFX está habilitado en el escritorio virtual. **True** si RemoteFX está habilitado; en caso contrario, **false**.

</dd> <dt>

*OSVersion* \[ enuncia\]
</dt> <dd>

Recibe la versión del sistema operativo del escritorio virtual.

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

[**Win32 \_ RDMSVirtualDesktop**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 






---
title: Método RdvCopyBaseVmLocally de la clase Win32_RdvhManagement
description: Copia una máquina virtual base local en un servidor host de virtualización de escritorio remoto (RDV) especificado.
ms.assetid: 13c0c629-42c6-4689-9740-f13f31688e42
ms.tgt_platform: multiple
keywords:
- Método RdvCopyBaseVmLocally Servicios de Escritorio remoto
- Método RdvCopyBaseVmLocally Servicios de Escritorio remoto, clase Win32_RdvhManagement
- Win32_RdvhManagement de clase Servicios de Escritorio remoto, método RdvCopyBaseVmLocally
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvCopyBaseVmLocally
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d96e01038a4b41edcf32a6a5a9b353403fa6021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422569"
---
# <a name="rdvcopybasevmlocally-method-of-the-win32_rdvhmanagement-class"></a>Método RdvCopyBaseVmLocally de la \_ clase RdvhManagement de Win32

Copia una máquina virtual base local en un servidor host de virtualización de escritorio remoto (RDV) especificado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RdvCopyBaseVmLocally(
  [in] string BaseVmLocation,
  [in] string FarmName,
  [in] string GoldCacheLocation
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*BaseVmLocation* \[ de\]
</dt> <dd>

La ubicación de la máquina virtual base.

</dd> <dt>

*FarmName* \[ de\]
</dt> <dd>

Nombre de la granja de host en la que se va a copiar.

</dd> <dt>

*GoldCacheLocation* \[ de\]
</dt> <dd>

La ubicación de caché Gold.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                             |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ RdvhManagement**](win32-rdvhmanagement.md)
</dt> </dl>

 

 






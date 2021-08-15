---
title: Método RdvCopyBaseVmLocally de la Win32_RdvhManagement clase
description: Copia una máquina virtual base local en un servidor host de virtualización de escritorio remoto (RDV) especificado.
ms.assetid: 13c0c629-42c6-4689-9740-f13f31688e42
ms.tgt_platform: multiple
keywords:
- Método RdvCopyBaseVmLocally Servicios de Escritorio remoto
- Método RdvCopyBaseVmLocally Servicios de Escritorio remoto , Win32_RdvhManagement clase
- Win32_RdvhManagement clase Servicios de Escritorio remoto , método RdvCopyBaseVmLocally
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
ms.openlocfilehash: 76c260f8e9b659ac6e1316fc699ab832174a4aa0d0c24df26daecf5a4895ccd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118852630"
---
# <a name="rdvcopybasevmlocally-method-of-the-win32_rdvhmanagement-class"></a>Método RdvCopyBaseVmLocally de la clase RdvhManagement de Win32 \_

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

*BaseVmLocation* \[ En\]
</dt> <dd>

Ubicación de la máquina virtual base.

</dd> <dt>

*FarmName* \[ En\]
</dt> <dd>

Nombre de la granja de servidores host en la que se copiará.

</dd> <dt>

*GoldCacheLocation* \[ En\]
</dt> <dd>

Ubicación de la caché gold.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                             |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost.mof</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ RdvhManagement**](win32-rdvhmanagement.md)
</dt> </dl>

 

 






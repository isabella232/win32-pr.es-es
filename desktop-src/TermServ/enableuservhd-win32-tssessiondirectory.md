---
title: Método EnableUserVhd de la clase Win32_TSSessionDirectory
description: Habilita un VHD de Perfil de usuario en un servidor RDSH.
ms.assetid: bb39fa19-38eb-4caf-ae81-2bccd901ee2f
ms.tgt_platform: multiple
keywords:
- Método EnableUserVhd Servicios de Escritorio remoto
- Método EnableUserVhd Servicios de Escritorio remoto, clase Win32_TSSessionDirectory
- Win32_TSSessionDirectory de clase Servicios de Escritorio remoto, método EnableUserVhd
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.EnableUserVhd
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 464e105d2f8f0c80126e6b9ca5e5a383b2d17628
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686243"
---
# <a name="enableuservhd-method-of-the-win32_tssessiondirectory-class"></a>Método EnableUserVhd de la \_ clase TSSessionDirectory de Win32

Habilita un VHD de Perfil de usuario en un servidor RDSH.

## <a name="syntax"></a>Sintaxis


```mof
uint32 EnableUserVhd(
  [in] string UvhdShareUrl,
  [in] string UvhdRoamingPolicyXml
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*UvhdShareUrl* \[ de\]
</dt> <dd>

Ubicación del recurso compartido donde se almacenan todos los VHD de Perfil de usuario.

</dd> <dt>

*UvhdRoamingPolicyXml* \[ de\]
</dt> <dd>

La Directiva de itinerancia para el VHD de Perfil de usuario.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

 






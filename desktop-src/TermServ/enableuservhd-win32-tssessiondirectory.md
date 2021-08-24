---
title: Método EnableUserVhd de la Win32_TSSessionDirectory clase
description: Habilita un VHD de perfil de usuario en un servidor RDSH.
ms.assetid: bb39fa19-38eb-4caf-ae81-2bccd901ee2f
ms.tgt_platform: multiple
keywords:
- Método EnableUserVhd Servicios de Escritorio remoto
- Método EnableUserVhd Servicios de Escritorio remoto , Win32_TSSessionDirectory clase
- Win32_TSSessionDirectory clase Servicios de Escritorio remoto , método EnableUserVhd
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
ms.openlocfilehash: 19e042b51c7060e4d4c2a8302a87b2d27ee2cf89608a9831cb3497fd0566689a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871745"
---
# <a name="enableuservhd-method-of-the-win32_tssessiondirectory-class"></a>Método EnableUserVhd de la clase TSSessionDirectory de Win32 \_

Habilita un VHD de perfil de usuario en un servidor RDSH.

## <a name="syntax"></a>Sintaxis


```mof
uint32 EnableUserVhd(
  [in] string UvhdShareUrl,
  [in] string UvhdRoamingPolicyXml
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*UvhdShareUrl* \[ En\]
</dt> <dd>

Ubicación del recurso compartido donde se almacenan todos los discos duros virtuales de perfil de usuario.

</dd> <dt>

*UvhdRoamingPolicyXml* \[ En\]
</dt> <dd>

Directiva de itinerancia para el VHD del perfil de usuario.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                          |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

 






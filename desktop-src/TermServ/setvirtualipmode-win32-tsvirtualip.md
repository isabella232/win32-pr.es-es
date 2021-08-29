---
title: Método SetVirtualIPMode de la Win32_TSVirtualIP clase
description: Establece el valor de la propiedad VirtualIPMode.
ms.assetid: d4b39566-ad2a-493b-8022-c006a857043d
ms.tgt_platform: multiple
keywords:
- Método SetVirtualIPMode Servicios de Escritorio remoto
- Método SetVirtualIPMode Servicios de Escritorio remoto , Win32_TSVirtualIP clase
- Win32_TSVirtualIP clase Servicios de Escritorio remoto , método SetVirtualIPMode
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39ec7007a82d274ca3ab6867eb5a4fe503cac4b37422a9ec8c267aa5f66da1db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058433"
---
# <a name="setvirtualipmode-method-of-the-win32_tsvirtualip-class"></a>Método SetVirtualIPMode de la \_ clase TSVirtualIP de Win32

Establece el **valor de la propiedad VirtualIPMode.**

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetVirtualIPMode(
  [in] uint32 VirtualIPMode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VirtualIPMode* \[ En\]
</dt> <dd>

Tipo: **uint32**

Especifica qué modo de virtualización de IP se usa en el servidor. Puede ser uno de los siguientes valores.

<dt>

0
</dt> <dd>

El modo de virtualización de IP es por sesión.

</dd> <dt>

1
</dt> <dd>

El modo de virtualización de IP es por usuario.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está bajo control de directiva de grupo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                       |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> </dl>

 

 






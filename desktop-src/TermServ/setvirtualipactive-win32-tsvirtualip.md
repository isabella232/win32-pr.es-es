---
title: Método SetVirtualIPActive de la Win32_TSVirtualIP clase
description: Establece el valor de la propiedad VirtualIPActive.
ms.assetid: e485aeb1-afdf-4572-bac7-daa80d903edc
ms.tgt_platform: multiple
keywords:
- Método SetVirtualIPActive Servicios de Escritorio remoto
- Método SetVirtualIPActive Servicios de Escritorio remoto , Win32_TSVirtualIP clase
- Win32_TSVirtualIP clase Servicios de Escritorio remoto , método SetVirtualIPActive
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ab43a007a2a8b04e91d5225e648d5667a87c468cbd52c005d85f4ba6496c919
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118850924"
---
# <a name="setvirtualipactive-method-of-the-win32_tsvirtualip-class"></a>Método SetVirtualIPActive de la clase \_ TSVirtualIP de Win32

Establece el **valor de la propiedad VirtualIPActive.**

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetVirtualIPActive(
  [in] uint32 VirtualIPActive
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VirtualIPActive* \[ En\]
</dt> <dd>

Tipo: **uint32**

Especifica si la virtualización de IP está activa en el servidor. Puede ser uno de los siguientes valores.

<dt>

cero
</dt> <dd>

La virtualización de IP no está activa.

</dd> <dt>

Distinto
</dt> <dd>

La virtualización de IP está activa.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está bajo control de directiva de grupo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 






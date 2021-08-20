---
title: Método SetTSRedirectorMode de la Win32_TSSessionDirectory clase
description: Establece el valor para indicar si el servidor actuará como Servicios de Escritorio remoto redirector.
ms.assetid: abdb92df-1e49-4445-ba02-bb83fd1ca541
ms.tgt_platform: multiple
keywords:
- Método SetTSRedirectorMode Servicios de Escritorio remoto
- Método SetTSRedirectorMode Servicios de Escritorio remoto , Win32_TSSessionDirectory clase
- Win32_TSSessionDirectory clase Servicios de Escritorio remoto , método SetTSRedirectorMode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetTSRedirectorMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6350d4b9a4858991616d45eb2b1092fe406c59b55b11c494a7f19be53dbb60ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127281"
---
# <a name="settsredirectormode-method-of-the-win32_tssessiondirectory-class"></a>Método SetTSRedirectorMode de la clase TSSessionDirectory de Win32 \_

Establece el valor para indicar si el servidor actuará como Servicios de Escritorio remoto redirector.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetTSRedirectorMode(
  [in] uint32 TSRedirValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TSRedirValue* \[ En\]
</dt> <dd>

Tipo: **uint32**

Especifica si el servidor actuará como Servicios de Escritorio remoto redirector. Puede ser uno de los siguientes valores.

<dt>

0
</dt> <dd>

El servidor actuará como un Servicios de Escritorio remoto de red.

</dd> <dt>

1
</dt> <dd>

El servidor no actuará como un Servicios de Escritorio remoto de red.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error WMI. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está bajo control de directiva de grupo.

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                       |
| Fin de compatibilidad de cliente<br/>    | No se admite ninguno<br/>                                                               |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2008 R2<br/>                                                       |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 


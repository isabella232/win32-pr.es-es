---
title: Método SetColorDepthPolicy de la Win32_TSClientSetting clase
description: El método SetColorDepthPolicy establece la propiedad ColorDepthPolicy para la clase .
ms.assetid: 7a8c2b51-5f7a-4188-aae0-0b2d47d043bd
ms.tgt_platform: multiple
keywords:
- Método SetColorDepthPolicy Servicios de Escritorio remoto
- Método SetColorDepthPolicy Servicios de Escritorio remoto , Win32_TSClientSetting clase
- Win32_TSClientSetting clase Servicios de Escritorio remoto , método SetColorDepthPolicy
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepthPolicy
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ecb53500a65c997ace21865492a0a473c2799bd38a3876c4676aaea4120610
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999853"
---
# <a name="setcolordepthpolicy-method-of-the-win32_tsclientsetting-class"></a>Método SetColorDepthPolicy de la clase \_ TSClientSetting de Win32

El **método SetColorDepthPolicy** establece la **propiedad ColorDepthPolicy** para la clase .

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetColorDepthPolicy(
  [in] uint32 ColorDepthPolicy
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ColorDepthPolicy* \[ En\]
</dt> <dd>

Marca que deshabilita o habilita la **propiedad SetColorDepthPolicy,** que especifica si se debe invalidar la configuración de color máxima del usuario.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Habilite la propiedad .

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Deshabilite la propiedad .

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve Correcto si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está bajo control de directiva de grupo.

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TSClientSetting de Win32 \_**](win32-tsclientsetting.md)
</dt> </dl>

 


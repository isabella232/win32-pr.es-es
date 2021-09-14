---
title: Método SetClientWallPaper de la Win32_TSEnvironmentSetting clase
description: El método SetClientWallPaper establece la propiedad ClientWallPaper.
ms.assetid: 08c41df4-5a3c-4799-bb64-61f414814d0c
ms.tgt_platform: multiple
keywords:
- Método SetClientWallPaper Servicios de Escritorio remoto
- Método SetClientWallPaper Servicios de Escritorio remoto , Win32_TSEnvironmentSetting clase
- Win32_TSEnvironmentSetting clase Servicios de Escritorio remoto método , SetClientWallPaper
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.SetClientWallPaper
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ae476134cf526602a059b4714cded6fd6c990e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172774"
---
# <a name="setclientwallpaper-method-of-the-win32_tsenvironmentsetting-class"></a>Método SetClientWallPaper de la clase \_ TSEnvironmentSetting de Win32

El **método SetClientWallPaper** establece la **propiedad ClientWallPaper.**

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetClientWallPaper(
  [in] uint32 ClientWallPaper
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ClientWallPaper* \[ En\]
</dt> <dd>

Marca que deshabilita o habilita la **propiedad ClientWallPaper,** que especifica si la imagen de fondo (o papel tapiz) se muestra en el cliente.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

La imagen de fondo (o fondo de pantalla) no se muestra en el cliente.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

La imagen de fondo (o fondo de pantalla) se muestra en el cliente.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está bajo control de directiva de grupo.

## <a name="remarks"></a>Observaciones

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSEnvironmentSetting**](win32-tsenvironmentsetting.md)
</dt> </dl>

 


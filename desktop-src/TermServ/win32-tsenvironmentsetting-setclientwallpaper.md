---
title: Método SetClientWallPaper de la clase Win32_TSEnvironmentSetting
description: El método SetClientWallPaper establece la propiedad ClientWallPaper.
ms.assetid: 08c41df4-5a3c-4799-bb64-61f414814d0c
ms.tgt_platform: multiple
keywords:
- Método SetClientWallPaper Servicios de Escritorio remoto
- Método SetClientWallPaper Servicios de Escritorio remoto, clase Win32_TSEnvironmentSetting
- Win32_TSEnvironmentSetting de clase Servicios de Escritorio remoto, método SetClientWallPaper
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802095"
---
# <a name="setclientwallpaper-method-of-the-win32_tsenvironmentsetting-class"></a>Método SetClientWallPaper de la \_ clase TSEnvironmentSetting de Win32

El método **SetClientWallPaper** establece la propiedad **ClientWallPaper** .

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetClientWallPaper(
  [in] uint32 ClientWallPaper
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ClientWallPaper* \[ de\]
</dt> <dd>

Marca que deshabilita o habilita la propiedad **ClientWallPaper** , que especifica si se muestra la imagen de fondo (o papel tapiz) en el cliente.

<dt>

<span id="0"></span>

<span id="0"></span>**0,1**


</dt> <dd>

La imagen de fondo (o papel tapiz) no se muestra en el cliente.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

La imagen de fondo (o papel tapiz) se muestra en el cliente.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está en control de directiva de grupo.

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSEnvironmentSetting**](win32-tsenvironmentsetting.md)
</dt> </dl>

 


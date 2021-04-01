---
title: Método SetColorDepth de la clase Win32_TSClientSetting
description: El método SetColorDepth establece la propiedad ColorDepth para la clase.
ms.assetid: 1ab8ac41-cbbf-4077-b91e-692856ccba42
ms.tgt_platform: multiple
keywords:
- Método SetColorDepth Servicios de Escritorio remoto
- Método SetColorDepth Servicios de Escritorio remoto, clase Win32_TSClientSetting
- Win32_TSClientSetting de clase Servicios de Escritorio remoto, método SetColorDepth
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepth
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f2b05c6b8ff02b78f48ff45751bdc8e57ef46a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996979"
---
# <a name="setcolordepth-method-of-the-win32_tsclientsetting-class"></a>Método SetColorDepth de la \_ clase TSClientSetting de Win32

El método **SetColorDepth** establece la propiedad **colorDepth** para la clase.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetColorDepth(
  [in] uint32 ColorDepth
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ColorDepth* \[ de\]
</dt> <dd>

Nuevo valor de la propiedad **colorDepth** .

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

8 bits por píxel

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

15 bits por píxel

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

16 bits por píxel

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

24 bits por píxel

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5**


</dt> <dd>

32 bits por píxel

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve SUCCESS si es correcto; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está en control de directiva de grupo.

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

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 


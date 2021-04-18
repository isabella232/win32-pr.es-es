---
title: Método SetSessionDirectoryProperty de la clase Win32_TSSessionDirectory
description: Establece la propiedad SessionDirectoryLocation o la propiedad SessionDirectoryClusterName de la clase.
ms.assetid: 728e1991-294f-4b80-86f8-a0c2cfd10e9c
ms.tgt_platform: multiple
keywords:
- Método SetSessionDirectoryProperty Servicios de Escritorio remoto
- Método SetSessionDirectoryProperty Servicios de Escritorio remoto, clase Win32_TSSessionDirectory
- Win32_TSSessionDirectory de clase Servicios de Escritorio remoto, método SetSessionDirectoryProperty
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryProperty
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32357e662ec9b2edb05d75a2814d5215fc9ec7f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490084"
---
# <a name="setsessiondirectoryproperty-method-of-the-win32_tssessiondirectory-class"></a>Método SetSessionDirectoryProperty de la \_ clase TSSessionDirectory de Win32

Establece la propiedad **SessionDirectoryLocation** o la propiedad **SessionDirectoryClusterName** de la clase.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetSessionDirectoryProperty(
  [in] string PropertyName,
  [in] string Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NombreDePropiedad* \[ de\]
</dt> <dd>

Tipo: **String**

Especifica la propiedad que está estableciendo el método.

<dt>

<span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>

<span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>**SessionDirectoryLocation**


</dt> <dd>

El método está estableciendo la propiedad **SessionDirectoryLocation** .

</dd> <dt>

<span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>

<span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>**SessionDirectoryClusterName**


</dt> <dd>

El método está estableciendo la propiedad **SessionDirectoryClusterName** .

</dd> </dl> </dd> <dt>

*Valor* \[ de de\]
</dt> <dd>

Tipo: **String**

Nuevo valor de la propiedad especificada por el parámetro *PropertyName* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está en control de directiva de grupo.

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 


---
title: Método SetResources de la clase Win32_TSGatewayResourceGroup
description: Establece la propiedad Resources para este grupo de recursos.
ms.assetid: 0043ee04-26d1-4907-87cc-a15f72cb0b93
ms.tgt_platform: multiple
keywords:
- Método SetResources Servicios de Escritorio remoto
- Método SetResources Servicios de Escritorio remoto, clase Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup de clase Servicios de Escritorio remoto, método SetResources
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23f2ca14597fc7d6ce3660e6e180bf93dfd86cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422121"
---
# <a name="setresources-method-of-the-win32_tsgatewayresourcegroup-class"></a>Método SetResources de la \_ clase TSGatewayResourceGroup de Win32

Establece la propiedad **Resources** para este grupo de recursos.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetResources(
  [in] string Resources
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Recursos* \[ de de\]
</dt> <dd>

Lista de recursos separados por punto y coma en este grupo de recursos. Un " \* " hace referencia a todos los recursos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Si hay varios recursos en el parámetro de *recursos* y no se puede procesar uno de los recursos, no se procesará ninguno de los recursos.

Para llamar a este método, debe ser miembro del grupo administradores.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 


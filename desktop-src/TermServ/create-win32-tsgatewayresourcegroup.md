---
title: Método Create de la Win32_TSGatewayResourceGroup clase
description: Crea un grupo de recursos.
ms.assetid: 715e6086-1c7d-4b20-983a-3ab98e875ca5
ms.tgt_platform: multiple
keywords:
- Creación de métodos Servicios de Escritorio remoto
- Create method Servicios de Escritorio remoto , Win32_TSGatewayResourceGroup class
- Win32_TSGatewayResourceGroup clase Servicios de Escritorio remoto , Método Create
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e4de66eff704ab5d061dcb7675c1ab4ef9d847e5e7235e872f5872b8f3376fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871755"
---
# <a name="create-method-of-the-win32_tsgatewayresourcegroup-class"></a>Método Create de la clase \_ TSGatewayResourceGroup de Win32

Crea un grupo de recursos.

## <a name="syntax"></a>Sintaxis


```mof
uint32 Create(
  [in] string Name,
  [in] string Description,
  [in] string Resources
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* \[ En\]
</dt> <dd>

Nombre del grupo de recursos.

</dd> <dt>

*Descripción* \[ En\]
</dt> <dd>

Descripción del grupo de recursos.

</dd> <dt>

*Recursos* \[ En\]
</dt> <dd>

Lista separada por punto y coma de los recursos de este grupo de recursos. "" \* significa todos los recursos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TSGatewayResourceGroup de Win32 \_**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 


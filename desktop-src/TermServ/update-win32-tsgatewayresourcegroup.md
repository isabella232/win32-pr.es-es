---
title: Método Update de la Win32_TSGatewayResourceGroup clase
description: Actualiza el grupo de recursos.
ms.assetid: b5927046-f461-41cd-861b-0fd77f2008e5
ms.tgt_platform: multiple
keywords:
- Actualización del método Servicios de Escritorio remoto
- Método Update Servicios de Escritorio remoto , Win32_TSGatewayResourceGroup clase
- Win32_TSGatewayResourceGroup clase Servicios de Escritorio remoto método , Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0c2f32e7f0c06f67ad0d32a7754c701097320564c5c01de3c348b9935b8b702
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423915"
---
# <a name="update-method-of-the-win32_tsgatewayresourcegroup-class"></a>Método Update de la clase \_ TSGatewayResourceGroup de Win32

Actualiza el grupo de recursos.

## <a name="syntax"></a>Sintaxis


```mof
uint32 Update(
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

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Observaciones

Si hay varios recursos en el *parámetro Resources* y uno de los recursos no se puede procesar, no se procesará ninguno de los recursos.

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

 


---
title: Método SetName de la Win32_TSGatewayResourceGroup clase
description: Establece la propiedad Name del grupo de recursos.
ms.assetid: 2c2fe1b6-5826-490e-aec2-479a0191e215
ms.tgt_platform: multiple
keywords:
- Método SetName Servicios de Escritorio remoto
- Método SetName Servicios de Escritorio remoto , Win32_TSGatewayResourceGroup clase
- Win32_TSGatewayResourceGroup clase Servicios de Escritorio remoto método , SetName
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36df7688627d059a93a6999493b936967d53e0c7aeaeac15fc51146db0684f85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865215"
---
# <a name="setname-method-of-the-win32_tsgatewayresourcegroup-class"></a>Método SetName de la clase \_ TSGatewayResourceGroup de Win32

Establece la **propiedad Name** del grupo de recursos.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* \[ En\]
</dt> <dd>

Nombre del grupo de recursos. El nombre debe tener 64 caracteres o menos, ser único (se omite case) y no puede contener los siguientes caracteres reservados:

<> : ; " / \\ \| ? \*\[TAB\]

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

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

 


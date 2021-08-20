---
title: Método SetDescription de la Win32_TSGatewayResourceGroup clase
description: Establece la propiedad Description del grupo de recursos.
ms.assetid: ab1280c7-ce53-4807-9537-953b597dd636
ms.tgt_platform: multiple
keywords:
- Método SetDescription Servicios de Escritorio remoto
- Método SetDescription Servicios de Escritorio remoto , Win32_TSGatewayResourceGroup clase
- Win32_TSGatewayResourceGroup clase Servicios de Escritorio remoto , método SetDescription
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetDescription
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d122bae83a9262b20afa50c942f2a79ca00558f810b46ce26fc077db3e49c460
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127490"
---
# <a name="setdescription-method-of-the-win32_tsgatewayresourcegroup-class"></a>Método SetDescription de la clase \_ TSGatewayResourceGroup de Win32

Establece la **propiedad Description** del grupo de recursos.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetDescription(
  [in] string Description
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Descripción* \[ En\]
</dt> <dd>

Descripción del grupo de recursos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 


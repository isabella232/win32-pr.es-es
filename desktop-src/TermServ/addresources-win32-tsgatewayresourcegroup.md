---
title: Método AddResources de la Win32_TSGatewayResourceGroup clase
description: Agrega recursos al grupo de recursos.
ms.assetid: 3210b468-6b82-4edb-ac8b-95f66a7b9328
ms.tgt_platform: multiple
keywords:
- Método AddResources Servicios de Escritorio remoto
- Método AddResources Servicios de Escritorio remoto , Win32_TSGatewayResourceGroup clase
- Win32_TSGatewayResourceGroup clase Servicios de Escritorio remoto , Método AddResources
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.AddResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a37498accf76b28f16e0de45565916c18ab8d9dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172798"
---
# <a name="addresources-method-of-the-win32_tsgatewayresourcegroup-class"></a>Método AddResources de la clase \_ TSGatewayResourceGroup de Win32

Agrega recursos al grupo de recursos.

## <a name="syntax"></a>Sintaxis


```mof
uint32 AddResources(
  [in] string Resources
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Recursos* \[ En\]
</dt> <dd>

Lista separada por punto y coma de los recursos que se van a agregar al grupo de recursos. "" \* significa todos los recursos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no es correcto, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Si hay varios recursos en el *parámetro Resources* y no se puede procesar uno de ellos, no se procesará ninguno de ellos.

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las clases Windows Management Instrumentation (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 


---
title: Método GetCurrentRedirectableAddresses de la Win32_TSSessionDirectory clase
description: Obtiene la lista configurada actualmente de direcciones aptas para DNS que se pueden usar para el redireccionamiento.
ms.assetid: 79f35d8f-b5f9-4b0f-bb7d-0d1ee3f02346
ms.tgt_platform: multiple
keywords:
- Método GetCurrentRedirectableAddresses Servicios de Escritorio remoto
- Método GetCurrentRedirectableAddresses Servicios de Escritorio remoto , Win32_TSSessionDirectory clase
- Win32_TSSessionDirectory clase Servicios de Escritorio remoto , método GetCurrentRedirectableAddresses
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.GetCurrentRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e6b4a859c77f449fb5a8f436be6e18c058ca59f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068636"
---
# <a name="getcurrentredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a>Método GetCurrentRedirectableAddresses de la clase TSSessionDirectory de Win32 \_

Obtiene la lista configurada actualmente de direcciones aptas para DNS que se pueden usar para el redireccionamiento.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetCurrentRedirectableAddresses(
  [out] uint32 fTokenRedirection,
  [out] string IPAddresses[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fTokenRedirection* \[ out\]
</dt> <dd>

Tipo: **uint32**

Marca que indica si se debe usar el redireccionamiento de tokens.

</dd> <dt>

*IPAddresses* \[ out\]
</dt> <dd>

Tipo: **\[ \] cadena**

Matriz de las direcciones IP aptas para DNS configuradas actualmente que se pueden usar para el redireccionamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="remarks"></a>Observaciones

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 


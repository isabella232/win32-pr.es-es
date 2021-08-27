---
title: Método GetRedirectableAddresses de la Win32_TSSessionDirectory clase
description: Obtiene la lista completa de direcciones aptas para DNS.
ms.assetid: 828079e7-472c-4428-97a0-2d5dedcdae91
ms.tgt_platform: multiple
keywords:
- Método GetRedirectableAddresses Servicios de Escritorio remoto
- Método GetRedirectableAddresses Servicios de Escritorio remoto , Win32_TSSessionDirectory clase
- Win32_TSSessionDirectory clase Servicios de Escritorio remoto , método GetRedirectableAddresses
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.GetRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ff3e5dda8459361855c6ff2b287b71cbe02136b906e7defc816d4e7df727a08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010114"
---
# <a name="getredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a>Método GetRedirectableAddresses de la clase TSSessionDirectory de Win32 \_

Obtiene la lista completa de direcciones aptas para DNS.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetRedirectableAddresses(
  [in]  uint32 fTokenRedirection,
  [out] string IPAddresses[],
  [out] string AdapterNames[],
  [out] string NetConName[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fTokenRedirection* \[ En\]
</dt> <dd>

Tipo: **uint32**

Marca que indica si se debe usar el redireccionamiento de tokens.

</dd> <dt>

*IPAddresses* \[ out\]
</dt> <dd>

Tipo: **\[ \] cadena**

Lista completa de direcciones IP que están disponibles para el redireccionamiento.

</dd> <dt>

*AdapterNames* \[ out\]
</dt> <dd>

Tipo: **\[ \] cadena**

Lista de nombres de adaptadores de red asociados a las direcciones que están disponibles para el redireccionamiento.

</dd> <dt>

*NetConName* \[ out\]
</dt> <dd>

Tipo: **\[ \] cadena**

Lista de nombres de conexión de red asociados a las direcciones que están disponibles para el redireccionamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 


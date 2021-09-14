---
title: Método GetRedirectableAddresses de la Win32_TSSessionDirectory clase
description: Obtiene la lista completa de direcciones aptas para DNS.
ms.assetid: 828079e7-472c-4428-97a0-2d5dedcdae91
ms.tgt_platform: multiple
keywords:
- Método GetRedirectableAddresses Servicios de Escritorio remoto
- Método GetRedirectableAddresses Servicios de Escritorio remoto , Win32_TSSessionDirectory clase
- Win32_TSSessionDirectory clase Servicios de Escritorio remoto método , GetRedirectableAddresses
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
ms.openlocfilehash: bd5348c11b5f2aba442f7f13ef06488c6d849be3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073344"
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

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error WMI. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="remarks"></a>Observaciones

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

 


---
title: Método IsTSCGroupPresent de la Win32_TSLicenseServer clase
description: IsTSCGroupPresent ya no está disponible para su uso a Windows Server 2012.
ms.assetid: 2bbb00ff-4fb3-4a7a-a0e7-3daabf97d70a
ms.tgt_platform: multiple
keywords:
- Método IsTSCGroupPresent Servicios de Escritorio remoto
- Método IsTSCGroupPresent Servicios de Escritorio remoto , Win32_TSLicenseServer clase
- Win32_TSLicenseServer clase Servicios de Escritorio remoto , método IsTSCGroupPresent
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsTSCGroupPresent
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4711236541999264a5a6f96066050f709cdcc087a751e0e56ddd6dea1b9103da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351344"
---
# <a name="istscgrouppresent-method-of-the-win32_tslicenseserver-class"></a>Método IsTSCGroupPresent de la clase TSLicenseServer de Win32 \_

\[**IsTSCGroupPresent** ya no está disponible para su uso a Windows Server 2012.\]

No se admite este método.

**Windows Server 2008 R2 y Windows Server 2008:** Recupera si el grupo local Equipos de Terminal Server existe en Escritorio remoto servidor de licencias.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsTSCGroupPresent(
  [out] boolean Present
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Presente* \[ out\]
</dt> <dd>

Valor booleano que indica si existe el grupo local Equipos con Terminal Server.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **WBEM \_ E NOT \_ \_ SUPPORTED**.

**Windows Server 2008 R2 y Windows Server 2008:** Si el método se realiza correctamente, devuelve cero. Si el método no es correcto, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Fin de compatibilidad de cliente<br/>    | No se admite ninguno<br/>                                                                 |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2008 R2<br/>                                                         |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 


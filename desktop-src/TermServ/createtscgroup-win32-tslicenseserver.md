---
title: Método CreateTSCGroup de la Win32_TSLicenseServer clase
description: CreateTSCGroup ya no está disponible para su uso a Windows Server 2012.
ms.assetid: 31751da7-263b-4911-a328-246457a606f0
ms.tgt_platform: multiple
keywords:
- Método CreateTSCGroup Servicios de Escritorio remoto
- Método CreateTSCGroup Servicios de Escritorio remoto , Win32_TSLicenseServer clase
- Win32_TSLicenseServer clase Servicios de Escritorio remoto , método CreateTSCGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.CreateTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf363d86cf663a3f9b626d9586140eb4c00f86e9750070f8a2000149b655bb34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737875"
---
# <a name="createtscgroup-method-of-the-win32_tslicenseserver-class"></a>Método CreateTSCGroup de la clase TSLicenseServer de Win32 \_

\[**CreateTSCGroup** ya no está disponible para su uso a Windows Server 2012.\]

No se admite este método.

**Windows Server 2008 R2 y Windows Server 2008:** Crea el grupo local Equipos de Terminal Server en el Escritorio remoto de licencias.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CreateTSCGroup();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **WBEM \_ E NOT \_ \_ SUPPORTED**.

**Windows Server 2008 R2 y Windows Server 2008:** Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

[**TSLicenseServer de Win32 \_**](win32-tslicenseserver.md)
</dt> <dt>

[**IsTSCGroupPresent**](istscgrouppresent-win32-tslicenseserver.md)
</dt> </dl>

 


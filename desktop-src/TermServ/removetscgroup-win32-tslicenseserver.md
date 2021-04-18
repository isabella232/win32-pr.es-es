---
title: Método RemoveTSCGroup de la clase Win32_TSLicenseServer
description: RemoveTSCGroup ya no está disponible para su uso a partir de Windows Server 2012.
ms.assetid: e5e3eca9-4990-4322-b41d-c6b6b3356272
ms.tgt_platform: multiple
keywords:
- Método RemoveTSCGroup Servicios de Escritorio remoto
- Método RemoveTSCGroup Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método RemoveTSCGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.RemoveTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26ca693e7e98ca811ce52292fb26622b7f2174cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535380"
---
# <a name="removetscgroup-method-of-the-win32_tslicenseserver-class"></a>Método RemoveTSCGroup de la \_ clase TSLicenseServer de Win32

\[**RemoveTSCGroup** ya no está disponible para su uso a partir de Windows Server 2012.\]

No se admite este método.

**Windows server 2008 R2 y Windows server 2008:** Quita el grupo local de Terminal Server equipos del servidor de licencias de Escritorio remoto.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RemoveTSCGroup();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **WBEM \_ E \_ no \_ compatible**.

**Windows server 2008 R2 y Windows server 2008:** Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Para llamar a este método, debe ser miembro del grupo administradores.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Fin de compatibilidad de cliente<br/>    | No se admite ninguno<br/>                                                                 |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2008 R2<br/>                                                         |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> <dt>

[**IsTSCGroupPresent**](istscgrouppresent-win32-tslicenseserver.md)
</dt> </dl>

 


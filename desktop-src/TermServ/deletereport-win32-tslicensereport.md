---
title: Método DeleteReport de la Win32_TSLicenseReport clase
description: Elimina un objeto de informe en el Escritorio remoto de licencias. No se trata de un método estático.
ms.assetid: cc70526c-7ce5-4d55-b72e-8a5e8799b1d8
ms.tgt_platform: multiple
keywords:
- Método DeleteReport Servicios de Escritorio remoto
- Método DeleteReport Servicios de Escritorio remoto , Win32_TSLicenseReport clase
- Win32_TSLicenseReport clase Servicios de Escritorio remoto método , DeleteReport
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.DeleteReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67449da66612368fe5991b43a94037cf4d413f5009af64c51dca58c646ee1d44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513494"
---
# <a name="deletereport-method-of-the-win32_tslicensereport-class"></a>Método DeleteReport de la clase TSLicenseReport de Win32 \_

Elimina un objeto de informe en el Escritorio remoto de licencias. No se trata de un método estático.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DeleteReport();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Comentarios

No se trata de un método estático. Se debe llamar a este método desde un objeto de informe de uso de licencias por usuario.

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TSLicenseReport de Win32 \_**](win32-tslicensereport.md)
</dt> </dl>

 


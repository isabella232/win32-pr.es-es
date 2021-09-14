---
title: Método ActivateServer de la Win32_TSLicenseServer activa
description: Activa el Escritorio remoto de licencias mediante un Escritorio remoto de servidor de licencias que se obtiene a través del teléfono o Internet.
ms.assetid: 628e87f0-600e-404d-a0b4-35f1570b4fc0
ms.tgt_platform: multiple
keywords:
- Método ActivateServer Servicios de Escritorio remoto
- Método ActivateServer Servicios de Escritorio remoto , Win32_TSLicenseServer clase
- Win32_TSLicenseServer clase Servicios de Escritorio remoto , método ActivateServer
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ActivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19db0df0ca9b0bf41fe692ba07fe605dc1e8d5c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073379"
---
# <a name="activateserver-method-of-the-win32_tslicenseserver-class"></a>Método ActivateServer de la clase TSLicenseServer de Win32 \_

Activa el Escritorio remoto de licencias mediante un Escritorio remoto de servidor de licencias que se obtiene a través del teléfono o Internet.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ActivateServer(
  [in]  string sLicenseServerId,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sLicenseServerId* \[ En\]
</dt> <dd>

Escritorio remoto de servidor de licencias que se obtuvo por teléfono o Por Internet. El *parámetro sLicenseServerId* es una cadena alfanumérica de 35 caracteres que no puede incluir guiones.

</dd> <dt>

*ActivationStatus* \[ out\]
</dt> <dd>

El estado de activación devuelto puede ser uno de los siguientes.

<dt>

0
</dt> <dd>

El Escritorio remoto de licencias está activado.

</dd> <dt>

1
</dt> <dd>

El Escritorio remoto de licencias no está activado.

</dd> <dt>

2
</dt> <dd>

Se produjo un error desconocido. No se sabe si el Escritorio remoto de licencias está activado.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no es correcto, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las clases Windows Management Instrumentation (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 


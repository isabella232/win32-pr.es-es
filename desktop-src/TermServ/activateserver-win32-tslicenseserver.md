---
title: Método ActivateServer de la clase Win32_TSLicenseServer
description: Activa el servidor de licencias de Escritorio remoto mediante un identificador de servidor de licencias Escritorio remoto que se obtiene a través del teléfono o Internet.
ms.assetid: 628e87f0-600e-404d-a0b4-35f1570b4fc0
ms.tgt_platform: multiple
keywords:
- Método ActivateServer Servicios de Escritorio remoto
- Método ActivateServer Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método ActivateServer
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686184"
---
# <a name="activateserver-method-of-the-win32_tslicenseserver-class"></a>Método ActivateServer de la \_ clase TSLicenseServer de Win32

Activa el servidor de licencias de Escritorio remoto mediante un identificador de servidor de licencias Escritorio remoto que se obtiene a través del teléfono o Internet.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ActivateServer(
  [in]  string sLicenseServerId,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sLicenseServerId* \[ de\]
</dt> <dd>

Escritorio remoto identificador del servidor de licencias que se obtuvo a través del teléfono o Internet. El parámetro *sLicenseServerId* es una cadena alfanumérica de 35 caracteres que no puede incluir guiones.

</dd> <dt>

*ActivationStatus* \[ enuncia\]
</dt> <dd>

El estado de activación devuelto puede ser uno de los siguientes.

<dt>

0
</dt> <dd>

Se activa el servidor de licencias de Escritorio remoto.

</dd> <dt>

1
</dt> <dd>

El servidor de licencias de Escritorio remoto no está activado.

</dd> <dt>

2
</dt> <dd>

Se ha producido un error desconocido. No se sabe si el servidor de licencias de Escritorio remoto está activado.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Para llamar a este método, debe ser miembro del grupo administradores.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 


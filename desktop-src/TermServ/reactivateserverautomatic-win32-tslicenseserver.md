---
title: Método ReactivateServerAutomatic de la clase Win32_TSLicenseServer
description: Reactiva el servidor de licencias de Escritorio remoto mediante una conexión automática a Internet.
ms.assetid: 98b9b8e5-4de4-418c-9175-58e8b84784d5
ms.tgt_platform: multiple
keywords:
- Método ReactivateServerAutomatic Servicios de Escritorio remoto
- Método ReactivateServerAutomatic Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método ReactivateServerAutomatic
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ReactivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81b9df7314abc3dccf6458322911c50d6120ad10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686166"
---
# <a name="reactivateserverautomatic-method-of-the-win32_tslicenseserver-class"></a>Método ReactivateServerAutomatic de la \_ clase TSLicenseServer de Win32

Reactiva el servidor de licencias de Escritorio remoto mediante una conexión automática a Internet.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ReactivateServerAutomatic(
  [in]  uint32 Reason,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Motivo* \[ de\]
</dt> <dd>

Motivo de la activación. Puede ser uno de los siguientes valores.

<dt>

0
</dt> <dd>

Se volvió a implementar el servidor.

</dd> <dt>

1
</dt> <dd>

El certificado está dañado.

</dd> <dt>

2
</dt> <dd>

La clave privada se ha puesto en peligro.

</dd> <dt>

3
</dt> <dd>

Expiró la clave de activación.

</dd> <dt>

4
</dt> <dd>

El servidor se actualizó.

</dd> </dl> </dd> <dt>

*ActivationStatus* \[ enuncia\]
</dt> <dd>

El estado de activación devuelto puede ser uno de los valores siguientes.

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

 


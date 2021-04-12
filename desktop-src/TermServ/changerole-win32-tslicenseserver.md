---
title: Método ChangeRole de la clase Win32_TSLicenseServer
description: Cambia el ámbito de detección del servidor de licencias de Escritorio remoto. El ámbito de detección determina qué servidores host de sesión de Escritorio remoto (host de sesión de escritorio remoto) de la red pueden detectar automáticamente el servidor de licencias.
ms.assetid: 3d98fd8a-4ade-489f-8edd-5df1227f15cd
ms.tgt_platform: multiple
keywords:
- Método ChangeRole Servicios de Escritorio remoto
- Método ChangeRole Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método ChangeRole
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ChangeRole
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9746b856c74e9603751fe85bb861e2b6869f03a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489688"
---
# <a name="changerole-method-of-the-win32_tslicenseserver-class"></a>Método ChangeRole de la \_ clase TSLicenseServer de Win32

Cambia el ámbito de detección del servidor de licencias de Escritorio remoto. El ámbito de detección determina qué servidores host de sesión de Escritorio remoto (host de sesión de escritorio remoto) de la red pueden detectar automáticamente el servidor de licencias.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ChangeRole(
  [in] uint32 ServerRole
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

Función de la  \[ de\]
</dt> <dd>

Ámbito de detección del servidor de licencias de Escritorio remoto. Puede establecer uno de los valores siguientes.

<dt>

0
</dt> <dd>

Los servidores host de sesión de escritorio remoto del mismo grupo de trabajo pueden detectar el servidor de licencias.

</dd> <dt>

1
</dt> <dd>

Los servidores host de sesión de escritorio remoto del mismo dominio pueden detectar el servidor de licencias. Debe haber iniciado sesión como administrador de dominio para establecer este valor.

</dd> <dt>

2
</dt> <dd>

Los servidores host de sesión de escritorio remoto de varios dominios del mismo bosque pueden detectar el servidor de licencias. Debe haber iniciado sesión como administrador de empresa para establecer este valor.

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

 


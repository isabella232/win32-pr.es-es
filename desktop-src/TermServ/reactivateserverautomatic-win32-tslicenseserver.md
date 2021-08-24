---
title: Método ReactivateServerAutomatic de la Win32_TSLicenseServer clase
description: Reactiva el servidor Escritorio remoto licencias mediante una conexión automática a Internet.
ms.assetid: 98b9b8e5-4de4-418c-9175-58e8b84784d5
ms.tgt_platform: multiple
keywords:
- Método ReactivateServerAutomatic Servicios de Escritorio remoto
- Método ReactivateServerAutomatic Servicios de Escritorio remoto , Win32_TSLicenseServer clase
- Win32_TSLicenseServer clase Servicios de Escritorio remoto , método ReactivateServerAutomatic
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
ms.openlocfilehash: d4e822c441410ae3757f7cdb0a4a714b435facbb20e171646c889e2ea53ec82b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866045"
---
# <a name="reactivateserverautomatic-method-of-the-win32_tslicenseserver-class"></a>Método ReactivateServerAutomatic de la clase TSLicenseServer de Win32 \_

Reactiva el servidor Escritorio remoto licencias mediante una conexión automática a Internet.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ReactivateServerAutomatic(
  [in]  uint32 Reason,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Motivo* \[ En\]
</dt> <dd>

Motivo de la activación. Puede ser uno de los siguientes valores.

<dt>

0
</dt> <dd>

Se ha vuelto a implementar el servidor.

</dd> <dt>

1
</dt> <dd>

El certificado estaba dañado.

</dd> <dt>

2
</dt> <dd>

La clave privada estaba en peligro.

</dd> <dt>

3
</dt> <dd>

La clave de activación expiró.

</dd> <dt>

4
</dt> <dd>

El servidor se actualizó.

</dd> </dl> </dd> <dt>

*ActivationStatus* \[ out\]
</dt> <dd>

El estado de activación devuelto puede ser uno de los siguientes valores.

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

Se produjo un error desconocido. No se sabe si el servidor Escritorio remoto licencias está activado.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

[**TSLicenseServer de Win32 \_**](win32-tslicenseserver.md)
</dt> </dl>

 


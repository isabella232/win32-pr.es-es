---
title: Método RemoveLSfromTSLSGroup de la clase Win32_TSLicenseServer
description: Quita el servidor de licencias de Escritorio remoto del grupo servidores de licencias de Servicios de Escritorio remoto en un controlador de dominio del mismo dominio que el servidor de licencias.
ms.assetid: 5ed4595b-0668-4dd8-953e-b6fc61088cfd
ms.tgt_platform: multiple
keywords:
- Método RemoveLSfromTSLSGroup Servicios de Escritorio remoto
- Método RemoveLSfromTSLSGroup Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método RemoveLSfromTSLSGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.RemoveLSfromTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b60c7a0e6b836b8fcf268942ba5d8eae1304b818
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534414"
---
# <a name="removelsfromtslsgroup-method-of-the-win32_tslicenseserver-class"></a>Método RemoveLSfromTSLSGroup de la \_ clase TSLicenseServer de Win32

Quita el servidor de licencias de Escritorio remoto del grupo servidores de licencias de Servicios de Escritorio remoto en un controlador de dominio del mismo dominio que el servidor de licencias.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RemoveLSfromTSLSGroup();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Para llamar a este método, debe ser miembro del grupo Admins. del dominio.

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

 


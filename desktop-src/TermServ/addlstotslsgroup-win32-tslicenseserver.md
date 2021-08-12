---
title: Método AddLStoTSLSGroup de la Win32_TSLicenseServer clase
description: Agrega el Escritorio remoto de licencias al grupo Servidores de licencias de Conexión a Escritorio remoto Broker (Agente de conexión a Escritorio remoto) en un controlador de dominio en el mismo dominio que el Escritorio remoto de licencias.
ms.assetid: 65c6b7cf-324a-44f1-8dfc-40e35ed45d4f
ms.tgt_platform: multiple
keywords:
- Método AddLStoTSLSGroup Servicios de Escritorio remoto
- Método AddLStoTSLSGroup Servicios de Escritorio remoto , Win32_TSLicenseServer clase
- Win32_TSLicenseServer clase Servicios de Escritorio remoto , método AddLStoTSLSGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.AddLStoTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf3d0464b42159ca1827caf579e21982c08d066495cd664ec1adfcaa883a4b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610410"
---
# <a name="addlstotslsgroup-method-of-the-win32_tslicenseserver-class"></a>Método AddLStoTSLSGroup de la clase TSLicenseServer de Win32 \_

Agrega el Escritorio remoto de licencias al grupo Servidores de licencias de Conexión a Escritorio remoto Broker (Agente de conexión a Escritorio remoto) en un controlador de dominio en el mismo dominio que el Escritorio remoto de licencias.

## <a name="syntax"></a>Sintaxis


```mof
uint32 AddLStoTSLSGroup();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no es correcto, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Debe ser miembro del grupo Administradores de dominio para llamar a este método.

El servidor de licencias debe ser miembro del grupo Escritorio remoto de servidores de licencias si el servidor está configurado para usar el ámbito de detección de dominios o bosques.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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
</dt> <dt>

[**IsLSinTSLSGroup**](islsintslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 


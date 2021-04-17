---
title: Método IsLSinTSLSGroup de la clase Win32_TSLicenseServer
description: Recupera si el servidor de licencias de Escritorio remoto es miembro del grupo de servidores de licencias de Escritorio remoto en un controlador de dominio de un dominio determinado.
ms.assetid: a6ad7f09-8972-47d4-8b3b-cd129b400ea8
ms.tgt_platform: multiple
keywords:
- Método IsLSinTSLSGroup Servicios de Escritorio remoto
- Método IsLSinTSLSGroup Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método IsLSinTSLSGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSinTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de3577e4632167612b4d71841501a2a2845203a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676815"
---
# <a name="islsintslsgroup-method-of-the-win32_tslicenseserver-class"></a>Método IsLSinTSLSGroup de la \_ clase TSLicenseServer de Win32

Recupera si el servidor de licencias de Escritorio remoto es miembro del grupo de servidores de licencias de Escritorio remoto en un controlador de dominio de un dominio determinado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsLSinTSLSGroup(
  [in]  string  Domain,
  [out] boolean IsMember
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Dominio* \[ de de\]
</dt> <dd>

Nombre del dominio.

</dd> <dt>

*IsMember* \[ enuncia\]
</dt> <dd>

Valor booleano que indica si el servidor de licencias es miembro del grupo de servidores de licencias Escritorio remoto en el dominio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Para llamar a este método, debe ser miembro del grupo administradores.

Si no se proporciona ningún nombre de dominio, se consulta un controlador de dominio en el mismo dominio que el servidor de licencias.

El servidor de licencias debe ser miembro del grupo de servidores de licencias de Escritorio remoto si el servidor está configurado para utilizar el ámbito de detección de dominio o bosque. Si el servidor de licencias no es miembro de este grupo, el seguimiento de licencias por usuario y los informes no funcionarán.

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
</dt> <dt>

[**AddLStoTSLSGroup**](addlstotslsgroup-win32-tslicenseserver.md)
</dt> <dt>

[**RemoveLSfromTSLSGroup**](removelsfromtslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 


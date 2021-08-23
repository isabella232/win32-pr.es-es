---
description: Obtiene la Storage de clave raíz para un módulo determinado de la parte pública del TPM Storage clave raíz.
ms.assetid: 08CBEB19-ECF5-4E43-B4A4-0F35987173E1
title: Win32_Tpm::GetSrkADThumbprint (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetSrkADThumbprint
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 9be4b7f02a9b645c29b431a9d974f5871ad5a95fc001e43df17bfe459483974e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004113"
---
# <a name="win32_tpmgetsrkadthumbprint-method"></a>Método \_ Tpm::GetSrkADThumbprint de Win32

Obtiene la Storage de clave raíz para un módulo determinado de la parte pública del TPM Storage clave raíz. La huella digital se usa para indexar las claves raíz de Storage en el servidor Active Directory si la copia de seguridad Active Directory de la información de autorización del propietario del TPM se habilita directiva de grupo configuración.

> [!Note]  
> A partir Windows 10, versión 1607, nunca se hace una copia de seguridad de la autorización del propietario del TPM Active Directory.

 

Solo los administradores locales pueden acceder a este método.

## <a name="syntax"></a>Sintaxis


```C++
uint32 GetSrkADThumbprint(
  [in]  uint8 SrkPublicKeyModulus,
  [out] uint8 SrkADThumbprint
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SrkPublicKeyModulus* \[ En\]
</dt> <dd>

Módulo de la parte pública del TPM Storage clave raíz. También se puede obtener mediante el [**método GetSrkPublicKeyModulus**](win32-tpm-getsrkpublickeymodulus.md) de la [clase \_ TPM Win32.](win32-tpm.md)

</dd> <dt>

*SrkADThumbprint* \[ out\]
</dt> <dd>

Devuelve una matriz de 20 bytes que contiene la huella digital de la clave raíz de almacenamiento para el módulo dado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de [TPM.](../tbs/tbs-return-codes.md)

A continuación se enumeran los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                      |
| Espacio de nombres<br/>                | \\\\.\\ root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tpm de \_ Win32**](win32-tpm.md)
</dt> </dl>

 

 

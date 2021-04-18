---
description: Obtiene la huella digital de la clave raíz de almacenamiento para un módulo determinado de la parte pública de la clave raíz de almacenamiento de TPM.
ms.assetid: 08CBEB19-ECF5-4E43-B4A4-0F35987173E1
title: 'Win32_Tpm:: GetSrkADThumbprint (método)'
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
ms.openlocfilehash: 81e1ec53596a3d5ce469d412e9bd7ca17e1ad8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666377"
---
# <a name="win32_tpmgetsrkadthumbprint-method"></a>Win32 \_ TPM:: GetSrkADThumbprint (método)

Obtiene la huella digital de la clave raíz de almacenamiento para un módulo determinado de la parte pública de la clave raíz de almacenamiento de TPM. La huella digital se utiliza para indizar las claves raíz de almacenamiento en el servidor de Active Directory si la Active Directory copia de seguridad de la información de autorización de propietario de TPM se habilita a través de directiva de grupo configuración.

> [!Note]  
> A partir de Windows 10, versión 1607, nunca se realiza una copia de seguridad de la autorización de propietario de TPM en Active Directory.

 

Este método solo es accesible para los administradores locales.

## <a name="syntax"></a>Sintaxis


```C++
uint32 GetSrkADThumbprint(
  [in]  uint8 SrkPublicKeyModulus,
  [out] uint8 SrkADThumbprint
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SrkPublicKeyModulus* \[ de\]
</dt> <dd>

El módulo de la parte pública de la clave raíz de almacenamiento de TPM. También se puede obtener mediante el método [**GetSrkPublicKeyModulus**](win32-tpm-getsrkpublickeymodulus.md) de la clase [ \_ TPM de Win32](win32-tpm.md) .

</dd> <dt>

*SrkADThumbprint* \[ enuncia\]
</dt> <dd>

Devuelve una matriz de 20 bytes que contiene la huella digital de la clave raíz de almacenamiento para el módulo especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se pueden devolver todos los errores de TPM, así como los errores específicos de los [servicios base de TPM](../tbs/tbs-return-codes.md) .

A continuación se enumeran los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte de la Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                      |
| Espacio de nombres<br/>                | \\\\.\\ \\MicrosoftTpm de \\ seguridad de cimv2 raíz \\<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ TPM. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TPM de Win32 \_**](win32-tpm.md)
</dt> </dl>

 

 

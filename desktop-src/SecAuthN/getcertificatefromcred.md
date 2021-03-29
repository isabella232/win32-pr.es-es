---
description: Obtiene el certificado de la credencial de usuario.
ms.assetid: 3C79D049-89DC-4AF5-8C0A-5B7EBBBD69D3
title: Función GetCertificateFromCred (Lsaidprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificateFromCred
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: 1120e7859080657e2a04202e01a01464694a3450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648303"
---
# <a name="getcertificatefromcred-function"></a>GetCertificateFromCred función)

Obtiene el certificado de la credencial de usuario.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS GetCertificateFromCred(
  _In_  PVOID  ProviderHandle,
  _In_  HANDLE ClientToken,
  _In_  PVOID  SuppliedCred,
  _In_  ULONG  SuppliedCredSize,
  _Out_ PVOID  *CertContext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ProviderHandle* \[ de\]
</dt> <dd>

Identificador del proveedor de identidades.

</dd> <dt>

*ClientToken* \[ de\]
</dt> <dd>

Token del llamador que está recuperando el certificado.

</dd> <dt>

*SuppliedCred* \[ de\]
</dt> <dd>

Puntero a una estructura [**de \_ \_ credenciales proporcionada por SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) que contiene la credencial de un identificador en línea cuyo certificado se solicita. El proveedor de identidades debe validar los datos de entrada como si provinieran de un origen que no es de confianza.

</dd> <dt>

*SuppliedCredSize* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer *SuppliedCred* .

</dd> <dt>

*CertContext* \[ enuncia\]
</dt> <dd>

Si la función se ejecuta correctamente, este parámetro es un puntero al puntero de contexto CCERT devuelto \_ . Cuando haya terminado de usar el contexto del certificado, suéltelo llamando a la función [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, la función devuelve el estado \_ Success.

Si se produce un error en la función, la función puede devolver uno de los siguientes códigos de error de NTSTATUS.



| Valor devuelto                                                                                            | Descripción                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>ESTADO \_ no \_ admitido</dt> </dl>       | El proveedor de identidades no reconoce el tipo de credencial de la credencial proporcionada. LSA probará el siguiente proveedor de identidades.<br/>                                           |
| <dl> <dt>error de inicio de sesión de estado \_ \_</dt> </dl>       | La credencial es incorrecta.<br/>                                                                                                                                                |
| <dl> <dt>ESTADO \_ parámetro no válido \_</dt> </dl>   | Un parámetro no es válido. La credencial puede tener un formato incorrecto y no estar en la estructura [**de \_ \_ credenciales proporcionada por SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) definida.<br/> |
| <dl> <dt>Estado de \_ red no \_ accesible</dt> </dl> | El proveedor de identidades no puede ponerse en contacto con la nube para obtener el certificado.<br/>                                                                                                   |
| <dl> <dt>contraseña de estado \_ \_ expirada</dt> </dl>    | La contraseña de la cuenta ha caducado.<br/>                                                                                                                                           |
| <dl> <dt>cuenta de estado \_ \_ bloqueada \_</dt> </dl> | La cuenta se ha bloqueado. <br/>                                                                                                                                           |
| <dl> <dt>Otros</dt> </dl>                       | Otros códigos de error específicos del proveedor. <br/>                                                                                                                                       |



 

## <a name="remarks"></a>Observaciones

Antes de recuperar el certificado de la nube, el proveedor de identidades debe comprobar que hay un certificado válido para este usuario en el almacén de certificados "mi" del usuario. Si existe un certificado válido, el proveedor debe devolver este certificado para evitar el tráfico de red innecesario.

El proveedor de identidades también puede almacenar en caché el certificado localmente siempre que esté protegido por el usuario actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Lsaidprov. h</dt> </dl> |



 


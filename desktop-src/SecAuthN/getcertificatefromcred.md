---
description: Obtiene el certificado de la credencial de usuario.
ms.assetid: 3C79D049-89DC-4AF5-8C0A-5B7EBBBD69D3
title: Función GetCertificateFromCred (Lsaidprov.h)
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
ms.openlocfilehash: 3660fd4cfb8baa3e025789a2cde9dc04dd7e1e1678b0516a56562f1ea5be43dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994494"
---
# <a name="getcertificatefromcred-function"></a>Función GetCertificateFromCred

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

*ProviderHandle* \[ En\]
</dt> <dd>

Identificador del proveedor de identidades.

</dd> <dt>

*ClientToken* \[ En\]
</dt> <dd>

Token del autor de la llamada que está recuperando el certificado.

</dd> <dt>

*SuppliedCred* \[ En\]
</dt> <dd>

Puntero a una [**estructura \_ \_ CREDENTIAL PROPORCIONADA POR SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) que contiene la credencial de un identificador en línea cuyo certificado se solicita. El proveedor de identidades debe validar los datos de entrada como si se tratase de un origen que no es de confianza.

</dd> <dt>

*SuppliedCredSize* \[ En\]
</dt> <dd>

Tamaño, en bytes, del *búfer SuppliedCred.*

</dd> <dt>

*CertContext* \[ out\]
</dt> <dd>

Si la función se realiza correctamente, este parámetro es un puntero al puntero CONTEXT de CCERT \_ devuelto. Cuando haya terminado de usar el contexto de certificado, descálelo llamando a la [**función CertFreeCertificateContext.**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve STATUS \_ SUCCESS.

Si se produce un error en la función, la función puede devolver uno de los siguientes códigos de error NTSTATUS.



| Valor devuelto                                                                                            | Descripción                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>ESTADO \_ NO \_ ADMITIDO</dt> </dl>       | El proveedor de identidades no reconoce el tipo de credencial de la credencial proporcionada. LSA probará el siguiente proveedor de identidades.<br/>                                           |
| <dl> <dt>ERROR DE \_ INICIO DE SESIÓN DE \_ ESTADO</dt> </dl>       | La credencial es incorrecta.<br/>                                                                                                                                                |
| <dl> <dt>PARÁMETRO STATUS \_ INVALID \_</dt> </dl>   | Un parámetro no es válido. La credencial puede estar en un formato incorrecto y no en la estructura [**SECPKG \_ \_ CREDENTIAL proporcionada**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) definida.<br/> |
| <dl> <dt>RED \_ DE ESTADO \_ INACCESIBLE</dt> </dl> | El proveedor de identidades no puede ponerse en contacto con la nube para obtener el certificado.<br/>                                                                                                   |
| <dl> <dt>CONTRASEÑA DE \_ ESTADO \_ EXPIRADA</dt> </dl>    | La contraseña de la cuenta ha caducado.<br/>                                                                                                                                           |
| <dl> <dt>CUENTA \_ DE ESTADO \_ BLOQUEADA \_</dt> </dl> | La cuenta se ha bloqueado. <br/>                                                                                                                                           |
| <dl> <dt>Otros</dt> </dl>                       | Otros códigos de error específicos del proveedor. <br/>                                                                                                                                       |



 

## <a name="remarks"></a>Comentarios

Antes de capturar el certificado de la nube, el proveedor de identidades debe comprobar que hay un certificado válido para este usuario en el almacén de certificados "MY" del usuario. Si existe un certificado válido, el proveedor debe devolver este certificado para evitar tráfico de red innecesario.

El proveedor de identidades también puede almacenar en caché el certificado localmente siempre que esté protegido del usuario actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Lsaidprov.h</dt> </dl> |



 


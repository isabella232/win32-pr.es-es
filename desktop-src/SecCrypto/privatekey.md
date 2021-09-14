---
description: Representa la clave privada asociada a un certificado.
ms.assetid: 26ad1d1c-17c5-4191-ac97-b911e62b4119
title: Objeto PrivateKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e87ca7a5bf12bbaf943bccacaa075a51ae75ed37
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170898"
---
# <a name="privatekey-object"></a>Objeto PrivateKey

\[El **objeto PrivateKey** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la propiedad [**X509Certificate2.PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **objeto PrivateKey** representa la [*clave privada asociada*](../secgloss/p-gly.md) a un certificado.

## <a name="when-to-use"></a>Cuándo se usa

El **objeto PrivateKey** se usa para realizar las siguientes tareas:

-   Recupera información sobre la clave privada.
-   Abra el contenedor de claves privadas.
-   Elimine la clave privada.

## <a name="members"></a>Members

El **objeto PrivateKey** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto PrivateKey** tiene estos métodos.



| Método                                                  | Descripción                                                                                                                                                          |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Eliminar**](privatekey-delete.md)                     | Elimina el contenedor de claves privadas al que hace referencia el **objeto PrivateKey.**<br/>                                                                                |
| [**IsAccessible**](privatekey-isaccessible.md)         | Recupera un valor booleano que indica si el usuario puede acceder a la clave privada. Si es true, el usuario puede acceder a la clave privada.<br/>                 |
| [**IsExportable**](privatekey-isexportable.md)         | Recupera un valor booleano que indica si se puede exportar la clave privada. Si es true, se puede exportar la clave privada.<br/>                               |
| [**IsHardwareDevice**](privatekey-ishardwaredevice.md) | Recupera un valor booleano que indica si la clave privada se almacena en un dispositivo de hardware. Si es true, la clave privada se almacena en un dispositivo de hardware.<br/> |
| [**IsMachineKeyset**](privatekey-ismachinekeyset.md)   | Recupera un valor booleano que indica si la clave privada es una clave de máquina. Si es true, la clave privada es una clave de máquina.<br/>                             |
| [**IsProtected**](privatekey-isprotected.md)           | Recupera un valor booleano que indica si la clave privada está protegida. Si es true, la clave privada está protegida.<br/>                                     |
| [**IsRemovable**](privatekey-isremovable.md)           | Recupera un valor booleano que indica si la clave privada está en un dispositivo extraíble. Si es true, la clave privada está en un dispositivo extraíble.<br/>             |
| [**Abrir**](privatekey-open.md)                         | Accede a un contenedor de claves existente.<br/>                                                                                                                       |



 

### <a name="properties"></a>Propiedades

El **objeto PrivateKey** tiene estas propiedades.



| Propiedad                                                                 | Tipo de acceso          | Descripción                                                                                               |
|:-------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------|
| [**ContainerName**](privatekey-containername.md)<br/>             | Solo lectura<br/> | Recupera una cadena que contiene el nombre del contenedor de claves privadas. Esta es la propiedad predeterminada.<br/> |
| [**KeySpec**](privatekey-keyspec.md)<br/>                         | Solo lectura<br/> | Recupera la especificación de clave.<br/>                                                               |
| [**ProviderName**](privatekey-providername.md)<br/>               | Solo lectura<br/> | Recupera una cadena que contiene el nombre del CSP.<br/>                                          |
| [**ProviderType**](privatekey-providertype.md)<br/>               | Solo lectura<br/> | Recupera un valor de enumeración que especifica el tipo de proveedor.<br/>                            |
| [**UniqueContainerName**](privatekey-uniquecontainername.md)<br/> | Solo lectura<br/> | Recupera una cadena que contiene el nombre único del contenedor de claves privadas.<br/>                        |



 

## <a name="remarks"></a>Observaciones

Se puede crear el objeto **PrivateKey** y es seguro para el scripting. El ProgID del **objeto PrivateKey** es CAPICOM. PrivateKey.1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

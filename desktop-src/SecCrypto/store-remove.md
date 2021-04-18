---
description: El método Remove quita un certificado de un almacén de certificados abierto. Este método solo se puede usar con un almacén que se ha abierto con permisos de lectura y escritura.
ms.assetid: 02bb8ff1-2240-4ec7-b8af-9a7812a12ba9
title: Store. Remove (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 188553d6091314e1a872145219ea321d581b35c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670711"
---
# <a name="storeremove-method"></a>Store. Remove (método)

\[El método **Remove** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El método **Remove** quita un [*certificado*](../secgloss/c-gly.md) de un [*almacén de certificados*](../secgloss/c-gly.md)abierto. Este método solo se puede usar con un almacén que se ha abierto con permisos de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Store.Remove( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Certificado* \[ de de\]
</dt> <dd>

Expresión que se resuelve como una instancia de un objeto de [**certificado**](certificate.md) que se va a quitar del almacén.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

> [!IMPORTANT]
> Cuando se llama a este método desde un script Web, el script debe eliminar los certificados digitales del equipo local. Permitir que los sitios web que no son de confianza eliminen los certificados digitales es un riesgo para la seguridad. Un cuadro de diálogo que pregunta si el sitio web puede eliminar certificados aparece cuando se llama a este método por primera vez. Si permite que la aplicación elimine certificados y selecciona "no volver a mostrar este cuadro de diálogo", el cuadro de diálogo ya no aparecerá para ningún script que elimine los certificados de ese dominio. Sin embargo, los scripts que se encuentren fuera del dominio y que intenten eliminar certificados seguirán apareciendo este cuadro de diálogo. Si no permite que el script elimine certificados y selecciona "no volver a mostrar este cuadro de diálogo", se rechazará automáticamente la capacidad de eliminar certificados de los scripts dentro de ese dominio.

 

Al eliminar un certificado de un almacén, primero debe eliminar la clave privada asociada con el certificado.

Si el almacén no está abierto con permiso de lectura y escritura, este método produce un error. Aunque este método se puede utilizar con almacenes de memoria, los cambios realizados en un almacén de memoria no se conservan cuando se cierra el almacén.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Store**](store.md)
</dt> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> </dl>

 

 

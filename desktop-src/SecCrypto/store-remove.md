---
description: El método Remove quita un certificado de un almacén de certificados abierto. Este método solo se puede usar con un almacén que se ha abierto con permiso de lectura y escritura.
ms.assetid: 02bb8ff1-2240-4ec7-b8af-9a7812a12ba9
title: Método Store.Remove
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473452"
---
# <a name="storeremove-method"></a>Método Store.Remove

\[El **método Remove** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método Remove** quita un certificado [*de*](../secgloss/c-gly.md) un almacén de [*certificados abierto.*](../secgloss/c-gly.md) Este método solo se puede usar con un almacén que se ha abierto con permiso de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Store.Remove( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Certificado* \[ En\]
</dt> <dd>

Expresión que se resuelve en una instancia de un [**objeto Certificate**](certificate.md) que se va a quitar del almacén.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

> [!IMPORTANT]
> Cuando se llama a este método desde un script web, el script debe eliminar certificados digitales del equipo local. Permitir que los sitios web que no son de confianza eliminen certificados digitales es un riesgo para la seguridad. Aparece un cuadro de diálogo que pregunta si el sitio web puede eliminar certificados cuando se llama por primera vez a este método. Si permite que la aplicación elimine certificados y selecciona "No volver a mostrar este cuadro de diálogo", el cuadro de diálogo ya no aparecerá para ningún script que elimine certificados dentro de ese dominio. Sin embargo, los scripts fuera de ese dominio que intenten eliminar certificados seguirán haciendo que aparezca este cuadro de diálogo. Si no permite que el script elimine certificados y selecciona "No volver a mostrar este cuadro de diálogo", se denegará automáticamente la capacidad de eliminar certificados a los scripts de ese dominio.

 

Al eliminar un certificado de un almacén, primero debe eliminar la clave privada asociada al certificado.

Si el almacén no está abierto con permiso de lectura y escritura, se produce un error en este método. Aunque este método se puede usar con almacenes de memoria, los cambios realizados en un almacén de memoria no se conservan cuando se cierra el almacén.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tienda**](store.md)
</dt> <dt>

[**Objetos criptografía**](cryptography-objects.md)
</dt> </dl>

 

 

---
description: Agrega un objeto de certificado a un almacén de certificados abierto.
ms.assetid: 787b8a41-dcdb-4b5b-a1fd-f5424300361b
title: Store. Add (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6d217c784fa5f994e88ee2de78f2e1944091d724
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671233"
---
# <a name="storeadd-method"></a>Store. Add (método)

\[El método **Add** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El método **Add** agrega un objeto de [**certificado**](certificate.md) a un [*almacén de certificados*](../secgloss/c-gly.md)abierto. Este método solo se puede usar con un almacén que se ha abierto con permisos de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Store.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Certificado* \[ de de\]
</dt> <dd>

Expresión que se resuelve como un objeto de [**certificado**](certificate.md) que se va a agregar al almacén.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

> [!IMPORTANT]
> Cuando se llama a este método en un almacén del sistema desde un script Web, el script debe tener acceso a los certificados digitales en el equipo local. Si permite que el script tenga acceso a los certificados digitales, el sitio web desde el que se ejecuta el script también obtendrá acceso a cualquier información personal almacenada en los certificados. La primera vez que se llama a este método desde un dominio determinado, se genera un cuadro de diálogo en el que el usuario debe indicar si se debe permitir el acceso a los certificados.

 

Si el almacén no está abierto en modo de lectura/escritura, este método produce un error. Aunque este método se puede utilizar con almacenes de memoria, los cambios realizados en un almacén de memoria no se conservan cuando se cierra el almacén.

Si el certificado que se va a agregar al almacén es el mismo que el que ya existe, el método **Add** elimina el certificado existente del almacén y, a continuación, agrega el nuevo certificado. El nuevo certificado hereda las propiedades del certificado existente.

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

 

 

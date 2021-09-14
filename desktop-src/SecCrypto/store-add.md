---
description: Agrega un objeto Certificate a un almacén de certificados abierto.
ms.assetid: 787b8a41-dcdb-4b5b-a1fd-f5424300361b
title: Método Store.Add
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170865"
---
# <a name="storeadd-method"></a>Método Store.Add

\[El **método Add** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método Add** agrega un objeto [**Certificate**](certificate.md) a un almacén de [*certificados abierto.*](../secgloss/c-gly.md) Este método solo se puede usar con un almacén que se ha abierto con permiso de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Store.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Certificado* \[ En\]
</dt> <dd>

Expresión que se resuelve en un [**objeto Certificate**](certificate.md) que se va a agregar al almacén.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

> [!IMPORTANT]
> Cuando se llama a este método en un almacén del sistema desde un script web, el script debe tener acceso a los certificados digitales en el equipo local. Si permite que el script acceda a los certificados digitales, el sitio web desde el que se ejecuta el script también obtendrá acceso a cualquier información personal almacenada en los certificados. La primera vez que se llama a este método desde un dominio determinado, se genera un cuadro de diálogo en el que el usuario debe indicar si se debe permitir el acceso a los certificados.

 

Si el almacén no está abierto en modo de lectura y escritura, se produce un error en este método. Aunque este método se puede usar con almacenes de memoria, los cambios realizados en un almacén de memoria no se conservan cuando se cierra el almacén.

Si el certificado que se agrega al almacén es el mismo que el que ya existe, el método **Add** elimina el certificado existente del almacén y, a continuación, agrega el nuevo certificado. El nuevo certificado hereda las propiedades del certificado existente.

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

 

 

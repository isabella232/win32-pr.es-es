---
description: El método Import copia en un almacén de certificados abierto el contenido de un almacén de certificados exportado previamente. Este método solo se puede usar con un almacén que se ha abierto con permiso de lectura y escritura.
ms.assetid: 22db8f1c-469b-4baf-9039-4da35c9c6aa0
title: Método Store.Import
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4eb16cc341eb6e5dcee87216a52e9e3de94d1b65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071147"
---
# <a name="storeimport-method"></a>Método Store.Import

\[El **método** Import está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método Import** copia en un almacén de certificados [*abierto*](../secgloss/c-gly.md) el contenido de un almacén de certificados exportado previamente. Este método solo se puede usar con un almacén que se ha abierto con permiso de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Store.Import( _
  ByVal EncodedStore _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EncodedStore* \[ En\]
</dt> <dd>

Cadena que contiene los certificados codificados que se importarán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

> [!IMPORTANT]
> Cuando se llama a este método desde un script web, el script debe tener acceso a los certificados digitales en el equipo local. Si permite que el script acceda a los certificados digitales, el sitio web desde el que se ejecuta el script también obtendrá acceso a cualquier información personal almacenada en los certificados. La primera vez que se llama a este método desde un dominio determinado, se genera un cuadro de diálogo en el que el usuario debe indicar si se debe permitir el acceso a los certificados.

 

Si el almacén no se abre con permiso de lectura y escritura, se produce un error en este método. Aunque este método se puede usar con almacenes de memoria, los cambios realizados en un almacén de memoria no se conservan cuando se cierra el almacén.

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

 

 

---
description: El método de importación copia en un certificado abierto almacena el contenido de un almacén de certificados exportado previamente. Este método solo se puede usar con un almacén que se ha abierto con permisos de lectura y escritura.
ms.assetid: 22db8f1c-469b-4baf-9039-4da35c9c6aa0
title: Store. Import (método)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650017"
---
# <a name="storeimport-method"></a>Store. Import (método)

\[El método de **importación** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El método de **importación** copia en un [*certificado abierto almacena*](../secgloss/c-gly.md) el contenido de un almacén de certificados exportado previamente. Este método solo se puede usar con un almacén que se ha abierto con permisos de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Store.Import( _
  ByVal EncodedStore _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EncodedStore* \[ de\]
</dt> <dd>

Cadena que contiene los certificados codificados que se van a importar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

> [!IMPORTANT]
> Cuando se llama a este método desde un script Web, el script debe tener acceso a los certificados digitales en el equipo local. Si permite que el script tenga acceso a los certificados digitales, el sitio web desde el que se ejecuta el script también obtendrá acceso a cualquier información personal almacenada en los certificados. La primera vez que se llama a este método desde un dominio determinado, se genera un cuadro de diálogo en el que el usuario debe indicar si se debe permitir el acceso a los certificados.

 

Si el almacén no se abre con permiso de lectura y escritura, este método produce un error. Aunque este método se puede utilizar con almacenes de memoria, los cambios realizados en un almacén de memoria no se conservan cuando se cierra el almacén.

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

 

 

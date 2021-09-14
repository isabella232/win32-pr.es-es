---
description: El método SourceListAddSource agrega una red o un origen de dirección URL. Acepta SourcePath, Type e Index como parámetros. Este método llama a MsiSourceListAddSourceEx.
ms.assetid: 61a8873f-c4ad-43d7-8bbb-5a2534ef2de7
title: Método Product.SourceListAddSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListAddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e0cfda9b8eab0e7dd00afd15eb701a6e7decf2ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069788"
---
# <a name="productsourcelistaddsource-method"></a>Método Product.SourceListAddSource

El **método SourceListAddSource** agrega una red o un origen de dirección URL. Acepta *SourcePath,**Type* e *Index* como parámetros. Este método llama [**a MsiSourceListAddSourceEx.**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)

## <a name="syntax"></a>Sintaxis


```JScript
Product.SourceListAddSource(
  Type,
  SourcePath,
  Index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Tipo* 
</dt> <dd>

Tipo de origen que se va a agregar: MSISOURCETYPE \_ NETWORK o MSISOURCETYPE \_ URL.

</dd> <dt>

*SourcePath* 
</dt> <dd>

Ruta de acceso al origen que se va a agregar.

</dd> <dt>

*Index* 
</dt> <dd>

Si se llama a **SourceListAddSource** con un nuevo origen y *Index* se establece en 0, el instalador agrega el origen al final de la lista de origen.

Si se llama a esta función con un origen ya existente en la lista de origen y *Index* se establece en 0, el instalador conserva el índice existente del origen.

Si se llama a la función con un origen existente en la lista de origen y *Index* se establece en un valor distinto de cero, el origen se quita de su ubicación actual en la lista y se inserta en la posición especificada por *Index*, antes de cualquier origen que ya exista en esa posición.

Si se llama a la función con un nuevo origen y *Index* se establece en un valor distinto de cero, el origen se inserta en la posición especificada por *Index*, antes de cualquier origen que ya exista en esa posición. El valor de índice de todos los orígenes de la lista después de que el índice especificado por *Index* se actualice para garantizar que los valores de índice únicos y el orden preexistido permanezcan sin cambios.

Si *Index* es mayor que el número de orígenes de la lista, el origen se coloca al final de la lista con un valor de índice uno mayor que cualquier origen existente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct se define como \_ 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Producto**](product-object.md)
</dt> <dt>

[**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





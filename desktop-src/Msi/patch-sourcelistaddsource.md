---
description: El método SourceListAddSource agrega un origen de red o dirección URL. Acepta SourcePath, Type e Index como parámetros. Este método llama a MsiSourceListAddSourceEx.
ms.assetid: 87797a8c-f1ba-4bfb-9296-3d3ef2a3c37f
title: Patch.SourceListAddSource (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListAddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 712551a31868ad3a97738ce9f49c9b0ff3526cf33cbae0ca5dd284f701869666
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519605"
---
# <a name="patchsourcelistaddsource-method"></a>Patch.SourceListAddSource (método)

El **método SourceListAddSource** agrega un origen de red o dirección URL. Acepta *SourcePath*, *Type* e *Index* como parámetros. Este método llama a [**MsiSourceListAddSourceEx.**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)

## <a name="syntax"></a>Sintaxis


```JScript
Patch.SourceListAddSource(
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

Si se llama a **SourceListAddSource** con un nuevo origen e *Índice* establecido en 0, el instalador agrega el origen al final de la lista de origen.

Si se llama a esta función con un origen ya existente en la lista de origen e *Index* se establece en 0, el instalador conserva el índice existente del origen.

Si se llama a la función con un origen existente en la lista de origen e *Index* se establece en un valor distinto de cero, el origen se quita de su ubicación actual en la lista y se inserta en la posición especificada por *Index*, antes de cualquier origen que ya exista en esa posición.

Si se llama a la función con un nuevo origen y *Index* se establece en un valor distinto de cero, el origen se inserta en la posición especificada por *Index*, antes de cualquier origen que ya exista en esa posición. El valor de índice de todos los orígenes de la lista después de actualizar el índice especificado por *Index* para garantizar que los valores de índice únicos y el orden preexistido permanezcan sin cambios.

Si *Index* es mayor que el número de orígenes de la lista, el origen se coloca al final de la lista con un valor de índice uno mayor que cualquier origen existente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IPatch se define como \_ 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Parche**](patch-object.md)
</dt> <dt>

[**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





---
description: La función RemoveFromBlob elimina cualquier nivel de entrada de BLOB (propietario, categoría o etiqueta).
ms.assetid: b8bb01e0-8b97-4c95-96f5-f2a30c8700e9
title: Función RemoveFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RemoveFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a23e4e7e6e6d5c85b1284f8aaba49c1f8eae728d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677347"
---
# <a name="removefromblob-function"></a>RemoveFromBlob función)

La función **RemoveFromBlob** elimina cualquier nivel de entrada de BLOB (**propietario**, **categoría** o **etiqueta**).

## <a name="syntax"></a>Sintaxis


```C++
DWORD RemoveFromBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hBlob* \[ de\]
</dt> <dd>

Identificador del BLOB del que se elimina una entrada.

</dd> <dt>

*pOwnerName* \[ de\]
</dt> <dd>

Puntero al nombre del **propietario** .

</dd> <dt>

*pCategoryName* \[ de\]
</dt> <dd>

Puntero al nombre de la **categoría** . Un valor de parámetro **null** indica que el autor de la llamada está intentando eliminar la información de **propietario** especificada y todas sus entradas secundarias. Tenga en cuenta que si el valor del parámetro *pCategoryName* es **null**, el parámetro *pTagName* también debe ser **null**.

</dd> <dt>

*pTagName* \[ de\]
</dt> <dd>

Puntero al nombre de la **etiqueta** . Un valor _PTagName_ **nulo** indica que el autor de la llamada está intentando eliminar la **categoría** especificada y todas sus entradas secundarias. Si el valor del parámetro no es **null**, el autor de la llamada solicita que solo se eliminen las entradas especificadas de la **etiqueta** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 





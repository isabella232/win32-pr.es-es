---
description: La función RemoveFromBlob elimina cualquier nivel de entrada BLOB (Propietario, Categoría o Etiqueta).
ms.assetid: b8bb01e0-8b97-4c95-96f5-f2a30c8700e9
title: Función RemoveFromBlob (Netmon.h)
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
ms.openlocfilehash: 09c9c7f5ada320f33d38cd9e935add7e47721c554fbeed11c35a1b73248d963c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063695"
---
# <a name="removefromblob-function"></a>Función RemoveFromBlob

La **función RemoveFromBlob** elimina cualquier nivel de entrada BLOB **(Propietario,** **Categoría** o **Etiqueta**).

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

*hBlob* \[ En\]
</dt> <dd>

Identificador del BLOB del que se elimina una entrada.

</dd> <dt>

*pOwnerName* \[ En\]
</dt> <dd>

Puntero al nombre **del** propietario.

</dd> <dt>

*pCategoryName* \[ En\]
</dt> <dd>

Puntero al nombre **de** categoría. Un valor de parámetro **NULL** indica que el autor de la llamada está intentando eliminar la información **de propietario** dada y todas sus entradas secundarias. Tenga en cuenta que si el *valor del parámetro pCategoryName* **es NULL,** el *parámetro pTagName* también debe ser **NULL.**

</dd> <dt>

*pTagName* \[ En\]
</dt> <dd>

Puntero al nombre **de la** etiqueta. Un valor  _pTagName_ NULL indica que el autor de la llamada está intentando eliminar la categoría dada y todas sus entradas secundarias. Si el valor del parámetro no es **NULL,** el autor de la llamada pide que solo se eliminen las entradas **de** etiqueta especificadas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto es un valor NMERR que indica el error.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 





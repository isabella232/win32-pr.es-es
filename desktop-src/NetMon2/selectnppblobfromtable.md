---
description: La función SelectNPPBlobFromTable selecciona una NIC de una tabla de BLOB de NPP proporcionada.
ms.assetid: 7f8010ed-472a-49b2-8d97-92851b6c14cd
title: Función SelectNPPBlobFromTable (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectNPPBlobFromTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d8f504d76d43b8a398947f435f7bd488678ea394
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260388"
---
# <a name="selectnppblobfromtable-function"></a>Función SelectNPPBlobFromTable

La **función SelectNPPBlobFromTable** selecciona una NIC de una tabla de BLOB de NPP proporcionada.

## <a name="syntax"></a>Sintaxis


```C++
DWORD SelectNPPBlobFromTable(
  _In_  HWND        hwnd,
  _In_  PBLOB_TABLE pBlobTable,
  _Out_ HBLOB       *hBlob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwnd* \[ En\]
</dt> <dd>

Identificador de la ventana que muestra el **cuadro de diálogo Seleccionar** una red.

</dd> <dt>

*pBlobTable* \[ En\]
</dt> <dd>

Puntero a la tabla BLOB proporcionada. Monitor de red esta tabla para rellenar el **cuadro de diálogo Seleccionar** una red.

</dd> <dt>

*hBlob* \[ out\]
</dt> <dd>

Controle el BLOB que representa la NIC seleccionada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente y el usuario selecciona una NIC, el valor devuelto es NMERR SUCCESS; el BLOB al que \_ *apunta hBlob* se rellena.

Si el usuario no selecciona una NIC, el valor devuelto es NMERR \_ NO \_ NPP \_ SELECTED.

Si la función no se realiza correctamente, el valor devuelto es otro valor NMERR.

## <a name="remarks"></a>Observaciones

Cuando se le llama, Monitor de red el **cuadro de** diálogo Seleccionar una red, que puede usar para seleccionar una NIC. El BLOB de NPP que representa la NIC seleccionada vuelve a la aplicación que realiza la llamada.

Para obtener información sobre las distintas formas de seleccionar NIC, consulte [Selección de una tarjeta de interfaz de red.](selecting-a-network-interface-card.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[GetNPPBlobFromUI](getnppblobfromui.md)
</dt> <dt>

[GetNPPBlobTable](getnppblobtable.md)
</dt> <dt>

[Entradas blob especiales](special-blob-entries.md)
</dt> </dl>

 

 





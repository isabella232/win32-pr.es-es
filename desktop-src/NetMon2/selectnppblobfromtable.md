---
description: La función SelectNPPBlobFromTable selecciona una NIC de una tabla BLOB de NPP proporcionada.
ms.assetid: 7f8010ed-472a-49b2-8d97-92851b6c14cd
title: Función SelectNPPBlobFromTable (Netmon. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275564"
---
# <a name="selectnppblobfromtable-function"></a>SelectNPPBlobFromTable función)

La función **SelectNPPBlobFromTable** selecciona una NIC de una tabla BLOB de NPP proporcionada.

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

*hWnd* \[ de\]
</dt> <dd>

Identificador de la ventana que muestra el cuadro de diálogo **seleccionar una red** .

</dd> <dt>

*pBlobTable* \[ de\]
</dt> <dd>

Puntero a la tabla de BLOBs proporcionada. Monitor de red usa esta tabla para rellenar el cuadro de diálogo **seleccionar una red** .

</dd> <dt>

*hBlob* \[ enuncia\]
</dt> <dd>

Identificador del BLOB que representa la NIC seleccionada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente y el usuario selecciona una NIC, el valor devuelto es NMERR \_ Success; el BLOB al que apunta *hBlob* se rellena.

Si el usuario no selecciona una NIC, el valor devuelto es NMERR \_ no \_ se \_ selecciona NPP.

Si la función no es correcta, el valor devuelto es otro valor de NMERR.

## <a name="remarks"></a>Observaciones

Cuando se llama, Monitor de red muestra el cuadro de diálogo **seleccionar una red** , que puede usar para seleccionar una NIC. El BLOB NPP que representa la NIC seleccionada vuelve a la aplicación que realiza la llamada.

Para obtener información sobre las distintas formas en que puede seleccionar NIC, consulte [seleccionar una tarjeta de interfaz de red](selecting-a-network-interface-card.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[GetNPPBlobFromUI](getnppblobfromui.md)
</dt> <dt>

[GetNPPBlobTable](getnppblobtable.md)
</dt> <dt>

[Entradas de BLOB especiales](special-blob-entries.md)
</dt> </dl>

 

 





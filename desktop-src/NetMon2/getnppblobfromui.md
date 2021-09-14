---
description: Selecciona una NIC de registro.
ms.assetid: 27814a40-6933-498b-a0d2-535698b1e402
title: Función GetNPPBlobFromUI (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobFromUI
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 4ff3887f10d35ec3b66d8eaaf1443140c768ca55
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171458"
---
# <a name="getnppblobfromui-function"></a>Función GetNPPBlobFromUI

La **función GetNPPBlobFromUI** selecciona una NIC de registro.

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetNPPBlobFromUI(
  _In_  HWND  hwnd,
  _In_  HBLOB hFilterBlob,
  _Out_ HBLOB *phBlob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwnd* \[ En\]
</dt> <dd>

Identificador de una ventana que muestra el **cuadro de diálogo Seleccionar** una red.

</dd> <dt>

*hFilterBlob* \[ En\]
</dt> <dd>

Identificador de un [*blob de filtro*](f.md) que se usa para limitar las NIC que se muestran.

</dd> <dt>

*phBlob* \[ out\]
</dt> <dd>

Puntero al identificador del BLOB que representa la NIC seleccionada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente (el usuario selecciona una NIC), el valor devuelto es NMERR SUCCESS y se rellena el BLOB al que \_ *apunta phBlob.*

Si el usuario no selecciona una NIC, el valor devuelto es **NMERR \_ NO \_ NPP \_ SELECTED**.

Si la función no se realiza correctamente, el valor devuelto es otro valor NMERR.

## <a name="remarks"></a>Observaciones

Cuando se le llama, Monitor de red el cuadro de **diálogo** Seleccionar una red, que puede usar para seleccionar una NIC. El BLOB de NPP que representa la NIC se devuelve a la aplicación que realiza la llamada.

Si el BLOB denominado *por hFilterBlob* es un [*BLOB especial,*](s.md)el buscador intentará procesarlo. Un ejemplo sería una llamada que previamente había devuelto un BLOB especial del NPP remoto. La aplicación insertó la etiqueta necesaria, MACHINE \_ NAME. En esta situación, el buscador pasaría este BLOB al NPP remoto, que devolvería una tabla de blobs de NPP que representa la máquina solicitada. Estos blobs de NPP remotos aparecerán en el cuadro de diálogo.

El autor de la llamada debe [llamar a la función DestroyBlob,](destroyblob.md) que destruye el BLOB devuelto cuando ya no es necesario.



| Para más información sobre | Vea                                                                          |
|----------------------------|------------------------------------------------------------------------------|
| Tres maneras de seleccionar NIC  | [Selección de una tarjeta de interfaz de red](selecting-a-network-interface-card.md) |
| Especificar un blob de filtro   | [Especificar un blob de filtro](specifying-a-filter-blob.md)                     |



 

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

[GetNPPBlobTable](getnppblobtable.md)
</dt> <dt>

[SeleccioneNPPBlobFromTable](selectnppblobfromtable.md)
</dt> </dl>

 

 





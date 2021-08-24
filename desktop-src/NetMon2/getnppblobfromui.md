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
ms.openlocfilehash: d3b88c369145d53d32d23773072f878d9834110e705cd8ff623a3726cbb98b88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743885"
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

Identificador de un [*blob de filtro*](f.md) que se usa para limitar qué NIC se muestran.

</dd> <dt>

*phBlob* \[ out\]
</dt> <dd>

Puntero al identificador del BLOB que representa la NIC seleccionada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente (el usuario selecciona una NIC), el valor devuelto es NMERR SUCCESS y el BLOB al que \_ *apunta phBlob* se rellena.

Si el usuario no selecciona una NIC, el valor devuelto es **NMERR \_ NO \_ NPP \_ SELECTED**.

Si la función no se realiza correctamente, el valor devuelto es otro valor NMERR.

## <a name="remarks"></a>Comentarios

Cuando se le llama, Monitor de red el **cuadro de** diálogo Seleccionar una red, que puede usar para seleccionar una NIC. El blob NPP que representa la NIC se devuelve a la aplicación que realiza la llamada.

Si el BLOB denominado por *hFilterBlob* es un [*BLOB especial,*](s.md)el buscador intentará procesarlo. Un ejemplo sería una llamada que previamente había devuelto un BLOB especial desde el NPP remoto. La aplicación insertó la etiqueta necesaria, MACHINE \_ NAME. En esta situación, el buscador pasaría este BLOB al NPP remoto, que devolvería una tabla de blobs de NPP que representa la máquina solicitada. Estos blobs de NPP remotos aparecerán en el cuadro de diálogo.

El autor de la llamada debe llamar [a la función DestroyBlob,](destroyblob.md) que destruye el BLOB devuelto cuando ya no es necesario.



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



## <a name="see-also"></a>Vea también

<dl> <dt>

[GetNPPBlobTable](getnppblobtable.md)
</dt> <dt>

[SeleccioneNPPBlobFromTable](selectnppblobfromtable.md)
</dt> </dl>

 

 





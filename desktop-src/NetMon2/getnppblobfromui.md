---
description: Selecciona una NIC de registro.
ms.assetid: 27814a40-6933-498b-a0d2-535698b1e402
title: Función GetNPPBlobFromUI (Netmon. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002237"
---
# <a name="getnppblobfromui-function"></a>GetNPPBlobFromUI función)

La función **GetNPPBlobFromUI** selecciona una NIC de registro.

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

*hWnd* \[ de\]
</dt> <dd>

Identificador de una ventana que muestra el cuadro de diálogo **seleccionar una red** .

</dd> <dt>

*hFilterBlob* \[ de\]
</dt> <dd>

Identificador de un [*BLOB de filtro*](f.md) que se usa para limitar las NIC que se muestran.

</dd> <dt>

*phBlob* \[ enuncia\]
</dt> <dd>

Puntero al identificador del BLOB que representa la NIC seleccionada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente (el usuario selecciona una NIC), el valor devuelto es NMERR \_ Success y se rellena el BLOB al que apunta *phBlob* .

Si el usuario no selecciona una NIC, el valor devuelto es **NMERR \_ no \_ se \_ selecciona NPP**.

Si la función no es correcta, el valor devuelto es otro valor de NMERR.

## <a name="remarks"></a>Observaciones

Cuando se llama, Monitor de red muestra el cuadro de diálogo **seleccionar una red** , que puede usar para seleccionar una NIC. El BLOB NPP que representa la NIC se devuelve a la aplicación que realiza la llamada.

Si el BLOB llamado por *hFilterBlob* es un [*BLOB especial*](s.md), el buscador intentará procesarlo. Un ejemplo sería una llamada que anteriormente devolvía un BLOB especial del NPP remoto. La aplicación insertó la etiqueta necesaria, el nombre de la máquina \_ . En esta situación, el buscador pasaría este BLOB al NPP remoto, que luego devolvería una tabla de blobs NPP que representa el equipo solicitado. Estos blobs NPP remotos aparecerán en el cuadro de diálogo.

El llamador debe llamar a la función [DestroyBlob](destroyblob.md) , que destruye el BLOB devuelto cuando ya no es necesario.



| Para más información sobre | Vea                                                                          |
|----------------------------|------------------------------------------------------------------------------|
| Tres formas de seleccionar NIC  | [Seleccionar una tarjeta de interfaz de red](selecting-a-network-interface-card.md) |
| Especificación de un BLOB en filtro   | [Especificación de un BLOB en filtro](specifying-a-filter-blob.md)                     |



 

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

[GetNPPBlobTable](getnppblobtable.md)
</dt> <dt>

[SelectNPPBlobFromTable](selectnppblobfromtable.md)
</dt> </dl>

 

 




